---
title: Pacific Trails - Part 2
name:  case-study-pacific-pt2-v1
---

<div class="alert alert-danger" role="alert">
  :exclamation: Overall the Pacific Trails Case Study will follow the case study from the textbook, but how we get from beginning to end will be a little different. Please use this assignment sheet to direct your work. The instructions from the end of chapter case studies in the book do not match my assignments.
</div>

## Grading
This assignment is worth 50 points and will be graded as follows:

- All HTML & CSS files are valid - 10 pts (all or nothing)
- Correct HTML5 template and structure elements - 5 pts each, 15 points total
- Page display/functionality in browser matches wireframes - 5pts each, 15 points total
- External Stylesheet is correct - 10 pts

The planned site map:
<img src="{{ "/assets/assignments/cs-pt/sitemap.png" | prepend:site.baseurl }}" title="Pacific Trails site map"
      alt="The site map - a Home Page with sub pages for Yurts, Activities, and Reservations." />


Current wireframes:
<a target="_blank" href="{{ "/assets/assignments/wireframes/PacificTrailsP2-Wireframes.pdf" | prepend:site.baseurl }}">PacificTrailsP2-Wireframes.pdf</a>

## Task 1 - Add Activities Page

### Edit HTML

1. In the project folder, add a new HTML page for Activities (activities.html).

2. Since the layout of the Activities page is very similar to the Yurts page, start by copying and pasting the HTML from the yurts.html file into the activities.html file.

3. Edit the content of the Activities page to reflect the content shown in the wireframes, ignoring the image for now. Be sure to edit the page title as well as body content.

### Validate & Test
Validate the page using the W3C validator. Check your page by viewing it in the browser and comparing it to the wireframes.


## Task 2 - Add Images

### Explore the images folder
To keep web projects neat and orderly, images are typically placed in a folder to keep them separate from the html pages. Most often reason for this is just file system organization. Sometimes however, there are also practical reasons, such as hosting images that change infrequently separately from HTML content that may change more often.

For this assignment we will be using the following images.

- marker.gif
- sunset.jpg
- coast.jpg
- yurt.jpg
- trail.jpg

When adding the images to your HTML pages, you will need to know the dimensions of the image. To determine the dimensions (height and width) of an image, find the image in the file system. If you are on Windows, right-click on the file and select Properties, then click on the Details tab. On a Mac, right-click on the file and select the Get Info option.

### Add the Content Images
The large images in the content area of each of the web pages will be added using HTML &lt;img&gt; tags. The image element is covered in your textbook on pages 132-133.

1. Open the Home page for editing.

2. Add an `<img>` tag for the coast.jpg. Add alt text for the image. It should be a complete sentence that describes the image contents. Set the height and width properties based on the actual image file size.

3. Open the home page in the browser and verify the display of the image. If you are not seeing the image, double check the path on the src attribute of the &lt;img&gt; tag. This path should be relative from the HTML file location, so it will need to include the folder name. See the FAQ at the bottom of pae 137.

4. Once the image displays properly on the Home page, validate the Home page using the W3C validator. Remember that even though a page displays properly, the actual HTML may not be valid.

5. Repeat these steps to add the images to the Yurts and Activities pages.

6. Open both pages in the browser to be sure that the images are showing.

7. Validate the Yurts and Activities page to double-check that there are no errors.


### Add the Header Image
Decorative images, such as the sunset in the header, can be configured using CSS. Configuring these images in the CSS allows them to be modified as part of the *theme* or visual style of the page. Notice that the sunset.jpg has coloration that blends it into the background color of the header. If the background color were to change, then the image would need to be edited as well to achieve the same effect.

1. Open the style sheet for editing.

2. Locate the existing style rule for the header.</p>

3. Add the property for the background image. Set it to not repeat, and position it on the right.

4. Open the Home page in the browser and verify the display of the header image. If you are not seeing the image, double check the url. The path should be relative from the CSS file location, so it will need to include the folder name.

5. Validate the CSS file.


### Add the Image bullet
Images for list bullets are also decorative images, and are configured using CSS. Changing list markers to use images is covered in your textbook on page 145.</p>

1. Open the style sheet for editing.

2. Add a new rule to select ul elements and set the list-style-image to use the marker.gif file.

3. Open the Home page in the browser and verify the display of the new list bullet images. If you are not seeing the image, double check the url.

4. Validate the CSS file.

### Validate & Test

1. Make sure to save all of your files and close your editor.

2. Validate all of your HTML pages and the external CSS file using the appropriate W3C validator.

3. Open the Home page in the browser.

4. Check each of the pages, carefully comparing it to the wireframes.

5. Use the links to navigate between pages to ensure they are not broken.</p>

## Task 3 - CSS for Text and Spacing

### Add CSS for fonts
The wireframes indicate several notes on text styling.  We will use <a href="http://www.cssfontstack.com/" target="_blank">CSS Font Stack</a> to assist us with creating the appropriate font families.

1. Open the style sheet for editing.

2. Locate the existing style declaration for the body. We will configure the default font here, along with the default color we set up in the previous assignment.

3. Use <a href="http://www.cssfontstack.com/" target="_blank">CSS Font Stack</a> to get an appropriate list of fonts to use for Arial.  You can click the icon to have CSS for the font family copied to your clipboard so that you can paste it into the CSS file.

                    <img src="images/P4_UsingCSSFontStack.jpg"
                         title="Using CSS Font Stack"
                         style="width:80%; max-width: 430px;"
                         alt="Screen capture showing how to use CSS font stack." />
4. Add the font family CSS to the existing body rule.

5. Verify the change to the font displayed is displayed in the browser. Note that Arial and sans-serif fonts do not have the serifs (or flags) on the tips of the letters.
                    <img src="images/homeP4_defaultFont.jpg"
                         title="Default San-Serif Font"
                         style="width:80%; max-width: 430px; "
                         alt="Screen capture showing the sans-serif default font." />
6. Next we will add the CSS for the heading fonts.  Locate the existing style declarations for the h1, h2 and h3.  You will need to add one for the h1. Use <a href="http://www.cssfontstack.com/" target="_blank">CSS Font Stack</a> to get an appropriate list of fonts to use for Georgia and update all three heading declarations to use these fonts.

7. Verify the change to the font displayed is displayed in the browser.</p>
                    <img src="images/homeP4_headingFont.jpg"
                         title="Default San-Serif Font"
                         style="width:80%; max-width: 430px; "
                         alt="Screen capture showing the serif heading font." />

8. Next, locate the declaration for the nav.  Add CSS to style the text bold.</p>

9. The links are not underlined in the new wireframes, so we should add CSS to remove the underline <strong>only</strong> for hyperlinks in the nav.</p>

10. The note in the wireframe, also indicates text color changes for the unvisited, visited, and hover hyperlink states.  To code these, you will use pseudo-classes applied to the &lt;a&gt; tag.  (See pages 212-213.  Note order is important.) Add CSS for this, again configuring only links in the nav.

11. Verify the changes to the nav are shown in the browser.
                    <img src="images/homeP4_navFont.jpg"
                         title="Default Nav Font-Styles"
                         style="width:80%; max-width: 430px; "
                         alt="Screen capture showing the updated nav fonts." />

12. The contact information should be smaller, 90%.  In the HTML, add an id of "contact" to the div surrounding the address information. Add a style rule to the CSS file to reduce the font size only for the contact information.  (See page 114 for id information, page 160 for font sizing.)

13. Verify the reduced size of the contact information in the browser.

14. The footer information should also be smaller, 75%.  Add a style rule to the CSS file to reduce the font size only for the footer.

15. The footer information should also be italic and should use the Georgia/serif fonts, similar to the headings.

16. Verify the reduced size and updated styling of the footer information in the browser.

17. The was some feedback that the resort style on the company name is hard to see.  Update the CSS for the resort style class to make the font bold.

18. Verify the company name has a bold font when displayed in the browser.

19. There is also a note to apply text shadow to the second level heading.  Locate the h2 style rules and add a 1px text shadow using the dk grey color from the wireframe palette.

#### Validate & Test

1. Make sure to save all of your files and close your editor.</p>

2. Validate the HTML for the home page and the external CSS file using the appropriate W3C validator.

3. Open the Home page in the browser. Double check all of the items in the font styling note from the wireframes.

4. Check each of the other pages carefully, using the links to navigate between pages.  Pay attention to the h3 styling as there is not an h3 on the home page.</p>

### Center the Content
Next we will add a wrapper div to allow us to center the content in the browser, adding a background image to the body area.  This helps to frame the content better and help it to stand out on the page.

1. Open all of your HTML pages for editing.

2. Update the content div so that it has an id of "content".

3. Add a new div, with an id of "wrapper" surrounding the header, nav, content and footer.  It sits just inside the body, surrounding all of our page content.

4. Open the CSS file.

5. Locate the existing style rule for the body.  Add a rule to set the background image to the ptrbackground.jpg.

6. Add a rule to set the background color for the wrapper div to white.

7. Add a new style rule  for the wrapper div.  We need to set the background color to white, set the width to 80% and the minimum width to 960px.

8. The wrapper should also be centered in the browser window.  Configure the margins to do this.  

9. There is also a note for box shadow.  No specifics are given, so we'll just aim for a pretty standard configuration of about 5px and use the dark blue color from the wireframe color palette.

#### Validate & Test

1. Make sure to save all of your files and close your editor.

2. Validate all of your HTML pages and the external CSS file using the appropriate W3C validator.

3. Open the Home page in the browser. The page should look similar to the image below.  <img src="images/homeP4_wrapper.jpg"
                         title="Pacific Trails Centered"
                         style="width:80%; max-width: 500px; "
                         alt="Screen capture of Home with centered content." />

4. Check each of the other pages carefully, using the links to navigate between pages.

### Fix the Spacing
While our page is looking good, things are a bit squished, and we still have that gap between the header and the nav.  We'll fix this up by configuring margin and padding.

1. Open the CSS file.

2. Let's start by removing the ugly gap.  If you examine the header element using the browser dev tools, you can see that there is a large bottom margin on the h1 element.
<img src="images/homeP4_headerGapDevTool.jpg"
                         title="Pacific Trails Header Gap in the Dev Tools"
                         style="width:80%; max-width: 500px; "
                         alt="Screen capture of Chrome Dev Tools showing the h1 box model and the large margin configured." />

3. To remove the gap, set the bottom margin on the h1 to 0.

4. Check the page display in the browser to confirm the gap is gone.

5. Much of the content squishing is on the left side.  To address that, we will add padding focusing on the left side.  About 20px should do it.

6. There is also a note that the header is too short and to add 10px of padding to all sides.  Adding the padding to the h1 instead of the header results in a more pleasing look.  (Try it both ways and see.)

7. For the nav, add 20px on the left and 5px on the top, bottom and right side.  For the content div, add 1px on top, and 20 on the left, right and bottom.  For the footer, add 20px on all sides. Note that if you had previously used line breaks in the HTML to separate the content from the footer, you should remove those.

<div class="alert alert-warning" role="alert">
:warning: Why do we increase the padding as opposed to the margin?</strong> Remember that gap between the header and the nav?  Margin space is "outside" the element boundaries, so the background color does not fill that space.  By increasing the space "inside" the element boundaries, the element background color fills that space and the text or other content moves away from the edge.  (Review the box model in your textbook.)
</div>

#### Validate & Test
1. Make sure to save all of your files and close your editor.</p>

2. Validate the style sheet file using the W3C CSS validator.</p>

3. Open the Home page in the browser. The page should look similar to the image below.   <img src="images/homeP4_spacing.jpg"
                         title="Pacific Trails Spacing"
                         style="width:80%; max-width: 500px; "
                         alt="Screen capture of Home with margins and padding configured." />
4. Check each of the other pages carefully, using the links to navigate between pages.


## Submit the Assignment
Before you zip your project folder for submission:</p>

1. If your editor is open, double check that you have saved all your files and close the editor.

2. Find your project folder in the file system, and open the index.html page in the Chrome browser. It should looks something like this: <img src="images/homeP3.jpg"
                         title="Pacific Trails Home Part3"
                         style="width: 400px; height: auto;"
                         alt="Screen capture of the home page with images." />

3. Using the navigation links, verify the Yurts and Activities pages against the wireframes.

4. Next open the Home page in a different browser such as Internet Explorer, Safari, or Firefox. Again re-check that all pages match the wireframes.

5. Use the W3C Validator to re-validate the CSS and all HTML pages.


When everything looks good, push your files up to GitHub and submit a pull request to have your work graded.  

Also, zip the project folder and upload to the D2L dropbox.
