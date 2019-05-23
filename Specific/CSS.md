# CSS

## CSS Style Rules

### CSS Validity

* Use valid CSS where possible.

* Using valid CSS is a measurable baseline quality attribute that allows to identify CSS code that may not have any effect and can be removed, and that ensures valid CSS usage.

### ID and Class Naming

* Use meaningful or generic ID and class names.

* Instead of cryptic names, always use ID and class names that reflect the purpose of the element in question.

* Names that are specific and reflect the purpose of the element should be preferred as these are most understandable and the least likely to change.

* Generic names are simply a fallback for elements that have no particular and clear destination. They are typically needed as “helpers.”

* Using functional or generic names reduces the probability of unnecessary document or template changes.

```css
/* Not recommended: meaningless */
#randomref-134{}

/* Not recommended: presentational */
.clear{}
```

```css
/* Recommended: specific */
.team-member-info {
    padding: 20px 10px;
}
/* Recommended: generic */
.alt {}
```
### ID and Class Name Style

* Use ID and class names that are as short as possible but as long as necessary.

* Try to convey what an ID or class is about while being as brief as possible.

* Using ID and class names this way contributes to acceptable levels of understandability and code efficiency.

```css
/* Not recommended */
.download-button-text {
    flex: 20;
}
```

```css
/* Recommended */
.download-btn-text {
    flex: 20;
}
```
### Type Selectors

* Avoid qualifying ID and class names with type selectors.

```css
/* Not recommended */
ul#example {}  
div.author-img {}
```
```css
/* Recommended */
#example {}
.author-img {}
```
### Shorthand Properties

* Use shorthand properties where possible.

* Using shorthand properties is useful for code efficiency and understandability.

```css
/* Not recommended */
{
border-top-style: none;
font-family:'Libre Baskerville';
font-size: 100%;
line-height: 1.6;
padding-bottom: 5em;
padding-left: 1em;
padding-right: 1em;
padding-top: 1;
}
```
```css
/* Recommended */
{
border-top: 0;
font: 100%/1.6 'Libre Baskerville';
padding: 1 1em 5em;
}
```

### 0 and Units

* Omit unit specification after “0” values, unless required.

```css
{
margin: 0 20px 0 0; /* Not ambiguous without the unit */
border: 0;
outline: 0
}
```

### Leading 0s

* Omit leading “0”s in values.

* Do not put 0s in front of values or lengths between -1 and 1.

```css
.hero-area-single-slide p {
    -webkit-transform: translateX(-140px);
    transform: translateX(-140px);
    -webkit-transition: all .15s linear 0s; /* Omitted leading 0s*/
    transition: all .15s linear 0s;
  }
```
### Hexadecimal Notation

* Use 3 character hexadecimal notation where possible.

```css
.hero-area-content {
    color: #fff;
  }
```

### Prefixes

* In large projects as well as for code that gets embedded in other projects or on external sites use prefixes (as namespaces) for ID and class names.

* Using namespaces helps preventing naming conflicts and can make maintenance easier, for example in search and replace operations.

```css
.showcase-area {
	padding-bottom: 50px;
}
.single-showcase-box {
	padding: 0 0 40px;
}
.single-showcase-box p {
	margin: 20px 0 25px;
}
.single-showcase-box h4 {
	font-size: 20px;
}
```
### ID and Class Name Delimiters

* Separate words in ID and class names by a hyphen.

* Do not concatenate words and abbreviations in selectors by any characters other than hyphens, in order to improve understanding.

```css
/* Not recommended: does not separate the words “city” and “offices” */
#citiesoffices {
    display: inline-block;
    font-size: 15px;
    text-transform: uppercase;
    font-family: 'Libre Baskerville';
    margin: 0 20px 0 0;
}
```
```css
/* Recommended */
#cities-offices {
    display: inline-block;
    font-size: 15px;
    text-transform: uppercase;
    font-family: 'Libre Baskerville';
    margin: 0 20px 0 0;
}
```

## CSS Formatting Rules

### Block Content Indentation

* Indent all block content.

* Indent all block content, that is rules within rules as well as declarations, so to reflect hierarchy and improve understanding.

```css
/* Recommended Indentation */
@media only screen and (min-width: 768px) and (max-width: 1024px) {
  .mobDisc {
    display: none;
  }
  .deskTabDisc {
    display: inline-block;
  }
  .dropdown-content {
    display: none;
  }
}
```
### Declaration Stops

* Use a semicolon after every declaration.

* End every declaration with a semicolon for consistency and extensibility reasons.

```css
/* Not Recommended */
.investment-page-download h4 {
  transition: 0.6s;
  transition-property: all /* Improper use of declaration stops */
  transition-duration: 0.6s;
  transition-timing-function: ease;
  transition-delay: 0s /* Improper use of declaration stops */
}
```

```css
/* Recommended */
.investment-page-download h4 {
  transition: 0.6s;
  transition-property: all;
  transition-duration: 0.6s;
  transition-timing-function: ease;
  transition-delay: 0s;
}
```
### Property Name Stops

* Use a space after a property name’s colon.

* Always use a single space between property and value (but no space between property and colon) for consistency reasons.

```css
/* Not Recommended */
.accept-button {
  background-color:#5bb237; /* Improper use of name stops */
  margin-right:10px; /* Improper use of name stops */
}
```

```css
/* Recommended */
.accept-button {
  background-color: #5bb237;
  margin-right: 10px;
}
```

### Declaration Block Separation

* Use a space between the last selector and the declaration block.

* Always use a single space between the last selector and the opening brace that begins the declaration block.

* The opening brace should be on the same line as the last selector in a given rule.

```css
/* Not recommended: missing space */
.disclaimer-text li{
  margin: 0 0 10px;
}
/* Not recommended: unnecessary line break */
.disclaimer-text li
{
  margin: 0 0 10px;
}
```

```css
/* Recommended */
.disclaimer-text li {
  margin: 0 0 10px;
}
```

### Selector and Declaration Separation

* Separate selectors and declarations by new lines.

* Always start a new line for each selector and declaration.

```css
/* Not recommended */
h1, h2, h3, h4, h5, h6 {
  font-family: 'Libre Baskerville', serif;
  font-weight: 500;
}

```

```css
/* Recommended */
h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: 'Libre Baskerville', serif;
  font-weight: 500;
}
```
### Rule Separation

* Separate rules by new lines.

* Always put a blank line (two line breaks) between rules.

```css
.sec-title {
  text-align: center;
  max-width: 450px;
  margin: 0 auto 40px;
}

.sec-title h2 {
  padding-bottom: 20px;
  margin-bottom: 20px;
  position: relative;
  top: -6px;
}
```
