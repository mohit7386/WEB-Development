VS Code Shortcuts- 
1- Alt + shift + downarrow - gives you the same multiple lines..
2- Alt + click - when you use this shortcuts then multiple cursors will made and you can write the same thing in multiple places
------------------------------------------------------------
HTML offers multiple ways to select and style elements. Two of the most commonly used selectors are IDs and Classes. This blog explores what they are, how to use them, and their differences.

What is an ID?
An ID is an attribute, a unique identifier assigned to only one HTML element within a page. It is often used for unique styling and JavaScript manipulations.

<div id="myUniqueID">This is a div with an ID.</div>
#id should be unique we can only use one id at a time...

What are Classes?
The class attribute lets you give the same name to multiple HTML elements. That way, you can easily change their look or behavior all at once. Classes are not unique and can be assigned to multiple elements. They are generally used for applying the same styles or behaviors to a group of elements.

<div class="myClass">This is a div with a class.</div>
<p class="myClass">This is a paragraph with the same class.</p>
.class should be used multiple times. We can use same class again n again for styling the web page.

The Style Tag
The style tag in HTML is used to include embedded CSS (Cascading Style Sheets) within an HTML document. It is commonly placed within the <head> section of the HTML file, although it can technically be used in the <body> as well. The style tag allows you to define the look and feel of various HTML elements on the page, including their colors, sizes, margins, and other visual styles.

Here's a simple example:

<!DOCTYPE html>
<html>
<head>
  <style>
    /* CSS rules go here */
    p {
      color: blue;
      font-size: 18px;
    }
    .highlight {
      background-color: yellow;
    }
  </style>
</head>
<body>
  <p>This is a blue paragraph.</p>
  <p class="highlight">This paragraph has a yellow background.</p>
</body>
</html>

In this example, we have targetted the second paragraph by its class name in CSS. The style tag is used to add CSS right into HTML. We will learn about CSS and selectors later in the CSS tutorial

Using IDs and Classes in CSS
In CSS, elements with IDs are selected using a hash (#) symbol before the ID, and elements with classes are selected using a dot (.) before the class name.

/* CSS for ID */
#myUniqueID {
  background-color: yellow;
}

/* CSS for Class */
.myClass {
  font-size: 18px;
}

Differences Between IDs and Classes

Uniqueness: IDs are unique, and classes can be reused.
JavaScript: IDs are often used for JavaScript operations.
Styling: Both can be used for styling, but IDs have (higher specificity).

Conclusion-
Understanding the difference between IDs and Classes is crucial for effective web development. While IDs are for unique elements, classes are for grouping elements.
-------------------------------------------------------------
HTML Inline Elements
Inline Elements don't start on a new line. It only takes the width required to cover the content. Only takes the width as mch needed.

HTML elements are generally divided into two categories: Block-level and Inline elements.

No matter what the width is, block elements will always start on a new line and take up the full available width of their container by default. This means they essentially claim all the horizontal space for themselves, pushing any content that comes after them to a new line. But the inline elements will fit snugly within the flow of other elements, taking up only as much width as their content requires.

What are Inline Elements?
Inline elements do not start on a new line and only take up as much width as necessary. They are part of the flow within other elements.

Inline elements can contain other inline elements, but they generally should not contain block-level elements. For example, you could nest a <strong> (strong emphasis) element within a <span> (a generic inline container) element, like so:

<span>This is <strong>important</strong> text.</span>

However, placing a block-level element like a <div> or <p> inside an inline element like <span> or <a> is typically considered incorrect HTML and could lead to unexpected behavior in terms of layout and styling.

<!-- This is generally considered incorrect -->
<span>This is <div>not recommended</div> text.</span>
Common Inline Elements
<span>: A generic inline container for text
<a>: Defines a hyperlink
<strong>: Defines important text
<em>: Defines emphasized text
<img>: Embeds an image
<input>: Defines an input control
Examples
Here is an example of using inline elements within a paragraph.

This text contains a link, an important text, and an emphasized text.

Styling Inline Elements
You can use CSS to style inline elements. However, some properties like width and height may not apply.

Here is an exhaustive list of the most used Inline Elements:

<a>
<abbr>
<acronym>
<button>
<br>
<big>
<bdo>
<b>
<cite>
<code>
<dfn>
<i>
<em>
<img>
<input>
<kbd>
<label>
<map>
<object>
<output>
<tt>
<time>
<samp>
<script>
<select>
<small>
<span>
<strong>
<sub>
<sup>
<textarea>
---------------------------------------------------------
CLS - Cumulative Layout shift

Sure! Imagine you're reading an article online, and just as you're about to click on a link, an ad suddenly pops up, pushing the content down. That's what Cumulative Layout Shift (CLS) measures.

CLS is a way to see how much the elements on a webpage move around while it's loading. For example, if you're trying to click a button but it moves because an image loads, that's a layout shift.
It all means ki jb aap click kr rhe hain kisi link ya button pe then because of delay in some images then on the clicking suddenly an image opens then your button is shifted downword....So it's very annoying for the user......
------------------------------------------------------------
The <video> Tag
The <video> tag is used to embed video files in an HTML document. It supports multiple attributes to control the video playback.

Example usage:

<video src="video.mp4" controls></video>
Attributes for <video> Tag
src: Specifies the path to the video file.
controls: Adds video controls, like play, pause, and volume.
autoplay: Automatically starts playing the video when the page loads.
loop: Repeats the video once it ends.
muted: Mutes the video by default.
poster: Specifies an image to be displayed before the video starts playing.
width and height: Specifies the dimensions of the video.
The <audio> Tag
The <audio> tag is used to embed audio files in an HTML document. It also supports multiple attributes for control.

Example usage:

<audio src="audio.mp3" controls></audio>
Attributes for <audio> Tag
src: Specifies the path to the audio file.
controls: Adds audio controls, like play, pause, and volume.
autoplay: Automatically starts playing the audio when the page loads.
loop: Repeats the audio once it ends.
muted: Mutes the audio by default.
preload: Specifies if and how the audio should be loaded when the page loads ('auto', 'metadata', 'none').
 

The "preload" attribute can have the following values:

none: This is the default value. It indicates that the browser should not preload the audio file at all. The audio file will only start downloading when the user initiates playback.

metadata: This value tells the browser to preload only the metadata of the audio file, such as its duration and basic information about the audio. This can be useful if you want to display the audio duration to the user without fully loading the audio data.

auto: This value instructs the browser to preload the entire audio file as much as possible without delaying the loading of other important page content. The browser will try to load the audio file in the background so that it's ready to play when the user decides to start it.
-------------------------------------------------------------------------------------------------------------------
iFrames in HTML
iFrames, or Inline Frames, are an integral part of modern web development. They allow you to embed another HTML page within your current page. In this blog, we'll delve into the utility of iFrames, their attributes, and some use-cases.

What is an iFrame?
An iFrame is an HTML element that enables an inline frame for the embedding of external content. Essentially, you can load another web page within a designated area of your current webpage.

Why Use iFrames?
iFrames offer a variety of use-cases:

Content Isolation: iFrames allow you to isolate third-party content, which can improve security.
Modularity: Easily embed external plugins, widgets, or content.
Resource Separation: Content within an iFrame can load separately from the rest of the page.
Basic Syntax
The basic syntax of an iFrame is quite straightforward:

<iframe src="URL" width="width" height="height"></iframe>
Attributes of iFrame
Several attributes can enhance the functionality of an iFrame:

src: Specifies the URL of the page to embed.
height and width: Define the dimensions.
frameborder: Indicates whether to display a border.
scrolling: Controls the scrollbars.
name: For targeting the iFrame in JavaScript.
Practical Examples
Embedding a YouTube Video
<iframe src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allowfullscreen></iframe>
Embedding Google Maps
<iframe src="https://maps.google.com/maps?q=LOCATION&output=embed" frameborder="0"></iframe>
-------------------------------------------------------------------------------------------------------------
HTML Code Tag
The HTML <code> tag is a powerful element for displaying code snippets within a webpage. It preserves both spaces and line breaks, making it ideal for showcasing code. In this blog post, we'll explore how to use the <code> tag effectively, especially in conjunction with Prism for code highlighting.

What is the <code> Tag?
The <code> tag is a semantic HTML tag that's used for displaying code snippets. It can be used both inline and within a block-level element like <pre>.

Why Use the <code> Tag?
Semantic Meaning: Provides semantic value to the enclosed code.
Readability: This makes it easier for both browsers and developers to understand that the text is code.
Styling: Easier to style and highlight with CSS or JavaScript libraries like Prism.
Basic Usage
The most straightforward way to use the <code> tag is inline for short code snippets:

<code>Your code here</code>
cwh tutorial image

Using <code> with <pre>
For multiline code snippets, it's common to combine the <code> tag with the <pre> tag:

<pre><code>Your multiline code here</code></pre>
===================================================================================================================
Use always semantic tags for better understanding and for SEO also. we are using semantic tags that's only our browser can understand our code easily..so it's a best practice to use semantic tags everytime..
<header>
<footer>
<main>
<aside>
<nav>
<figure>
<article>
<section>
these are the semantic tags of HTML. with the help of these tags we can understand the code better..
------------------------------------------------------------------------------------------------------------------------------
CSS-

CSS is used for styling to style the page content without CSS our page will look like a simple text write on notepad so if we want to add styles in our html page then we need to use the CSS...

Types of CSS-
1- Inline CSS
2- Internal CSS
3- External CSS

Inline - <p style="color: red;"> - this is called inline CSS where we are adding the styles in one line but this is not a best practice because in some case if we want to add styles on 100 h1 then by inline CSS we need to apply style in all 100 h1 so it takes very much time to style the page that's why we are not using the inline CSS...

Internal CSS - 
<style>
h1{
  background-color: yellow;
}
</style> - In internal CSS We are applying the style in our webpage with the help of selectors in style tag it will help to add styles to all the tags at a time...we don;t need to add again and again and one by one.

External CSS - 
In this method we are creating the new file with .css extension then in this file we are adding the styles which is applied to all the tags you want..but there is a catch you need to link the CSS into your HTML page.
<link rel="Stylesheet" href="Style.css">

.css - In the .css file
p{
  color: blue;
}
CSS Selectors:- selectors are nothing but the tags of HTML in which we want to apply the styles.
Element Selector-

div{ //div is the selector 
  color: red; //declearation - color is our property and red is our value.
}
Class Selectors -

.mohit{
  color: blue;
}
Id Selector -

#aman{
  color: blue;
}
Child Selector -

div > p{ //This is a child selector this style will apply only when the paragraph is direct child of the div then only styles applied..
  background-color: black; 
}
Descendant Selector -
div p{ //descendant selector is a selector in which if you want to apply style into the paragrapgh and paragraph is present in the tag inside tag not a direct child of the div then you need to apply descendant selector. this is the method to apply descendant selector you need to give the space between the selector and the tag.
  color: red; 
}
Chaining Selector -
h1.aman{ //In this method you don't need to give the spaces between class and element selector it targets the h1 which class is .aman
  color:green;
}
div p:first-child{ //Use of this is if you have multiple paragraphs in your content then if you want to apply the styles only in the first paragraph then you can use this first-child property.
  color: blue;
}
CSS Specificity - 
Specificity Calculation
To calculate specificity, assign a value to each part of the selector:

Universal Selector: 0
Element selectors and pseudo-elements: 1
Class selectors, attribute selectors, and pseudo-classes: 10
ID selectors: 100
Inline styles: 1000

**agar same selector hai ek hi tag mein like 3 classes to jo sabse baad me aayegi wahi maani jaayegi baaki neglect kar di jaayegi.
**If we applied !important in front of any tag then iski proirity sabse upar hogi and ye inline style ko bhi override kar sakta hai  

CSS Box Model
The CSS Box model defines how elements are rendered and how their dimensions are calculated.

It describes the structure of an element as a rectangular box that has content, padding, a border, and a margin.

The box model consists of four main components, which are

1. Content
The innermost component of the box model is the actual content of the element. It can be text, image, video, etc.
The content area is defined by the width and height properties.
2. Padding
The space between the actual content and the border of the element is the padding.
The padding area is defined by the property padding. For more details, follow the CSS Padding tutorial.
3. Border
The border surrounds the content and padding and gives the visual border of the element.
The border properties can be controlled using the border keyword. For more details, follow the CSS Borders tutorial.
4. Margin
The margin is the space outside the element that separates it from other elements in the layout.
The margin of the element is controlled by the margin property. For more details, follow the CSS Margin tutorial.
 

The CSS Box model can be visually represented as:

cwh tutorial image

Calculating the total dimension of the element
The total width and height of the element is calculated with the formula:

Total Width = Width + Left Padding + Right Padding + Left Border + Right Border + Left Margin + Right Margin

Total Height = Height + Top Padding + Bottom Padding + Top Border + Bottom Border + Top Margin + Bottom Margin

Example:

<head>
    <style>
        p{
            width: 200px;
            height: 300px;
            padding: 15px;
            border: 10px solid red;
            margin: 5px;
        }
    </style>
</head>
<body>
    <p>CodeWithHarry</p>
</body>
</html>
Here, the total height and width will be represented as

Total Width = 200px (width) + 15px (left padding) + 15px (right padding) + 10px (left border) + 10px (right border) + 5px (left margin) + 5px (right margin) = 260px.

Total Height = 300px (Height) + 15px (Top Padding) + 15px (Bottom Padding) + 10px (Top Border) + 10px (Bottom Border) + 5px (Top Margin) + 5px (Bottom Margin) = 360px

 

Playaround:
To view the dimension of any element follow the steps or video:

Right-click and click on Inspect.
Click on the arrow key in the top left corner.
Select the element
Unhide the computed styles sidebar.
Toggle the properties.
Here's a Quick Video Explaining the playaround:
--------------------------------------------------------------------------------------------------------------------
when we write padding:20px; -> that means 20px top , 20px right , 20px bottom , 20px left 
so this is clockwise direction..
-------------------------------------------------------
fonts Properties:-
font-size; //It is used to define the size of the font
font-weight; //It is used to bold the font - set the range as per your need.
font-style; //like italic,normal etc these are font-style
font-family; //It is used to style the fonts like sans-serif, poppins etc.
line-height; //It is used to give the spaces between the lines of the paragraph.
letter-spacing-//It is used to give the spaces between the letters of the word.

text Properties:-
text-transform: Uppercase/Lowercase ; //It is used to change the case of the text.
text-decorartion: none; //Removes the line in the bottom of the text
text-decoration-color: red; //It is used to change the colour of the line which is present in the bottom of the text.
text-decoration-thickness: 50px; //It is used to increase the thickness of the bottom line of the text.
text-indent:40px; //It gives the space in the left side and shift the whole text in the right.So you want to shift the text from left to right side of the web page then you need to use this property.
overflow:hidden; //It is used to hide the overflow text from the paragraph.
text-overflow: ellipses; //It is used to style the overflow text when you use ellipses then it shows dotted in the end of the overflow text and when you use clip then you will see the overflow text is hidden.
----------------------------------------------------------------------------------------------------------------
CSS Colors
Let's Learn about colors in CSS

    CSS Colors can be represented in these types:

    1 -  Color Keywords
    2 -  HEX Color Codes
    3 -  RGB
    4 -  RGBA
    5 -  HSL
---------------------------------------------------------------------------------------------------------------------
:nth-child(1){ //This is the nth child property where we can target the nth child of their parent.
       
}     
-> div p:nth-child(1){
  this property targeting the first child of their div means style the first paragraph of the div.
}
CSS Units -
vw- viewport width -//It takes the width of your viewport
vh- viewport height -//It takes the height of your viewport
px- pixel 
em - 1.5em - means it inherits the font-size of the parent element 
for example- if you are setting 20px size of the parent font-size and setting the font-size of the child is 1.5em then it inherits the font-size of the parent = 20*1.5 =30px so the font-size of the child will be 30px.
rem - In CSS, rem stands for "root em." Unlike the em unit, which is relative to the font size of the current element, the rem unit is relative to the font size of the root element (usually the <html> element).
for example - html - font-size is 16 and you sets the font-size of para to 1rem it means it inherits the root element and the size will be - 16px..

it will not effect the font-size of the em part when you are applying the rem.
However, if you directly set the font-size of the parent element where em units are used, it will override the inherited font size from the <html> element. In this case, the em units will be calculated based on the font size of the parent element, not the root <html> element.

min-height: 40vh; //when you are setting the min-height then iski minimum height jo hai wo 40 viewport hi rahegi but max kitni bhi badh jaayegi jitna content hoga uske hisaab se adjust kr legi..
---------------------------------------------------------------------------------------------------------------------
when you are transfrorm the block level element to the inline element then it does not support the padding and margin on the top then, we need to always transform the element to the inline-block element....then the div able to take the padding on the top and margin also.
---------------------------------------------------------------------------------------------------------------
CSS Shadows:- 
--------------
Box Shadows
box-shadow is a popular CSS property that enables designers to add shadow effects around an element's frame. It can be used to give any element, be it a div, image, or button, a 3D feel or to emphasize on hover.

box-shadow: h-offset v-offset blur spread color inset;
h-offset and v-offset: Determines the shadow's horizontal and vertical position.
blur: The larger the value, the blurrier the shadow.
spread: Expands or shrinks the shadow size.
color: Defines the shadow color.
inset: Makes the shadow inner.
Here is an example:

.div-element { box-shadow: 5px 5px 15px 5px #888888; }
Text Shadows
text-shadow is utilized to give shadows specifically to the text. It can elevate the readability of the text or give it an elegant appearance.

 

The Syntax for Text-Shadows is as follows:

text-shadow: h-offset v-offset blur color;
Here is an example:

.text-element { text-shadow: 2px 2px 4px #888888; }
Outlines
An outline is a line that is drawn around elements, outside the borders, to make the element "stand out". It's commonly used for accessibility purposes, like highlighting focused elements.

The Syntax for Outlines is as follows:

outline: width style color;
width: Sets the outline width.
style: Determines the style of the outline such as solid, dotted, or dashed.
color: Sets the outline color.
Here is an example:

.button-element:focus { outline: 2px solid blue; }
Differences between Outlines and Borders:
While both can visually appear similar, outlines differ from borders in a few ways:

Position: Outlines don't take up space; they're drawn around the element, outside of any border.
Offset: Using the outline-offset property, you can set the space between an outline and the edge or border of an element.
Width: Borders can have varying widths on different sides, outlines have a uniform width.
Rounded Corners: Borders can have rounded corners using border-radius, while outlines generally cannot.
---------------------------------------------------------------------------------------------------------------------------
CSS Positioning
The CSS positions allow you to precisely control the placement of an element on the web page.

It helps to determine how elements are placed inside the container element and how they interact with the other elements on the page.

There are various types of position property values, such as:

Static(Default)
The elements are positioned according to the normal flow of the document.

Syntax:

selector {
      position: static;
}
 Example:

<head>
    <style>
        img {
            position: static;
        }
    </style>
</head>
<body>
    <p id="p1">Lorem ipsum dolor sit amet.</p>
    <p id="p2">Lorem ipsum dolor sit amet.</p>
    <img src="./logo.png" alt="logo">
    <p id="p3">Lorem ipsum dolor sit amet.</p>
    <p id="p4">Lorem ipsum dolor sit amet.</p>
</body>
</html>
cwh tutorial image

Relative
Elements are positioned relative to the normal position in the document.

You can use the top, right, bottom, and left properties to move the element from its original position.

Syntax:

selector {
      position: relative;
}
Example:

<head>
    <style>
        img {
            position: relative;
            left: 100px;
            top: 50px
        }
    </style>
</head>

<body>
    <p id="p1">Lorem ipsum dolor sit amet.</p>
    <p id="p2">Lorem ipsum dolor sit amet.</p>
    <img src="./logo.png" alt="logo">
    <p id="p3">Lorem ipsum dolor sit amet.</p>
    <p id="p4">Lorem ipsum dolor sit amet.</p>
</body>
</html>
cwh tutorial image

Here you can see that the image is repositioned from its original place, and the gap is not filled by another element.

Absolute
Elements are positioned relative to the closest positioned ancestor (parent), which means we need to have a parent element with a positioning other than 'static'.

Note: An absolutely positioned element is removed from the normal flow.

Example:

<head>
    <style>
        #about{
            position: relative;
        }
        .logo{
            position: absolute;
            right: 10px;
            top: 10px;
        }
    </style>
</head>
<body>
    <h1>CodeWithHarry</h1>
    <div class="about">
        <p>Developer</p>
        <p>founder of CodeWithHarry</p>
        <img class="logo" src="./logo.png" alt="logo">
    </div>
</body>
</html>
cwh tutorial image

Explanation:

cwh tutorial image

Here, as we have set position relative to the body and absolute to the about section, the about section position can be manipulated with the left of top, left, right, and bottom.

Fixed
Elements are positioned relative to the viewport (screen) and do not move when the page is scrolled.

This is useful for creating elements like fixed headers or footers.

Example:

<head>
    <style>
        h1{
            position: fixed;
            top: 10px;
            right: 20px;
        }
    </style>
</head>
<body>
    <h1>CodeWithHarry</h1>
</body>
</html>

Here, the image position will be fixed.

Float
The float property is used to shift an element to the left or right within its containing element. For more details, follow CSS Float.

Sticky
Position sticky is a hybrid between 'relative' and 'fixed'.

It allows an element to become "stuck" to the top or bottom of its container when scrolling, but it behaves like relative positioning within the container until it reaches a specified offset.

Example:

<head>
    <style>
        h1{
            position: sticky;
            top: 10px;
            right: 20px;
        }
    </style>
</head>
<body>
    <h1>CodeWithHarry</h1>
</body>
</html>
------------------------------------------------------------------------------------------------------------------
We can target multiple list items by using nth-child property -
for example :- <li>Home </li>
for example :- <li>About </li>
for example :- <li>Contact </li>
here we have multiple li so if we want to target the second li then we use li:nth-child(2){}
for 3rd li we use li:nth-child(3){} and so on.
------------------------------------------------------------------------------------------------------------------
Media queries Breakpoints - mobile - 480 max 
tablet - 481-1200 max
laptop - 1201-1600 max 
desktop - 1600 and more
------------------------------------------------------
float and clear- 
float: right;
float: left; 
these two properties helps to float the image either left or right.
clear: right;
clear: left;
these two properties helps to clear all the text from left or right and move the content downword..
-------------------------------------------------------------------------------------------------------------------------------
Seudo Properties-
.boxes::before{
  content: "My Name is Mohit Pratap Singh";
  color:red;
}
--------------------------------------------------------------------------------------------------------------------------------
CSS FlexBox
FlexBox aka Flexible Box Layout makes it easier to layout, align and style items in the container while maintaining the responsiveness of the website.

 

To create a flexbox you need to set the display of the container as flex

Eg: {display: flex;}

 

This element is called the flex container, and stores the sub-elements which are known as flex items

 

Flex Container Properties
The flex container properties are:

1. Flex Direction
It defines in which direction the flex elements would be displayed. It takes values like row, column or “reverse” too.

 

Eg:



 

Output:



2. Flex Wrap
By using this property we can make our elements responsive for different screen sizes. 

 

Eg:

.flex-container {
            display: flex;
            flex-direction: row;
            background-color: yellowgreen;
            flex-wrap: wrap;
        }
 

Output:



You can use flex flow as a short to add both these properties. Eg: {flex-flow: row wrap;}

 

3. Justify Content
This property is used to set the position of content or rather align content along the main axis.

Eg:

.flex-container {
            display: flex;
            flex-direction: row;
            background-color: yellowgreen;
            justify-content: center;
        }
 

Output:



It can take other values too like “space-around” which distributes flex items equally spaced in the container. Other properties include flex-end, flex-start, space-between, etc. (These could be seen in vs code when the justify-content property is selected).

 

4. Align Items
Just like the justify-content property, align-items define the alignment of the flex container but along the cross-axis.

 

Eg:

.flex-container {
            display: flex;
            height: 200px;
            flex-direction: row;
            background-color: yellowgreen;
            align-items: center;
        }
 

Output:



5. Align Content
This property is very similar to align item but here rather than the flex items, the content present in the item is selected for the property.

 

Eg:

.flex-container {
            display: flex;
            height: 200px;
            flex-direction: row;
            background-color: yellowgreen;
            align-content: center;
        }
 

Output:



Flex Items Properties
The flex item properties are:

1. Order:
As the name suggests, this property sets the order in which the flex items are shown.

 

Eg:

<div style="order: 4;">1</div>
<div style="order: 3;">2</div>
<div style="order: 1;">3</div>
<div style="order: 5;">4</div>
<div style="order: 2;">5</div>
 

Output:



2. Flex Grow & Shrink
Decides the relative size of flex items. By default, this property is zero and thus items have the same size.

 

Eg:

<div>1</div>
<div>2</div>
<div style="flex-grow: 3;">3</div>
<div>4</div>
<div>5</div>
 

Output:



We can also use flex-shrink to decrease size of an element.

3. Align Self
This property allows default alignment to be overridden for the individual flex items. Try adding inline CSS to see how this property is used.
-------------------------------------------------------------------------------------------------------------------------------
The display: flex; property is used to create a flex container, which allows its direct children (flex items) to become flexible and participate in flex layout. By default, the flex container's direction is set to row, which means its flex items are arranged horizontally along the main axis. So, display: flex; indeed enables flex layout and defaults to arranging items horizontally.

Properties of the Parent (Flex Container):

display: Defines the element as a flex container.
flex-direction: Defines the direction of the flex container's main axis (row, row-reverse, column, column-reverse).
flex-wrap: Defines whether the flex items are forced onto a single line or can be wrapped onto multiple lines (nowrap, wrap, wrap-reverse).
flex-flow: A shorthand property for setting both flex-direction and flex-wrap
justify-content: Defines how the browser distributes space between and around content items along the main axis of the flex container (flex-start, flex-end, center, space-between, space-around, space-evenly).
align-items:  Defines how the browser aligns flex items along the cross axis of the flex container (stretch, flex-start, flex-end, center, baseline).
align-content: Defines how the browser aligns flex lines (flex container's cross-axis) when there is extra space in the flex container (stretch, flex-start, flex-end, center, space-between, space-around).

Properties of the Child (Flex Item):

order: Defines the order of the flex items within their flex container.
flex-grow: Specifies how much the flex item will grow relative to the rest of the flex items in the flex container.
flex-shrink: Specifies how much the flex item will shrink relative to the rest of the flex items in the flex container.
flex-basis: Specifies the initial size of the flex item before it's placed in a flex container.
flex: A shorthand property for setting flex-grow, flex-shrink, and flex-basis
align-self: Allows the default alignment to be overridden for individual flex items.
gap: 20px; It is used to give the gap between the boxes or elements

These properties allow you to control the layout and behavior of flex containers and their child elements, giving you fine-grained control over the arrangement and sizing of content in a flexible and responsive manner.
=================================================================================================================================

CSS Transitions:- 
It means move anything from one state to another state in slow motion very smoothly.

1- Translate Property:

The translate function is one of the transformation functions used with the transform property.
It specifically moves an element along the horizontal and/or vertical axes.
The translate function takes one or two values: translateX() for horizontal movement and translateY() for vertical movement. You can also use translate() for combined horizontal and vertical movement.

-----------------------------------------------------------
Bootstrap:- 

Bootstrap is a CSS Framework created by 2010 by two developers of twitter mark otto and jacob.
It contains pre made CSS Files which you can simply include into your project and in order to use their pre-built components and styling.
One of the biggest reason why bootstrap took off because of his 12-column layout system build on the top of flexbox.
So the main of the bootstrap is to create responsive websites but mobile first approach.

How to use bootstrap?

Include Via CDN(Content Delivery Network) 
link for HTML and CSS Styling - <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
link for provide functionality - <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM" crossorigin="anonymous"></script>
these are the two links which you can add into your web page for fast styling and quickly provide the designing to your website..
---------------------------------------------------------------------------------------------------------------------------------
Bootstrap Breakpoints for different different screen sizes:- 
small - sm - >=576px - mobile
medium - md - >=768px - ipad/tablet
large - lg - >=992px - Laptop
Extra large - xl - >=1200px - Desktop
Extra extra large - xxl - >=1400px - TV etc.

Bootstrap 5 Grid System:-

Bootstrap's grid system is built with flexbox and allows up to 12 columns across the page.

If you do not want to use all 12 columns individually, you can group the columns together to create wider columns:
The grid system is responsive, and the columns will re-arrange automatically depending on the screen size.

Make sure that the sum adds up to 12 or fewer (it is not required that you use all 12 available columns).

Grid Classes:-

The Bootstrap 5 grid system has six classes:

.col- (extra small devices - screen width less than 576px)
.col-sm- (small devices - screen width equal to or greater than 576px)
.col-md- (medium devices - screen width equal to or greater than 768px)
.col-lg- (large devices - screen width equal to or greater than 992px)
.col-xl- (xlarge devices - screen width equal to or greater than 1200px)
.col-xxl- (xxlarge devices - screen width equal to or greater than 1400px)
The classes above can be combined to create more dynamic and flexible layouts.

Tip: Each class scales up, so if you want to set the same widths for sm and md, you only need to specify sm.

Basic Structure of a Bootstrap 5 Grid:-

The following is a basic structure of a Bootstrap 5 grid:

<!-- Control the column width, and how they should appear on different devices -->
<div class="row">
  <div class="col-*-*"></div>
  <div class="col-*-*"></div>
</div>
<div class="row">
  <div class="col-*-*"></div>
  <div class="col-*-*"></div>
  <div class="col-*-*"></div>
</div>

<!-- Or let Bootstrap automatically handle the layout -->
<div class="row">
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
</div>
First example: create a row (<div class="row">). Then, add the desired number of columns (tags with appropriate .col-*-* classes). The first star (*) represents the responsiveness: sm, md, lg, xl or xxl, while the second star represents a number, which should add up to 12 for each row.

Second example: instead of adding a number to each col, let bootstrap handle the layout, to create equal width columns: two "col" elements = 50% width to each col, while three cols = 33.33% width to each col. Four cols = 25% width, etc. You can also use .col-sm|md|lg|xl|xxl to make the columns responsive.

Below we have collected some examples of basic Bootstrap 5 grid layouts.

Three Equal Columns
.col
.col
.col
The following example shows how to create three equal-width columns, on all devices and screen widths:

Example
<div class="row">
  <div class="col">.col</div>
  <div class="col">.col</div>
  <div class="col">.col</div>
</div>
Responsive Columns
.col-sm-3
.col-sm-3
.col-sm-3
.col-sm-3
The following example shows how to create four equal-width columns starting at tablets and scaling to extra large desktops. On mobile phones or screens that are less than 576px wide, the columns will automatically stack on top of each other:

Example
<div class="row">
  <div class="col-sm-3">.col-sm-3</div>
  <div class="col-sm-3">.col-sm-3</div>
  <div class="col-sm-3">.col-sm-3</div>
  <div class="col-sm-3">.col-sm-3</div>
</div>
Two Unequal Responsive Columns
.col-sm-4
.col-sm-8
The following example shows how to get two various-width columns starting at tablets and scaling to large extra desktops:

Example
<div class="row">
  <div class="col-sm-4">.col-sm-4</div>
  <div class="col-sm-8">.col-sm-8</div>
</div>
=================================================================================================================================
Now we are Develop new Project which is our Netflix Clone project and which is responsive also working on any screen sizes.

