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
