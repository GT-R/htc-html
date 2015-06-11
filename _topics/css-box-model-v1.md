---
title:  CSS Box Model
name:   css-box-model-v1
---

The CSS box model shows an element's size, padding, border, and margin.  Remember that the browser developer tools will illustrate the box model for you for a selected element.  In the image below, you can see the element's size (in the blue area in the center), the padding (the inner green area), the border (the yellow area separating the padding and margin), and the margin (the orange outer area).

<img src="{{ "/assets/topics/css-box-model-ex.png" | prepend:site.baseurl }}"
    alt="Image of the CSS box model diagram from the Chrome developer tools.">

Remember that padding picks up the element's background color, while the margin is transparent and thus shows the color of the parent or containing element.

Key properties:
- width and height
- margin (note both the shorthand and individual properties)
- padding (note both the shorthand and individual properties)
- border (note both the shorthand and individual properties)

Understanding the box model and how it affects the layout of HTML elements is important to creating a *theme* or look-and-feel for your web site.  It controls the size and spacing of elements, which can have a significant effect on your page layout.  It is especially important to consider the visible (padding) and invisible (margin) spacing when moving and *floating* elements outside of their normal positions.  (We will look at in the next session.)  
