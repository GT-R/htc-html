---
title:  Update the First Web Site - Part 2
name:   ex-update-simple-html-pt2-v1
---

We're going to continue updating the First Web Site that we started by adding the HTML5 structural elements, a second page for the goals, and a link to your main GitHub account page.

<div class="alert alert-danger" role="alert">
:exclamation: Do not skip this assignment.  I will check your work at the start of the next class.  If you need help, make sure to visit our [Gitter online chat room](https://gitter.im/htc-ccis1301) and/or email me.
</div>

#### Target
So that you have some idea where we are going, here is what you site should look like when you are finished.


##### The Home Page

<img src="{{ "/assets/topics/ex-update-simple-html-pt2-home.png" | prepend:site.baseurl }}"
    alt="Image illustrating what the Home page should look like.">

##### The Goals Page
<img src="{{ "/assets/topics/ex-update-simple-html-pt2-goals.png" | prepend:site.baseurl }}"
        alt="Image illustrating what the Goals page should look like.">


#### Add HTML5 Structural Elements
Update your page to have:

- a `<header>` (surrounding the `<h1>` tag)
- an empty (for now) `<nav>` tag following the header
- a `<footer>` (surrounding the `<hr>` and the copyright info.  

Next, add a `<div>` with the id="content" around the main page content - everything below the `<nav>` and above the `<footer>`.  Now everything in your page body should be contained inside one of these structural elements.

#### Fill in the Nav with Links
We are going to some links to our site to fill in the `<nav>`.  Since it is a *list* of links, we will add them as an unordered list.  Add the following, setting the appropriate value for the `href` in each link:

- Home - a link to the index.html page
- Goals - a link to the soon-to-be-created new page (call this goals.html)
- My Stuff on GitHub - a link to your GitHub account


#### Add Your Email
Add your email to the footer.  This doesn't have to be your *real* email address if you don't want it to be. (Though I'd encourage you to have a way for people to contact you from GitHub. Good for future job hunting.)

Right now though, it is just important that this is a proper email link, even if it doesn't connect to a real account.


#### Make the Goals page
Make the goals.html page by creating a new file and copying over the contents from your home page.  Then delete the content above the goals, and make the goals heading an `<h2>`.  Finally, remove the goals information from your Home page.  

<div class="alert alert-info" role="alert">
It is important to test your links on all of your pages before submitting your work. I will often find that a link works to get to a new page, but the links don't work to go back or to go to other pages. Make sure to keep your nav consistent and well tested.
</div>


#### Assignment Wrap-up
Validate both of your HTML pages using the [W3C HTML validator](https://validator.w3.org/) and correct any errors.  Then review (`git status`) and commit your changes.

That's all we'll do with this project now, but we'll come back to it again after the next section to and add some CSS to make it look better.  
