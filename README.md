# Development Guidelines
Swiss Realty's development guidelines focus at providing developers both in-house and in the community a clear framework to write code for this project. Swiss Realty commits to provide accessible and readable code to facilitate cross-team work and collaboration, as such every developer working on this project need to follow the guidelines defined in the documents listed below.

## General considerations
Some considerations go accross programming language and should be followed accordingly.

* **Tab size is of 4**

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

* **IDs and labels should be as verbal as possible**
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

* **Spacing is important**
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
## Syntax specific guidelines
