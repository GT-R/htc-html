---
title: "Structure of the Site"
---

It's been interesting learning about [Jekyll](http://jekyllrb.com/) and trying to put together a structure there that works for what I'm aiming for with this site.  The structure I've decided to work with is built around [Collections](http://jekyllrb.com/docs/collections/).  There is a collection for semesters, sessions, topics, and assignments.

The structure is intended to be flexible and easy to write, without the need for much HTML, however I've been writing more HTML than I expected for alerts and wells and such. I like the ability to write markdown, as it is *much* faster than writing in HTML, but sometimes the combination gets confusing.  

## Semesters
The collection of semesters drives the creation of the <em>current semester</em> nav link and the <em>other semesters</em> nav dropdown. If a semester is marked with the isCurrent variable set to true, then it will be displayed as a main nav link.  If there is only one semester present, it is assumed to be current.  If there is more than one semester file, then a dropdown menu will appear in the nav.  The name will be "All Semesters" if none is marked as current and all semesters will be included in this list.  If there is a current semester, then it will display as "Other Semesters" and the current one will not be included in the list as it will appear as a main nav link separately.

Currently the only semester is for this summer, but once I'm settled into the summer course, I'll begin working on fall.  I expect that the material will evolve a bit each semester, and I want both me and my students to be able to come back to it as it was at any given point in time.


## Sessions & Topics
Each course is made up of sessions.  Typically this course has contained 8 in-class sessions and 7 online sessions.  My main focus in putting together this site is to better structure the online (or at home) sessions to provide a little more direction and interactive learning.

Each session has key skill listed that you should learn from the session, and a list of individual topics. Currently the topics are focused around the reading from the textbook. At some point, I may aim to drop the text and teach the topics directly from this site, but for the time being I don't have the time or desire to write all of that material myself. (And though I balk at the price, the textbook is pretty darn good at what it presents.)

The session layout allows you to page through each topic (ajax loads the topic pages w/out full refresh). The only annoyance with this I have yet to sort out is getting the name off the page.  While it looks like you can do this, it was coming back empty and I didn't have time to sort it out.  I'm currently storing the name in the page as a property. Boo!  


## Assignments
While small assignments are written as topics, the larger project assignments are too large to fit this format.  I also want a way to make those printable for my students who love their paper.  I'm still working on this piece, but I expect it to be a more minimal and clean layout.
