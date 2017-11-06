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
> `ul#example {...}`
> 
> `div.error {...}`
>
> Recommended
> `.example {...}`
>
> `.error {...}`

