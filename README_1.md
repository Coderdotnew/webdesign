# What is HTML?
* HTML stands for *Hypertext Markup Language*. Every page you see on the web is built with HTML. 
* You view webpages *in a browser*. You have one open right now as you are reading this text!
  * A browser is an application on your computer that lets you view webpages on the internet.
  * Google Chrome, Safari, Firefox, and Internet Explorer are a few examples of web browsers.
* HTML is made up of tags that structure the content on the page, which essentially alters the look and/or content.
* This basically acts as the "skeleton" of a website--it holds everything together.
* HTML is interpreted by your browser where the code is translated to form a webpage.

![alt text](https://media.giphy.com/media/89bq55CYqPQDS/giphy.gif)

# What is CSS?
* CSS stands for *Cascading Style Sheets*.
* This gives a style and format to your HTML, pretty much just making it look pretty.
* It can help define certain aspects of HTML such as font, background, positioning, sizing, spacing, and other visual information. CSS basically takes in that aspect of HTML and allows you to change the way it is presented on the webpage.
* Though HTML allows you to change some of these items, CSS will allow you to get more detailed to create a more visually appealing and organized website.



# HTML Syntax
* Just like normal text, HTML reads top to bottom, left to right.
* HTML uses *tags* for the browser to distinguish between plain text and your code.
* Tags are used to describe certain elements that are going to be edited, like headers and links for example.
* They are enclosed in angle-brackets (<, >). Without these, the tag will just be interpreted as text, and will be printed on your webpage. 
* Tags *almost* always end with a closing tag, which is just including a foward slash inside a tag as seen below. (There are a couple exceptions!)
* The text you are editing will be placed inside of the opening and closing tag.
```html
<p>This is a paragraph!</p>
```
* As you can see, the tag in this example is "p" which is the tag for paragraph. This also includes a closing tag. Without the closing tag, this element would be applied to all of the subsequent text/code. (We will get more into this concept later)

# Page Structure
* Three tags essentially make up and hold everything in an HTML page--head, html, and body. ALL code goes inside the html tag. (Which lets the browser know what language we are coding in!)
* Below is an example of the VERY basic HTML structure, what you start out with every time you build a page.
* Note: "!DOCTYPE html" is just a declaration for the browser to read the document as HTML, and not any other language.
```html
<DOCTYPE! html>
<head></head>
<body></body>
</html>
```

![alt text](https://media.giphy.com/media/l41m04gr7tRet7Uas/giphy.gif)

<head>
* This is where you put all of the information that does not appear on the page itself (i.e. metadata, which describes the webpage and let search engines find your page, the page title, etc.)
* Adding a title for the page is simple, just use <title></title>. This will be displayed at the top of your browser, usually in the tab.
* Think of the head as your brain; it contains information about language it speaks (HTML), what it calls itself (<title>), any realtives it has (links to other sheets CSS, JS).
```html
<DOCTYPE! html>
<head>
    <title>Personal Website</title>
</head>
<body></body>
</html>
```
* This is also where you link other pages of code (like CSS) to the HTML document, which we will learn in the next lesson.
* Now that we have the basic structure for our page, we can start adding some text!

<body>
* Everything that you put in the body will appear on the page. 
* Plain text that is not enclosed in tags will be shown as the browser's default font.
* Lets start out with a header...

<h1>
* Header tags are used for titles/headings, pretty much any text you want to be large.
* There are different sizes of header tags (h1, h2, h3, h4, h5, h6) with h1 being largest and h6 being smallest.
* Here we are adding an h1 header to the body of our page:
```html
<!DOCTYPE html>
<head>
    <title>Personal Website</title>
</head> 
<body>
    <h1>Title here</h1>
</body>
</html>
```

<p>
* As mentioned before, p is the paragraph tag, used for smaller font in addition to long chunks of text.
* To add a tagline under our header, we're going to use this tag.
* Using these tags to separate different content will help organize the body while also making it easier to style when we get into CSS.
```html
<!DOCTYPE html>
<head>
	<title>Personal Website</title>
</head>
<body>
	<h1>Title here</h1>
	<p>"Tagline or quote here."</p>
</body>
</html>
```

<button>
* This tag is pretty self-explanitory; it adds a basic button to your page.
* We will learn more about creating links with buttons in later lessons.
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

# HTML Cheat Sheet
Tag | Example
--- | --- 
<!DOCTYPE html> | Defines document language as HTML
<p> | Paragraph
<h1>...<h6> | Headers, biggest=1, smallest=6
<a href="link"> | Makes text clickable
<img src="image"> | Displays an image on webpage
<br> | Creates a space between text (like pressing enter)
<hr> | Similar to  <br>, but inserts a horizontal line







# Resources
http://www.w3schools.com/tags/
* This is a great source to find a more extensive and complete list of tags and a lot of other helpful info on HTML, CSS, and many other languages!
