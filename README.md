# Development Guidelines
Swiss Realty's development guidelines focus at providing developers both in-house and in the community a clear framework to write code for this project. Swiss Realty commits to provide accessible and readable code to facilitate cross-team work and collaboration, as such every developer working on this project need to follow the guidelines defined in the documents listed below.

## General considerations
Some considerations go accross programming language and should be followed accordingly.

### Tab size is of 4

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

### IDs and labels should be as verbal as possible
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

### Spacing is important
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

### Comment, comment, comment
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
// wromg commenting behavior

public function returnValue(value: string) {
	let valueHolder = value
	console.log(valueHolder)
	return valueHolder
}
```

## Syntax specific guidelines
