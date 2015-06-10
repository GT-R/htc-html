---
title: Chrome Developer Tools 
name:  dev-tools-pt1-v1
---


Access the Developer Tools in Chrome from the Chrome menu in the top right corner of the window. Select Tools ­> Developer Tools. (It is helpful to learn the shortcuts.)

The DevTools window will appear at the bottom of the browser window. You can have it open in a separate window (click on) or move it to the side (click and hold for sub­menu) by using the window pop­out button in the upper right.

The main window has eight main groups of tools accessible as tabs along the top, that support various aspects of web development. We will go through some basics, but you can learn more about the DevTools from the [Chrome DevTools Overview](https://developer.chrome.com/devtools).

### The Elements Tab
This tab is very helpful when working with HTML and CSS. The left side of the view shows you the DOM tree and allows you to view and modify and remove elements. If you select an element on the left, you can see the CSS applied to that element in the window on the right.

There are multiple tabs on the right side. The Styles tab shows all of the styles applicable to the selected element from the highest priority to the lowest.

You’ll notice that some may have strikethrough text. This means that style is overridden.  Generally speaking styles will *cascade* by the following rules, where number one has the highest priority:

1. Inline style (inside an HTML element)
2. Internal style sheet (in the head section)
3. External style sheet
4. Browser default

This matches the order you will see them (top to bottom) the in Styles tab.
Click on the <div id=”footer”> in the DOM tree. Notice that when you click on the element in the DOM tree, it highlights in the main browser window.

If you switch to the Computed tab, you will see the end result of applying the styles. It also has a very helpful display of the CSS box­model for margins, border & padding. We’ll be taking advantage of that more later, but it's a very helpful feature as you begin adjusting the page layout.

#### Editing CSS
You can experiment with getting your styles right by editing them directly in the DevTools. For example, you can edit the background color of the footer by clicking on the little color block which brings up a color chooser.

This can be particularly helpful when editing margins, padding and positioning when you aren’t sure exactly how many pixels you need. You can also add new properties to an existing rule or use the + (in the upper right) to add a new style.

Note:​While editing in the browser can help you get the look you want, these styles will be gone when you refresh the page. You need to copy the changes you make here into your CSS or HTML file.


### Modifying the DOM
You can also modify the HTML through the developer tools. If you select an element, such as the <div id=”footer> and right click on it in the DOM tree view, you will see options to edit or delete that element.

You can add or edit attributes, edit the HTML, copy it to the clipboard, or delete a node. You can also use drag-­and-­drop to move items around in the DOM tree. Just as with the CSS, any changes made here are gone when the page is refreshed, so you need to make sure those are also made in your HTML file if you want to keep them.
