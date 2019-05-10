# Development Guidelines
Swiss Realty's development guidelines focus at providing developers both in-house and in the community a clear framework to write code for this project. Swiss Realty commits to provide accessible and readable code to facilitate cross-team work and collaboration, as such every developer working on this project need to follow the guidelines defined in the documents listed below.

## General considerations
Some considerations go accross programming language and should be followed accordingly.

### Tab size is of 4 📑

``` javascript
// correct indentation
function sumVars(var1, var2) {
    var var3 = null;
    var3 = var1 + var2;
    return var3;
}
```
``` javascript
// wrong indentation
function sumVars(var1, var2) {
  var var3 = null;
  var3 = var1 + var2;
  return var3;
}
```
This is a mandatory rule, all code written with two space tabs will be asked to be changed.

### IDs and labels should be as verbal as possible 🗣
```javascript
// correct labelling
var surName = "Doe";
var name = "John";

var completeName = name.concat(' ', surName);
```
```javascript
// wrong labelling
var a = "Doe";
var b = "John";

var x = b.concat(' ', b);
```
Exceptions can be made for functions that abstract values and purpose to a level for which understanding of the variable/function purpose or value is not needed.

### Spacing is important 🚀
Although spacing is open for interpretation Swiss Realty has defined the following guidelines for readability purposes:
```html
<!-- correct spacing -->
<body>
	<div class="container">

		<div class="row">
		</div>

		<div class="row">
		</div>

	<div>
</body>
```
```html
<!-- wrong spacing -->
<body>
	<div class="container">
		<div class="row">
		</div>
		<div class="row">
		</div>
	<div>
</body>
```

### Comment, comment, comment 📝
Comments are essential for several different reasons:
	* They provide an immense source of information on purpose of certain functions
	* They provide context as to how a certain action is being performed (your way is not the only way)
	* They are helpful to debug and reas through the code in a highlevel manner
```typescript
// recommended commenting behavior

// function that will return a string of character provided by the user
public function returnValue(value: string) {

	// create local variable to hold the value
	let valueHolder = value

	// log the value for debugging purposes
	console.log(valueHolder)

	// return the value
	return valueHolder
}
```
```typescript
// wrong commenting behavior

public function returnValue(value: string) {
	let valueHolder = value
	console.log(valueHolder)
	return valueHolder
}
```

## Syntax specific guidelines
The syntax specific guidelines are completed as we run into use cases and specificities that we would like to see applied in the code.

 ### HTML
HTML Style Rules

  1 HTML Document Type

    Utilize HTML5.

    HTML5 is preferred for all HTML documents: <!DOCTYPE html>.

    (It’s recommended to use HTML, as text/html. Do not use XHTML. XHTML, as application/xhtml+xml, lacks both browser and infrastructure support and offers less room for optimization than HTML.)

    Do not close void elements, i.e. write <br>, not <br />.

2 HTML Validity

    Please use valid HTML where possible.

    Use valid HTML code unless it is not possible to do so due to file size/performance goals.

    Using valid HTML is a measurable baseline attribute that contributes to keep learning about the proper usage, constraints and requirements of HTML

```typescript
//  Wrong validity/documenting example

<title>Test</title>
<p>This is only a test.
```  
```typescript
// Correct validity/documenting behavior
<!DOCTYPE html>
<html lang="zxx">
<title>Test</title>
<p>This is only a test.</p>
```
3 Semantics

    Use HTML according to its purpose.

    Use elements apropiately and for the purpose they've been given. For example, use heading elements for headings, p elements for paragraphs, div elements for division, etc.

    Using HTML according to its purpose is important for accessibility, readability, and code efficiency reasons.

```typescript
// Wrong Semantics example
<div onclick="goToApp();">Access the Web Application</div>
```
```typescript
// Correct Semantics example
<a href="https://mvp-realty-207409.appspot.com/">Start Investing Today!</a>
```
4 Multimedia Fallback/Alternative

    Provide fallback content in case of multimedia crash.

    For failed multimedia, such as images, videos, animated objects via canvas, make sure to offer alternative access. For images that means use of meaningful alternative text (alt) and for video and audio transcripts and captions, if available.

    Providing alternative contents is important for accessibility and user interaction reasons: A blind user has few cues to tell what an image is about without @alt element, and other users may have no way of understanding what video or audio contents are about either.

    For multimedia in which the element @alt would cause redundancy or lack of usefulness, and/or for images used for solely decorative purposes which CSS cannot immediately find use for, please leave the alternative text blank i.e. alt="".

```typescript
// Wrong Multimedia Fallback/Alternative example
<img src="assets/img/logo.png"/>
    ```
```typescript
// Correct Multimedia Fallback/Alternative example
<img src="assets/img/logo.png" alt="logo"/>
        ```
5 Separation of Functionality

    Separation of structure from behavior from design is key.

    Keep the interaction between structure (markup), design (stylying) and behavior(scripting) to a minimum to prevent confusion.

    Meaning that documents and/or templates should only contain HTML for structural reasons, therefore moving anything behavioral into scripts and presentational into style sheets.

    Furthermore it is important to keep the contact area as small as possible to avoid confusion and promote clean understandable code.

    The separation of such is key for maintenance as it is harder to alter HTML documents than it is style sheets or scripts.

```typescript
    // Wrong Separation of Functionality example
    <!DOCTYPE html>
<title>Swiss Realty</title>
<link rel="stylesheet" href="base.css" media="screen">
<link rel="stylesheet" href="grid.css" media="screen">
<link rel="stylesheet" href="print.css" media="print">
<h1 style="font-size: 1em;">Contact information</h1>
<p>To contact for career opportunities please email:
  <u>*****@swissrealty.com</u>
<center>Looking forward hearing from you and why you want to join!!</center>
```

```typescript
            // Correct Separation of Functionality example
<!DOCTYPE html>
<title>Swiss Realty</title>
<link rel="stylesheet" href="default.css">
<h1>My first CSS-only redesign</h1>
<p>To contact for career opportunities please email: >*****@swissrealty.com</p>
<p>Looking forward hearing from you and why you want to join!!</p>
```

6 Entity References

    Please refrain from using entity references.

    There is no need to use entity references like &mdash (long dash);, &rdquo(right double quotes);, or &#x263a(White smiley face);, assuming the same encoding (UTF-8) is used for files and editors among the team.

    There are Exceptions however like the characters < and & which have specific meaning within the HTML language. Same applies to 'invisible' characters such as no-break spaces.

```typescript
    // Wrong Entity references example
    <p>The currency symbol for the Euro is &ldquo;&eur;&rdquo;.</p>
```
```typescript
    // Correct Entity references example
    <p>The currency symbol for the Euro is “€”.</p>
```

7 'type' Attributes

    Please do not include 'type' attribute for stylesheets and scripts unless not using CSS, for stylesheets, and javascript, for scripts.

    Specifying type attributes is not necessary as HTML5 implies that type/CSS and type/javascript are already defaults.

```typescript
    //Wrong 'type' attribute example CSS
<link rel="stylesheet" href="C:\Documents\GitHub\clean-code\website\css\style.css"
    type="text/css">
```

```typescript
    //Correct 'type' attribute example CSS
<link rel="stylesheet" href="C:\Documents\GitHub\clean-code\website\css\style.css">

```
```typescript
    //Wrong 'type' attribute example javascript
<script src="C:\Documents\GitHub\clean-code\website\js\theme.js"
        type="text/javascript"></script>
```
```typescript
    //Correct 'type' attribute example javascript
<script src="C:\Documents\GitHub\clean-code\website\js\theme.js">

```
HTML Formatting Guidelines

1 General Formatting

    Use a new line for every block, list, or table element, and indent every such element.

    Independent of the styling of an element (as CSS allows elements to assume a different role per display property), put every block, list, or table element on a new line.

    Also, indent them if they are child elements of a block, list, or table element.

```typescript
<section class="hero-area" id="home">
  <div class="container">
    <div class="row">
      <div class="col-lg-7"> <!-- stops text taking whole screen -->
        <div class="hero-area-content">
          <h1>Investors & Partners</h1> <!-- hero area title -->
          <p>Swiss Realty is here to revolutionize the way people invest in Real Estate accross the world. By using the power of new technologies, we are able to open a stable and profitable market to a broader audience than ever before.</p>
        </div>
      </div>
    </div>
  </div>
</section>
```
```typescript
<ul>
  <li>Mikael Gross
  <li>Antony Chamieh
  <li>Noortje van Ophem
</ul>
```
2 Breaking long Lines

    While there is no length limit recommendation for HTML, you may consider wrapping long lines if it significantly improves readability.

    When line-wrapping, each continuation line should be indented at least 4 additional spaces from the original line.

```typescript
// Inappropiate break of lines
<div class="row"> <div class="col-lg-12"> <div class="sec-title"> <h2>Our solution<span class="sec-title-border"><span></span><span></span><span></span></span></h2>
      <p>Swiss Realty offers you a digital, automated, cost-efficient and secure global platform to invest and manage your investments in Real Estate</p> </div> </div>	</div>
```
```typescript
// Correct break of lines
<div class="row">
  <div class="col-lg-12">
      <div class="sec-title">
      <h2>Our solution<span class="sec-title-border"><span></span><span></span><span></span></span></h2>
      <p>Swiss Realty offers you a digital, automated, cost-efficient and secure global platform to invest and manage your investments in Real Estate</p>
    </div>
  </div>
</div>
```  

3 HTML Quotation Marks

    When quoting attribute values please use double quotations ("") instead of single('').

```typescript
        //Correct use of quotation marks
  <img src="assets/img/ico-process.png" class="ico-pictures">            
```
```typescript
        //Incorrect use of quotation marks
  <img src='assets/img/ico-process.png" class="ico-pictures'>            
```    




* css
* php
* Typescript
* scss
* javascript
