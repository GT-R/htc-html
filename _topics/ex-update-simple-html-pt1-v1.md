---
title:  Update the First Web Site
name:   ex-update-simple-html-pt1-v1
---

We're going to update the First Web Site that we started in class.  To begin, you'll want to clone your firstWebSite repository to your home computer. Remember how to do this?  If not, it is similar to what you did to get the students repository in the [Intro to Git and GitHub, Student Directory](http://htcmosman.github.io/courses-gen/documents/intro-to-git.html) assignment that we did in class.

<div class="alert alert-danger" role="alert">
:exclamation: Do not skip this assignment.  I will check your work at the start of the next class.  If you need help, make sure to visit our [Gitter online chat room](https://gitter.im/htc-ccis1301) and/or email me.
</div>

#### Update the home page
Remember that a website's home page is called `index.html`.  Open this file in [Brackets](http://brackets.io/).  Use the *Live Preview* feature to watch how the page changes in the browser as you update the HTML in the editor.

Update the page so that it looks like the image below.  What tags do you need to use?  It's your job to figure that out for yourself based on what you have learned in the previous section.  Think of this as a quiz.  

<a href="{{ "/assets/topics/ex-update-simple-html-pt1-page.png" | prepend:site.baseurl }}" target="_blank">
    <img src="{{ "/assets/topics/ex-update-simple-html-pt1-page.png" | prepend:site.baseurl }}"
        alt="Image illustrating what the final web site should look like.">
</a>

Hard to see the text in the image above?  Click on it to open in a new tab or window and you can use zoom to magnify the view.

#### Assignment Wrap-up
That's all we'll do for now, but we'll come back to it after each section of reading and add a little bit more to it.  

For now let's commit our changes.  Go to your command shell and check the `git status`.  You should see something like this:

{% highlight bash %}
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")
{% endhighlight %}

What's the deal?  We've already added the file right?  After all we've committed it before.  

Git allows you to selectively stage modifications for commit.  Why? Maybe you have a few different files and only one is really ready to go.  (Want more details?  Read more about the three Git States in the online [Pro Git](http://git-scm.com/book/en/v2/Getting-Started-Git-Basics#The-Three-States) book.)  

Because of this, you'll need to do one of two things:

1. Use the `git add` command to stage your modified file.
2. Use the -a flag on the `git commit` command.

Either will do, but this time let's use the -a flag this time for practice.

{% highlight bash %}
$ git commit -a -m "updates for session 1 HW, practice pt-1"
{% endhighlight %}

Once your changes are committed (and optionally pushed to GitHub) you are ready to move on.
