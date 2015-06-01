---
title:  Basic HTML
name:   basic-html-v1
---

We often talk about HTML as code, but writing HTML and CSS is different from *programming*. HTML is a markup language, meaning that it *marks up* or adds structure to text content. CSS tells a web browser how it should display that marked up content, but neither involve any programming logic.  While many web developers are programmers and also write JavaScript for their websites (JavaScript is a programming language), there are some who do not and focus more on web design, marketing, and user experience.

This course will teach you HTML5 and CSS3.  As you work through this material, it is important to keep in mind that different browsers and different operating systems may display the same web page differently.  Both the web browser itself and the version that is installed make a difference.  On top of that, even in the same version of the same browser, the page may look different due to the operating system.  While we will only skim the surface of handling these issues, it is very important to remember this while you develop web pages.  

It is also important to keep in mind that we are learning the latest version of HTML and CSS.  While support for this is currently good in the *latest* version of Chrome and Firefox, Internet Explorer lags a bit behind.  For earlier versions of all browsers, support might not be as strong or it may not be there at all.

#### Template
The core structure of an HTML page is always the same.  You will always begin with the `<!DOCTYPE>` tag. The content of this tag is different based on the version of HTML that you are writing.  This will always be followed by the `<html>` tag.  All of your page's HTML is included between the opening `<html>` and closing `<\html>` tags.  Notice that the closing tag has a \ before the tag name.

Inside the `<html>` tags, you will always have a `<head>` and `<body>` tag.  The content of the `<head>` tag is not shown in the browser display area.  It contains information *about* the page - things like the title, the stylesheet or CSS to apply, and `meta` information.  The contents of the `<body>` tag are what is shown in web browser display area.

<code class="gist" data-gist="5785c6e9534e956b79d7" data-gist-file="basicHTML5.html">
</code>

<div class="well well-sm">
:memo: Note that you can view and bookmark the above template on GitHub by clicking the link at the bottom of the <em>Gist</em>.  (I suggest that if you do that you open it in a new tab or window.)  When looking at it while logged into GitHub, <em>star</em> the gist to bookmark it or <em>fork</em> the gist if you want to be able to alter it.  Gists are snippets of code you want to keep handy.  You can create you own from the + button next to your profile in the upper right.
</div>

#### Nesting of Tags
It is important to understand the structure of HTML is a tree or branching hierarchy - much like a folder structure.  The `<html>` tag is the root of this structure.  Looking at our template it has two children - `<head>` and `<body>`.  These children are between (or inside) the opening and closing tags. You could also say they are *wrapped* (or surrounded) by the `<html>` tag.

Using the Chrome Browser Developer tools, we can view the structure of the HTML similar the the way you might see a file tree shown on your computer.  
<img src="{{ "/assets/topics/basic-html-tree1.png" | prepend:site.baseurl }}"
    alt="Image illustrating the tree structure of the template above. The html tag contains the head and body.">

By clicking the arrow next to a tag name, you can see what is inside of it.
<img src="{{ "/assets/topics/basic-html-tree2.png" | prepend:site.baseurl }}" 
    alt="Image illustrating the tree structure of the template above. The html tag contains the head and body.">
