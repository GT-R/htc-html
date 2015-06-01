---
title:  Core HTML Part 1
name:   core-html-pt1-v1
---

This section covers highlights from the first part of Chapter 2 of your textbook.  These are only highlights, and it is expected that you will fill in the details by reading the material presented in the textbook. Don't skip things just because I don't point them out here.  However, if you are short on time, those are good things to skim.  

I expect that you will work through the hands on practice exercises provided in the textbook. While these are not graded, they will give you practice with the techniques that you will use for the larger case study assignments that are graded.  It is suggested that you make a [GitHub](http://github.com/) repository for these practice exercises, as that will give you practice working both with HTML/CSS and managing your files using Git.

<div class="well well-sm">
:memo: Remember that all of the tags that we learn about here are placed inside the HTML body.  Web browsers will display the tags in the body in the display area.  Tags in the head section are not shown (though the title is used for the name of the browser window or tab) and only provide information *about* the document.
</div>


#### Headings and Paragraphs
Headings and paragraphs provide structure for the main content of your pages.  The headings provide an outline, and paragraphs provide the details underneath.  The `<h1>` tag is used for the most general heading, followed by the `<h2>`, `<h3>`, etc.  The proper use of headings to outline the structure of your pages supports a good user experience as well as accessibility tools.

It is a common mistake for beginners to choose a heading tag based on it's appearance (size) in the web browser.  *Do not do this!*  Even if you think the `<h1>` tag is too big or don't like the way it looks, use it for your main or top level heading(s).  It is the structure that is important right now, not the appearance.  We will soon learn how to modify the default way that tags are displayed in the browser using CSS.  

When designing web sites, it is often helpful to get some dummy text to put on your page to work on your layout.  Traditionally, *fake* Latin text called lorem ipsum is used for this. The [Lorem ipsum](http://www.lipsum.com/) website will generate various amounts of this text for you to use on your page while you work on the layout.  You can then come back later and replace it with the actual content text.


#### Phrase Elements
These tags are used to call attention to special words or phrases. They change the appearance of the text in browser specific ways, but again, that is easy to change and control with CSS.  When using these tags, focus on the meaning or structure over the appearance.  

Another common beginner mistake is to use `<b>` or `<i>` tags with other tags to change the way they are displayed.  For example, perhaps you want your headings to be italicized.  You might do this:

{% highlight html %}
<h2><i>My Heading</i></h2>
{% endhighlight %}

A better choice would be to use CSS to italicize the heading text.  By using CSS, all `<h2>` tags would be italicized the same way, providing a more consistent experience for the visitors to your website.

So when *would* you use the `<i>` tag and *not* CSS?  Exactly in an instance like the previous sentence.  When you want to call attention to specific words or text.
{% highlight html %}
<p>
   So when <i>would</i> you use the &lt;i&gt; tag and <i>not</i> CSS?  
   Exactly in an instance like the previous sentence.  
   When you want to call attention to specific words or text.
</p>
{% endhighlight %}

Notice that in the example above, when I am talking about the `<i>` tag but not wanting to italicize the text I used `&lt;` and `&gt;` around the i instead of the < and >.  These are special entity characters.  We will learn more about them soon.

<div class="well well-sm">
:memo: Technically, for HTML5 with its focus on semantic markup, the &lt;em&gt; or &lt;strong&gt; tag would be a better choice over &lt;i&gt; and &lt;b&gt;.
</div>


#### Lists
Lists - both ordered and unordered - are very common on websites.  They are used both for structure and display.  Most web sites have a set of links that serves as the website's main navigation.  This is often not displayed as a bullet-point list, but structurally it *is* a list.  Again, remember that CSS allows us to change the display of HTML tags.  Even if you do not want to see something as a bullet-point or numbered list, if is is structurally a list then you should mark it up using HTML list tags.

A common beginner mistake is to mark up the list items using `<li>` tags, but to forget to put the `<ul>` or `<ol>` tags around them.  It is also easy to forget the closing `</ul>` or `</ol>` tag at the end of the list.  A good practice is to write both the open and close list tags first, then move the cursor back in between them to start writing the list item `<li>` tags.

Description lists are less commonly used on websites, mainly because structurally they are just less common for the content most commonly seen.  While the layout might *look* nice, again remember that your HTML tags should reflect the structure of the content, not how you want it to appear.  If your content is not text and a description or definition, do not use a definition list to mark it up.


#### Special entity characters
These special codes are used to insert symbols into your web page.  These are often things that you cannot type (like a &copy; copyright symbol), or a character that you could type but that has a special meaning in HTML markup (like the < character).  

I will expect you to know and use the following in your web pages:

- `&copy`
- `&lt;`
- `&gt;`
- `&amp;`
- `&nbsp;`

Be careful that if you want to use the & character on your page that you remember to use the `&amp;` entity.  It is easy to forget this.


#### Check-in
If you've been reading along with me, at this point you should have covered the first part of Chapter 2, up to HTML Syntax Validation.  This is pages 26-43  in the 2nd edition, or 28-45 in the 3rd edition.

If you haven't done this yet, do it now before moving on.  In the next exercise, we will update your First Web Site with some new HTML tags.
