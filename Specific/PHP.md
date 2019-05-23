# PHP

## PHP Style and Formatting Rules

### Introduction

* This section of the development guidelines comprises what should be considered the standard coding elements that are required to ensure a high level of technical interoperability between shared PHP code.

## Files

### PHP Tags

* PHP code must use the long <?php ?> tags or the short-echo <?= ?> tags; it MUST NOT use the other tag variations.

### Side Effects

* A file should declare new symbols (classes, functions, etc.) and cause no other side effects, or it should execute logic with side effects, but should not do both.

* The phrase "side effects" means execution of logic not directly related to declaring classes, functions, constants, etc., merely from including the file.

```PHP
// Not recommended //
<?php

ini_set('error_reporting', E_ALL);


include "file.php";


// declaration
function foo()
{
    // function body
}
?>
```

```PHP
/*  Recommended */

<?php
// declaration
function foo()
{
    // function body
}

// conditional declaration is *not* a side effect
if (! function_exists('bar')) {
    function bar()
    {
        // function body
    }
}
?>
```

###  Class Constants, Properties, and Methods

* The term "class" refers to all classes, interfaces, and traits.

* Whatever naming convention is used SHOULD be applied consistently within a reasonable scope. That scope may be vendor-level, package-level, class-level, or method-level.

* Method names MUST be declared in camelCase().

```PHP
<?php

    // arrays of the links for the navigation
    $navArray = array(
        "home" => array( // lay out of dropdown menu
          ?>
```
