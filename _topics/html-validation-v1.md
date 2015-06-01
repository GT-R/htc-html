---
title:  HTML Validation
name:   html-validation-v1
---

As you learned earlier, HTML5 is a W3C standard.  As we write HTML pages, it is important to ensure that they conform to that standard.  Pages that validate against this standard are more likely to display correctly and consistently in different web browsers, providing a better user experience.

<div class="alert alert-danger" role="alert">
:exclamation: This is a skill that you are expected to learn in this class. Significant points will be deducted for validation errors in your assignments.
</div>

To determine if a web page is valid HTML5, we can run it through the online [HTML validator](https://validator.w3.org/) provided by the W3C.  Use the HTML file that you created in the previous exercise and validate it on their site.  (I recommend using File Upload.)

If you used my template from the previous exercise, you should have an error.
<img src="{{ "/assets/topics/html-validation-error-top.png" | prepend:site.baseurl }}"
    alt="Image showing the W3C HTML Validation page with an error.">

When you have an error, you'll see that clearly at the top of the page, but you must scroll down to see details on what has caused the error.

<img src="{{ "/assets/topics/html-validation-error-msg.png" | prepend:site.baseurl }}"
    alt="Image showing the W3C HTML Validation page with an error.">

The error message clearly shows you:

- the line number where the problem was identified
- the error message
- the HTML that it is detecting as wrong

Usually these things will point you to the error, but it is up to you to determine how to fix it.  Here the error is saying we can't have a "Bad value for attribute href on element link: Must be non-empty." If you look at the HTML show below, the tag does include href="".  There is no value for the href attribute.  That seems to be the problem.  Now how do we fix it?

On most web pages we create, we will have stylesheets.  That is why I included it in the template code.  However, right now, we haven't learned about them yet and so for this project we don't have one.  Since we don't need the tag, let's just take it out.  (Leave it in your template, but take it out of the index.html file.)

Once you have made the change and saved the index.html file validate it again. This time, you should see no errors and the page should display green instead of red.

<img src="{{ "/assets/topics/html-validation-no-errors.png" | prepend:site.baseurl }}"
    alt="Image showing the W3C HTML Validation page no errors.">

If you made changes to your files, be sure to commit and push those changes to GitHub.


#### Validation Tips

- Make sure that it says it is validating as HTML 5. A missing or incorrect doctype will cause it to make incorrect assumptions.
- Correct errors one at a time. Fixing one error often resolves many. Make one change and then save and validate again.
- Let Brackets help you. It will often highlight tag closure errors along the left margin.
- Watch for double tags or partial double tags, where you typed the tag but Brackets also auto-completed it for you.

If you get stuck with a validation error, try asking one of your peers before you ask me for help.  But *DO* ask for help if you are stuck. These errors are very important to fix, even if you think your page looks fine.

Remember that the [Gitter online chat room](https://gitter.im/htc-ccis1301) is a good place to find me when I am available outside of class, and you can post questions even no one is there. Perhaps another student will be able to help out before I can. Also note that if you call out someone specifically, they can be notified of your message and respond when they are available.
