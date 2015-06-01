---
title:  Make a Simple Web Site
name:   ex-simple-html-pt1-v1
---

Now we're going to put our skills to use.  We'll use the template above to make a simple web page that shows the text "Web development is awesome!!!"

#### Start with a folder
Every web project you make should start with a folder.  Pick a spot on your computer (or portable drive) and create a folder called `firstWebSite`.  

<div class="alert alert-danger" role="alert">
:exclamation: It is is very important that you do not use spaces in your web site file or folder names.  You will lose points on assignments for this!
</div>

Next open [Brackets](http://brackets.io/).  It has some excellent features that allow you see your HTML/CSS in the browser as you write it.  Because of this, I strongly encourage you to use it for this course.  The *Live Preview* feature of Brackets requires the [Google Chrome](https://www.google.com/intl/en/chrome/browser/desktop/) browser.  Make sure that you have it and have updated to the latest version.

Open the `firstWebSite` folder you created for your project.  Use the main menu to select File -> Open Folder... and browse to your `firstWebSite` folder.  
<div class="well well-sm">
:memo: You should always open your project folder in Brackets, as opposed to just a single file. Many of its features do not work as well if it does not have control of the entire project folder.
</div>

#### Make the Home page
Once you have the folder open, right-click in the space below the folder name to create a new folder in that file.
<img src="{{ "/assets/topics/ex-simple-html-pt1-brackets-new-file.png" | prepend:site.baseurl }}"
    alt="Image illustrating using the context menu to create a new file in Brackets.">

Click on the name to change it to `index.html`.
<div class="alert alert-danger" role="alert">
:exclamation: Using index.html as the file name for your web site's main page is a web standard.  You will lose points on assignments if the main (or home) page is not called index.html!
</div>

Paste in the basic template that you learned in the previous topic.  Change the title to "First Web Site".  (The title is in the head section.)  

#### Look at it in Chrome
The Brackets *Live Preview* feature allows you to see your file in the browser while you edit it.  To open it, click on the lightning bolt icon along the right side of the window.
<img src="{{ "/assets/topics/ex-simple-html-pt1-brackets-preview.png" | prepend:site.baseurl }}"
    alt="Image illustrating location of the lightning bolt icon to start the live preview.">

When working with the *Live Preview* feature, it is nice to position your editor and the browser side by side if you have a large enough monitor or better yet if you have two monitors. This allows you to see your page change in the browser as you edit it.
<img src="{{ "/assets/topics/ex-simple-html-pt1-brackets-with-chrome.png" | prepend:site.baseurl }}"
    alt="Image illustrating side by side positioning of Brackets and Chrome.">

Watch the *Live Preview* change as you update the body to have the content "Web development is awesome!!!"

#### Make a repository
We've made our first page. Don't worry, we'll make it look better next week. For now let's make sure we don't lose it by saving it to a new [GitHub](https://github.com/) repository.  

From your main page, click the Repositories tab, then click the button to make a new repository.  Name your repository `firstWebSite`, just like your project folder.  Give it a description, and leave it set as a public repository. (That will allow me to check it out over the next few weeks as we finish it up.)  

Don't initialize it.  Click the button to `Create repository`.

On the next page, you'll notice that it gives you some information to create a new repository from the command line.  We'll be following along with those steps (and adding in a few more).

First, copy that HTTPS url from the quick setup.  Open your command shell and go to your project folder.  Enter the following commands, filling in the appropriate values for your name, email, and URL.

{% highlight bash %}
$ git init
$ git config user.name <your-full-name>
$ git config user.email <your-github-email>
$ git remote add origin <your-remote-url>
{% endhighlight %}


#### Add suggested files
Next, we're going to set up a few basic files every repository should have:

- .gitignore
- README.md
- LICENSE.md (optional)

Firs let's add the `.gitignore` file.  This prevents stuff we don't want versioned from ending up in our repository.  Go back to Brackets and create a new file called `.gitignore` in your project folder.  Give it the following contents, then save the file.

{% highlight bash %}
.DS_store*
*~
._*
*#*#*
*Thumbs.db*
ehthumbs.db
.Spotlight-V100
.Trashes
{% endhighlight %}

Make a new file called `README.md` - .md stands for [Markdown](https://help.github.com/articles/markdown-basics/), it is a simple markup language used on GitHub. Give it the following contents, then save the file.

{% highlight html %}
# First Web Site
This is the first project created in my HTML course.  We're not just learning HTML; we're learning to use git to version files on GitHub too!
{% endhighlight %}

Optionally you can create a LICENSE.md file.  You'll notice a lot of my stuff uses a [Creative Commons (CC) License](https://creativecommons.org/licenses/). Putting things out on GitHub publicly does mean you are giving stuff out for free, but Licenses allow you to do this with the understanding of certain restrictions (like non-commercial use only).  Adding a license to this project really isn't important.  (It isn't going to be anything someone couldn't whip up in a few minutes if they knew what they were doing.)  But you may want to keep this in mind for future projects you put out publicly on GitHub.

#### Commit and push
Now it's time to add our files to the local repository, commit, and push those file to GitHub.

{% highlight bash %}
$ git add .
$ git status
{% endhighlight %}

From the `git status` command, you should see that you have 3 new files (or 4 if you added a License) to commit.  If you see other files, especially ones you do not expect, you should remove those now.  

To remove a file (if you need to), once it has been added to git:
{% highlight bash %}
$ git rm <full-file-path>
{% endhighlight %}

When the `git status` command shows you the correct files and you are ready to commit, enter:
{% highlight bash %}
$ git commit -m "initial commit of my first web project"
$ git push origin master
{% endhighlight %}

#### Assignment Wrap-up
That's all we'll do with this project now, but we'll come back to it later and add some more HTML and CSS to make it look better.  

As you work on the hands on practice assignments that go with your assigned reading, you may want to get some additional practice working with Git and GitHub as well.  Going forward, I won't be giving you all the commands to use.  You'll need to remember them, or know where to look them up.  You might want to make your own [Gist](https://gist.github.com/) cheat sheet.
