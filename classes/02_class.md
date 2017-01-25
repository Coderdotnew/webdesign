# CSS Syntax
* Unlike HTML, CSS does *not* use brackets to define code. Since there is not any plain text in a CSS file, we do not need to separate plain text and code.
* CSS is split up into 3 simple components:
  * selector { property: value } 
  * **selector** is what HTML element you want to style
  * **property** defines what aspect of the selector you want to change
  * **value** is what you are styling
* For example, 
```css
p { color: blue }
```
* We are matching up the selector, *p*, with the tag, *<p>* (paragraph).
  * This means that every paragraph tag will be styled with a blue colored font.

# Linking to HTML
* Because we are creating a separate file for CSS, we need to create a link between this and the HTML file. 
  * This link lets the browser know to use the CSS file in conjunction with the HTML.
  * We put this link in the <head> tag in the HTML document. Putting it inside this tag lets the browser read over it while making it not visible to the viewers.
```html
<link rel="stylesheet" href="style.css">
```
* "style.css" is generally what CSS documents are named, though it can be anything as long as you link it correctly in the document.
* As soon as the CSS file is linked, you will be able to start styling and making your HTML look pretty!

# Basic CSS Attribute Examples
-----
#### Font Size
```css
p { font-size: 15px }
```
* Font size is generally styled using pixels. There are other measurements that can be used for sizing, which we will go over later.
* You know when you zoom into a picture so much it becomes a whole bunch of squares? Each one of those squares is considered a pixel. This is the smallest piece of an image that your computer is able to display.
* The smaller number of  pixels you set, the smaller the font will be.

#### Font Color
```css
p { color: blue }
```
*  Color can be set by either using the name of a color, or by using a *hex code*.
*  Hex (hexadecimal) codes are defined by a # followed by a six digit sequence that represents a certain color.
*  http://htmlcolorcodes.com/ is a great resource to find hex codes!

#### Font Family
```css
p { font-family: Arial }
```
*  Just like in Microsoft Word, you can choose what font you want by using it's font-family name.
*  NOTE: If a font name has spaces in it, (i.e. Times New Roman) it must be contained within quotation marks - "Times New Roman"


# Inheritence
* Inheritence is EXTREMELY important when dealing with CSS, but first off, we need to talk about nesting.
* Nesting in HTML is when there is a tag inside of a tag. It looks like this: 
```html
<body><h1>Hello</h1></body>
```
* This basically means that the h1 tag will "inherit" any style that is on the body tag.
  * For example, if the body tag has a blue font color, it will be applied to every tag inside of it, which in this case is h1.
* It can become MUCH more complex as well. 
* Nested elements must be set inside of one another. The code snippet above is the correct way to place the tags. This is incorrect:
```html
<body><h1>Hello</body></h1>
```
# The Box Model
* Elements of HTML are represented as invisible recatngular boxes. This helps us figure out the dimensions and size of an element.
* There are multiple layers of this box---content, padding, border, and margin.
   * Content contains whatever information is inside this specific element. For example, in the code, <h1>Hello</h1>, "Hello" is the content.
   * Padding is the space between the content and the border of the box. Using CSS we are able to make this space as big or as small as we like. The same goes for margins, though they are on the outside of the border. A margin is the space between different elements.
----------
Now that we have some CSS basics now, we can start adding onto the code we started from last class.
```html
<!DOCTYPE html>
<head>
	<title>Personal Website</title>
</head>
<body>
	<h1>Title here</h1>
	<p>"Tagline or quote here."</p>
	<button>Learn more..</button>
</body>
</html>
```
In a separate file we can start styling some of the elements in this document.
* Lets start with the font. The font is going to be styled within the *body* element. This means that every tag inside the body (which should be all of them!) will be affected by this change.
* NOTE: The different spacing in the code seen below makes it easier to read CSS, especially when we start styling different properties within the selector.   
```css
body { 
    font-family: sans-serif;
}
```
* Also within the body selector, we are going to insert a background image. To do this, we must find a high resolution image so it will not look pixelated when it is stretched across the screen.
* Because we are using an image URL instead of a color name we need to insert this URL in between parenthesis and quotes like so.
```css
body { 
    font-family: sans-serif;
    background: url("http://images.summitpost.org/original/272289.jpg");
}
```
* NOTE: semi-colons MUST be used at the end of a line of CSS in order for the browser to distinguish new lines within the code. If your code is not working, check the semi-colons as this is a very common mistake.
* You may notice the background looks a bit funky and is not centered correctly on the page. To fix this, enter the following code to the end of the background line. This just ensures that the background will cover the entire page while centering the image and not repeat.
* We need to enter additional code (bottom four lines) in order to make the background cover the whole screen, because different browsers will read the code slightly differnt.
```css
body { 
    font-family: sans-serif;
    background: url("http://images.summitpost.org/original/272289.jpg") no-repeat center center fixed;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
}
```
* Next, we will start styling our title, h1 selector.
* First off, let's change the font color to white. We can either use the word "white," or we can use the hex code, #FFFFFF.
* Let's also change the size of the font so that it will stand out on the page since it is the header, 50px will be a good size. 
* NOTE: we are not putting this in the body selector because we do not want to apply this font size and color to every element containing text! We only want to apply this change to the h1 selector.
```css
body { 
    font-family: sans-serif;
    background: url("http://images.summitpost.org/original/272289.jpg") no-repeat center center fixed;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
}

h1 {
    color: white;
    font-size: 50px;
}
```
* Now we will do the same thing to the p selector, though making it a smaller font size.
```css
body { 
    font-family: sans-serif;
    background: url("http://images.summitpost.org/original/272289.jpg") no-repeat center center fixed;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
}

h1 {
    color: white;
    font-size: 50px;
}

p {
    color: white;
    font-size: 30px;
}
```
* Styling the button will use some logic from the box model. We are going to add a border and create some padding space within the button, in addition to changing the font size and color.
* In order for the button to just have a border and no background, the background property's value can be set to "transparent."
* The new property, border, has 3 values, which are separated by a space.
  * Thickness, what type of line (solid, dashed, dotted), and color.
* It is also possible to style different sides of the box separately. For example, we will be changing the padding to be greater on the sides than on top and bottom. To do this we will change the value of the padding to individually change each side: "padding: top right bottom left;" in which the sides will be replaced by pixels.
```css
body { 
    font-family: sans-serif;
    background: url("http://images.summitpost.org/original/272289.jpg") no-repeat center center fixed;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
}

h1 {
    color: white;
    font-size: 50px;
}

p {
    color: white;
    font-size: 30px;
}

button {
    background: transparent;
    border: 1px solid white;
    color: white;
    padding: 20px 60px 20px 60px;
}
```
* To finish this basic webpage, we want to center this text. In order to do this we must use the text-align property in the body selector to change the position of all the text on the page. The value of this property will be set to "center."
```css
body { 
    font-family: sans-serif;
    background: url("http://images.summitpost.org/original/272289.jpg") no-repeat center center fixed;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
    text-align: center;
}

h1 {
    color: white;
    font-size: 50px;
}

p {
    color: white;
    font-size: 30px;
}

button {
    background: transparent;
    border: 1px solid white;
    color: white;
    padding: 20px 60px 20px 60px;
}
```