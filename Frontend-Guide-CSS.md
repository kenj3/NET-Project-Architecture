# Frontend Style Guide - CSS
---
## Introduction
There are many options on the 'ideal' style in the world of the Front-End Web Development. Therefore, in order to reduse the confusion on what style we should follow during the development, we urge all people to refer to this style guide for all projects.

## General Formatting Rules
### Capitalization
Use only lowercase

All code has to be lowercase. This applies to CSS selectors, properties and property values.

> ###### Not Recommended
>
>`color: #FFFFFF;`
>
> ###### Recommended
>
>`color: #ffffff;`

### Trailing Whitespace
Reomve trailing white spaces.

Trailing white spaces are unnecessary and can complcate diffs.

> ###### Not Recommended
>
>`color: #FFFFFF;__`
>
> ###### Recommended
>
>`color: #ffffff;`

### Indentation
Indetation should be consistent throughout the entire file. Whther you choose to use tabs or spaces, or 2-spaces vs. 4-spaces, just be consistent!

## General Meta Rules
### Encoding
Use UTF-8

Make sure your editor uses UTF-8 as character encoding.

### Comments
Explain code as needed, where possible.

Use comments to explain code: What does it cover, What porpose does it serve, and why is the respective solution used or preferred?

### Action Items
Mark todos and action items with `TODO:`

Highlight todos by using the keyword `TODO` only. Append action items after a colon like this: `TODO: action item`

> Recommend:
> `/* TODO: add color style */`

## CSS Style Rules
### CSS Validity
Use valid CSS

Using valid CSS is a measurable baseline quality that ensures proper CSS usage allow you to spot CSS code that may not have any effect and can be removed.

### ID and Class Naming
Use meaningful or general ID and Class names.

Instead of presentational of cryptic names, always use ID and Class names that reflect the purpose of element in question or that are otherwise generic. Names that are specific and reflect the purpose of element should be preferred as these are most understandable and least likely to change. Generic names are simply a fallback for elements that have no particular meaning different from their siblings. They are typically needed as helpers.

> Not Recommended
>
> `btn-green {...}`
>
> Recommended
>
> `btn-default {...}`

### Type Selectors
Avoid qualifying ID and class names with type selectors.

Unless necessory(for example, with helper classes), do not use element names in conjuction with IDs or classes. Avoiding unnecessary ancester selectors is useful for performance reasons.

It is also considered bad practice to use IDs in CSS files. There are no situations where IDs provide benefit over classes. If you need to use a unique name for an element, use a class. (The only benefit IDs provide is speed, and is only beneficial on pages with thousands of similar elements)

> Not Recommended
>
> `ul#example {...}`
> 
> `div.error {...}`
>
> Recommended
>
> `.example {...}`
>
> `.error {...}`

### Shorthand Properties
Shorthand should be used

CSS offers a variety of shorthand properties. like `padding` rather than `padding-top`, `padding-left` etc. That should be used whenever possible, with the exception of font properties and properties intend to overwrite properties of the same name in framework such as Bootstrap.

> Not Recommended
``` css
border-top-style: none;
font-family: palatino, georgia, serif;
font-size: 100%;
line-height: 1.6;
padding-bottom: 2em;
padding-left: 1em;
padding-right: 1em;
padding-top: 0;
```

> Recommend
``` css
border-top: 0;
font: 100%/1.6 palatino, georgia, serif;
padding: 0 1em 2em;
```

### 0 and Units
omit unit specification after `0` value.

> Not Recommended:
>
> `margin: 0em;`
>
> Recommended
>
> `margin: 0;`

### Leading 0s
Include leading `0`s in decimal values for readability.

> Not Recommended
>
> `font-size: .9em;`
>
> Recommended
>
> `font-size: 0.9em;`

### Hexadecimal Notation
Use 3-character hexadecimal notation where possible.

> Not Recommended
>
> `color: #eeffcc;`
>
> Recommended
>
> `color: #efc;`

### ID and Class Name Delimeters
Separate words ID and class names by a hyphen (`-`)

Use hyphens to concatenate words and abbreviations in selectors in order to improve understanding and scannability.

One exception: underscores(`_`) are also acceptable separators.

> Not Recommended
> 
> `.errorStatus {...}`
>
> Recommend
>
> `.error-status {...}`

### Hacks
Avoid user agent detection as well as CSS "hacks" - try a different approach first.

## CSS Formatting Rules
### Block Content Indentation
Indent all block content, that is rules within rules as well as declarations to reflect hierarchy and improve understanding.

> Recommend
``` css
@media screen, projection {
    html {
        background: #000;
        color: #fff;
    }
}
```

### Declaration Stops
Use a semicolon after every declaration for consistency and extensibility reasons.

> Not Recommended
``` css
.error-status {
    display: block;
    color: red
}
```
> Recommended
``` css
.error-status {
    display: block;
    color: red;
}
```
