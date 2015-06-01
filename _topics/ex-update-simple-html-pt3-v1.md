---
title:  Update the First Web Site - Part 3
name:   ex-update-simple-html-pt3-v1
---

<div class="alert alert-danger" role="alert">
:exclamation: Do not skip this assignment.  I will check your work at the start of the next class.  If you need help, make sure to visit our [Gitter online chat room](https://gitter.im/htc-ccis1301) and/or email me.
</div>

Finally we're going to add some CSS to our First Web Site to make it look good.  I know, you're excited! You can barely wait.

#### Watch and Learn
As you work through this assignment, use the *Live Preview* feature of Brackets to watch the CSS get applied as you write it.  This is one of the best ways to learn and understand how CSS works.  If you are not able to use Brackets or its *Live Preview* feature, make sure to save your work and refresh the browser display frequently to see the effects of the CSS you are writing.

<div class="alert alert-warning" role="alert">
:warning: This assignment may seem a little convoluted, but have some patience.  We are going to explore the CSS Cascade as we get our page to be styled the way that we want it.  This assignment is more about the journey than the destination.
</div>

#### Add Embedded Styles
We're going to start by adding some embedded styles to our Home page.  Recall that embedded styles are added to an HTML page by placing a `<style>` tag in the `<head>` section of the page.  This can seem a little strange at first, but the CSS is written just like any other text content you put into a tag - only the browser knows it is special.

Add CSS inside the `<style>` tag to:

- set the background color to #FFFFCC (light yellow)
- set the text color to #3399CC (medium blue)

Remember to use *Live Preview* to watch the effect that this has on the display of your web page.  Your page should look like this:

<img src="{{ "/assets/topics/ex-update-simple-html-pt3-embedded1.png" | prepend:site.baseurl }}"
    alt="Image illustrating the Home page with the light yellow background and blue text.">

Notice that while we applied the CSS to the body, we see that it is also applied to our headings and paragraphs. They inherit the styles applied to the body because they are child tags of the body.

Next add CSS to set the text color of the top level heading (h1) to black #000000.

<div class="well well-sm">
:memo: There is more information on hexadecimal color codes in your textbook. It is helpful to remember that the codes are always the # sign plus 6-characters. Those characters are restricted to digits (0-9) and the letters A-F. This can help you avoid typos and invalid color codes. It can also be handy to remember that white is #FFFFFF and black is #000000.
</div>

In the live preview, you should see your heading text color change to black.
<img src="{{ "/assets/topics/ex-update-simple-html-pt3-embedded2.png" | prepend:site.baseurl }}"
    alt="Image illustrating the Home page with the light yellow background, black heading (h1) and blue text.">

While the heading still inherits the color style rule from the body, the h1 style rule overrides it.  If you specifically write a rule for a property, that overrides any other values for that property that might be inherited from a parent.  This causes us to see black text, not blue text for the heading.

#### What if you have two rules?
What happens if you have two rules for the same selector? Let's try it out and see!

Add a second h1 selector to your embedded CSS after the one you added above. Then add a property to set the background-color to black.  It should look like this:

{% highlight css %}
h1 {
   color: #000000;
}
h1 {
    background-color: #000000;
}
{% endhighlight %}

In the live preview, you should see the heading get a black background which makes it look like the text disappears.
<img src="{{ "/assets/topics/ex-update-simple-html-pt3-embedded3.png" | prepend:site.baseurl }}"
    alt="Image illustrating what the heading with a black background-color and black text.  You see a black bar or rectangle; you cannot see the text.">

When you have two selectors that are the same at the same level of precedence (both external or both embedded or both inline) they are combined together. When they contain different properties, both properties are applied to the selected element.

Add a second property to the last h1 selector to set the text color to white (#FFFFFF) so that we can read it.

{% highlight css %}
h1 {
   color: #000000;
}
h1 {
   background-color: #000000;
    color: #FFFFFF;
}
{% endhighlight %}

In the live preview, you should have seen the text color change to white.
<img src="{{ "/assets/topics/ex-update-simple-html-pt3-embedded4.png" | prepend:site.baseurl }}"
    alt="Image illustrating the Home page with the light yellow background, black background and white text for the heading (h1), and blue text for everything else.">

When you combine rules for the same selector at the same level of precedence together, if more than one value is given for the same property (like color), then the last value in  wins.

A common error that I see especially in large CSS files is that the student will have the same selector in the file multiple times.  They'll look at one and say "See!  Here I'm setting the color to black.  Why isn't it black?"  And then I'll tell them to search the file to see if the selector is present later on, and sure enough further down in the file they will have another copy of the same selector setting the color to white.

Lesson to learn - before you add a selector to your file, make sure that it isn't already there.  You don't want to have two rules for the h1 like we did above.  You want to have one rule that includes all properties.

Delete the first h1 rule - the one that sets the color to black - from your embedded styles.


#### Add an Inline Style
Inline styles are added to an HTML page by adding the style attribute onto an HTML tag in the page body.

Locate your first level heading in the index.html file.

After the h1 tag name, add the style attribute so that it looks like this:

{% highlight html %}
<h1 style="background-color:#3399CC;">
{% endhighlight %}

You should see the background on the heading change to blue.
<img src="{{ "/assets/topics/ex-update-simple-html-pt3-embedded5.png" | prepend:site.baseurl }}"
    alt="Image illustrating the Home page with the light yellow background, blue background and white text for the heading (h1), and blue text for everything else.">

While the heading still inherits the embedded h1 styles, the inline style overrides it causing the background-color to change to blue. Inline styles override both external and embedded styles.  

While we only have one h1 tag in the document, if we had more than one, the others would still have the black background-color.  An inline style only applies to the HTML tag that it is added onto. This allows you to customize just one instance of a tag.

#### Add an External Style Sheet
Generally you will write all of your CSS in an external style sheet. An external style sheet is a separate file, often called something like style.css. The external style sheet is linked to all the HTML files in your website by adding a `<link>` tag to the head section *in every file*. This provides consistent styling across all of the pages on your website.

Add a new file called style.css to your project, then add `<link>` tags for it to both your Home page and your Goals page.

Let's purple up the site a bit. Open the external style sheet and add the following CSS to the file:

{% highlight css %}
body {
   background-color: #E6E6FA;
   color: #191970;
}
h1 {
   color: #E6E6FA;
   background-color: #191970;
}
p {
   background-color: #AEAED4;
}
{% endhighlight %}

Note that in an external style sheet you should **_never_** have any HTML tags. There should be no `<style>` tag inside your CSS file!

The CSS above should make the page background a light purple, and the text color a dark purple. This is overridden for the h1, which has a dark purple background and a light purple font color. The paragraphs should get a medium purple background.

Does this match what you see?  
<img src="{{ "/assets/topics/ex-update-simple-html-pt3-embedded6.png" | prepend:site.baseurl }}"
    alt="Image illustrating that only the paragraph gets the expected style from the external stylesheet.">

No.  Why not?

The answer is found in the CSS cascade order.  Both the embedded and inline CSS override the external stylesheet.

<img src="{{ "/assets/topics/basic-css-cascade.png" | prepend:site.baseurl }}"
    alt="Illustration of the CSS Cascade: Browser Defaults, Overridden by External Style Sheet, Overridden by Embedded Styles, Overridden by Inline Styles.">

To review, we start with the browser defaults.  These are added to and overridden by the external stylesheet.  Those style rules are then added to and overridden by embedded styles on the HTML page, and finally those can be added to and overridden by any inline styles.

#### Clean up
Remove your embedded styles from the head section of the index.html file. In the Live Preview you should see that the background color is now a light purple and the paragraph text is dark purple. The heading will have the light purple text, but still has the blue background.

Remove the inline style from the h1 element. In the live preview, you should now see the dark purple background on the heading.  The final page should look like this:

<img src="{{ "/assets/topics/ex-update-simple-html-pt3-embedded7.png" | prepend:site.baseurl }}"
    alt="Image illustrating all of the expected styles from the external stylesheet.">

Use the link to go to your goals page.  Make sure it is also styled in purple.  Then use the link to go back to the home page.  

Use the [W3C CSS Validator](http://jigsaw.w3.org/css-validator/) to validate your CSS file and resolve any errors.

#### Assignment Wrap-up
That's it for this project.  Make sure to review, commit and push your changes to GitHub so that you can have your assignment marked off as completed in our next class.
