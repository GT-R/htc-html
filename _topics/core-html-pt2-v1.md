---
title:  Core HTML Part 2
name:   core-html-pt2-v1
---

This section covers highlights from the last part of Chapter 2 of your textbook.  Again, these are only highlights, and it is expected that you will fill in the details by reading the material presented in the textbook.


#### HTML5 and Web Browsers
For this class it is important that you are working with a browser that has good support of HTML5.  I strongly encourage you to work with the latest version of the [Google Chrome](http://www.google.com/chrome/) browser.  It has very high support of new HTML5 features and also has excellent developer tools.  Firefox is a decent fallback, but do not use Internet Explorer or Safari as your main browser for this course. (Feel free to use them as a comparison, but for now do not be overly concerned by differences or problems with their display.)

How can you tell if a browser will support the HTML tags that you want to use?  There are many sites on the internet, such as  [CanIUse?](http://caniuse.com/) that are dedicated to providing this information, as it is a common problem that all web developers face.

 Alongside the information on browser support of these features, it is important to know what browsers and versions are most used.  This information can be quite dynamic, as it also includes browsers used on mobile devices. One site that provides such information is [NetMarketShare](https://www.netmarketshare.com/browser-market-share.aspx?qprid=2&qpcustomd=0)

As you can see this is not a simple issue.  Fortunately there are many tools, libraries, and frameworks available to help us deal with the problems caused by the different levels of support found in various browsers. As we start to learn CSS, we'll address some simple issues, and will follow up on this at the end of the class as we discuss some web frameworks and libraries.  However it is a large issue, and a comprehensive discussion is beyond the scope of this course.


#### HTML5 Structural Elements
These tags are used to call attention to special words or phrases. In the previous section we learned to structure the content of our site.  Now we are going to look at the HTML tags to structure the web page itself.  

The HTML5 structural elements `<header>`, `<nav>`, and `<footer>` support a structure that was common across most websites before these tags were created.  At that time, it was common to see `<div>` tags used instead with ids to indicate they represented the page header, navigation, and footer.

We will use these structural tags for the websites that we develop in this course, so having a template or [Gist](https://gist.github.com/) for this code will be helpful.
<code class="gist" data-gist="5785c6e9534e956b79d7" data-gist-file="structuredHTML5.html">
</code>

Note that I've also used comments to highlight each structural area.  You can remove these if you like, but I find that the comments often help these tags to stand out more once you have all of their inner html filled in.  Comments are often shown in editors in a different color from other tags.

<div class="alert alert-warning" role="alert">
:warning: The hands on practice for this section (and likely others too) has you use &lt;b&gt; and &lt;i&gt; tags in ways I've told you not to - strictly for appearance. Keep in mind that it is <em>not</em> the proper way to alter the appearance of these things; it is just the only way that you know right now. Don't make a habit of it.
</div>

#### Div Tags
The `<div>` tag is not new to HTML5. It's been around and is used all over the place.  You will commonly see `<div>` tags inside of `<div>` tags inside of `<div>` tags.  Get used to the idea that you can put them pretty much anywhere and use them to group just about anything you want.  

They are often used to apply a particular look (or style) to a set of HTML tags. This is done by adding `id` or `class` attributes onto the div.  We'll talk more about this after we have learned some basic CSS.

#### HTML Attributes
An attribute is a name/value pair that is placed inside the HTML tag after the tag name.  Common attributes are `id` and `class`, as they can be used on any HTML tag.

{% highlight html %}  
<div id="myId" class="specialStyle">
   Some stuff in the div.  A div can contain text and/or other tags.
</div>
{% endhighlight %}

Notice that the attribute name is followed by an = and the value is in quotes.  It is not required that an attribute has a value, but most of them do.  If you put an id on your tag, it is required for the value to be unique on that particular web page.  (It is OK to reuse it on a different page, but it can only be used once per page.)

There are other attributes that are only used on certain tags, and some HTML tags require certain attributes in order to be valid.  (We'll see an example of this for links in the next section.)  


#### Links
Web pages would probably not be as popular as they are if there wasn't a way to link from page to page and site to site. In fact links or *hyperlinks* are so important they are the *H* in HTML.  

You make a link with the `<a>` or anchor tag.  It is very common for beginners to confuse this with the actual `<link>` tag which has a very different purpose - to *link* the page to a stylesheet or CSS file.  Keep this in mind from the beginning and you'll *anchor* this in your mind forever.

The most important concept around links is getting the path for the `href` attribute correct. If this is not correct, your link won't work and you'll get an error saying the page could not be found.  This is mainly a concern for relative links within your site, though it can apply to external links too.  However you'll usually be able to copy external links, but you have to figure out the path yourself for files in your own site.

Remember that relative links *do not* include http and *do not* start with a / character.  They must contain the full path from the current document to the one that you want to get to.  For small websites that do not use folders, this is simple, just use the file name.  If the other file is in a folder, you must include the folder name as well.  

<div class="alert alert-danger" role="alert">
:exclamation: Pay attention to the text that you use for the actual link - the text inside the open and close &lt;a&gt; tags.  You should not use text like "click here" or "see this". You should use specific descriptive text for what you are linking to or the name of the other page or site.  This supports accessibility and offers a better user experience for everyone.
</div>


#### Email Links
Email contact information is another common feature found on websites. Trends around this have varied over the years as people have tried many different things to avoid having their email addresses picked up off websites and used for spam.  Unfortunately as quickly as people come up with ways to try and get around this, the spammers find ways to circumvent their efforts.  

The best approach is really to let your email software deal with the spam and to just use and display the email address clearly and visibly on the web page.  This provides the best user experience for your visitors - with or without accessibility concerns.


#### Check-in
If you've been reading along with me, at this point you should have finished Chapter 2.  Take a few minutes to answer the Review Questions at the end of the chapter before moving on .  These questions are similar to the ones that you will be asked on the course exams.  Answers to the review questions are found in the back of the textbook.
