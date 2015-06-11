---
title:  Text CSS
name:   text-css-v1
---

#### Fonts
One of the most common things that you'll do to style a website is choose specific fonts to match the look that is desired for the page.  Remember that fonts fall into 2 main categories: serif and sans-serif. Serif fonts have little marks at the tips of the letters and tend to look more formal and are often used for headings.  Sans-serif fonts tend to be used when a lot of text content is displayed for reading.  Studies have shown sans-serif content is easier to read.

There are also monospace, cursive and fantasy font categories, but those are less commonly used.  They are also typically used only for small sections of text, such as headings or perhaps code snippets in an IT related page.  [CSS Font Stack](http://www.cssfontstack.com/) is a great common font reference.  It will show you font availability for different operating systems and provides good fall back options for when a font is unavailable.

In addition to using CSS to determine which font to use, you can also configure the size, weight, style, alignment, and even convert to upper or lowercase all using CSS.  Some important properties to remember are:

- font-family
- font-size
- font-weight
- font-style
- text-align
- text-decoration
- text-transform

Pay attention to the various ways to set the font size. While older websites tend to set font sizes in pixels, the trend toward responsive design has put more focus on relative font sizes using either em or percentages. Using this type of sizing also helps when visitors zoom in or out on the web page using the browser.  (Try doing either CTR + or - (or CMD + or - on a Mac) when looking at a web page.)


#### List Markers
It is also fairly common to use images for list markers or bullets. (Custom fonts, which we will discuss later are also frequently used for this.)   These are configured using the `list-style-image` property.

Sometimes we don't want to see the markers for our list.  For example if we have a list of `nav` links.  To disable the list markers (bullets or numbers), sets `list-style-type: none`.
