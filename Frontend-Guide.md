# Frontend Nanodegree Style Guide - HTML
---
## General Formatting Rules

### Capitalization
Use only lowercase.

All code has to be lowercase. This applies to HTML element names, attributes, attribute values (unless text/CDATA).

> ###### Not Recommended
>
>`<A HREF="/">Home</A>`
>
> ###### Recommended
>
>`<a href="/">Home</a>`

### Trailing Whitespace
Remove trailing white spaces.

Trailing white spaces are unnecessary and can complicate diffs.

> ###### Not Recommended:
> 
>`<p>What?</p>__`
>
> ###### Recommended
>
>`<p>What?</p>`

If using Sublime Text, this can be done automatically each time you save a file by adding the following to your User Settings JSON file (you should be able to find this within Sublime Text's menu):

>
>`"trim_trailing_white_space_on_save": true`

### Indentation
Indentation should be consistent throughout the entire file. Whether you choose to use tabs or spaces, or 2-spaces vs. 4-spaces - just be consistent!

## General Meta Rules
###  Encoding
Use UTF-8 (no BOM).

Make sure your editor uses UTF-8 as character encoding, without a byte order mark. Specify the encoding in HTML templates and documents with <meta charset="utf-8">.

### Comments
Explain code as needed, where possible.

Use comments to explain code: What does it cover, what purpose does it serve, and why is the respective solution used or preferred?

### Action Items
Mark todos and action items with `TODO:`

Highlight todos by using the keyword TODO only, not other formats like @@. Append action items after a colon like this: TODO: action item.

> ###### Recommended:
``` html
<!-- TODO: add other fruits -->
<ul>
  <li>Apples</li>
   <li>Oranges</li>
</ul>
```

## HTML Style Rules
### Document Type
Use HTML5.

HTML5 (HTML syntax) is preferred for all HTML documents: `<!DOCTYPE html>`.

Do not close self-closing elements, ie. write `<br>`, not `<br />`.

### HTML Validity
Use valid HTML.

Using valid HTML is a measurable baseline quality that ensures proper HTML usage and contributes to learning about technical requirements and constraints.

> ###### Not Recommended:
```html
<title>Page Title</title>
<article>This is an article.</article>
```
> ###### Recommended:
```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Page Title</title>
    </head>
    <body>
        <article>This is an article.</article>
    </body>
</html>
```

### Semantics
Use HTML according to its purpose.

Use elements for what they have been created for. For example, use heading elements for headings, p elements for paragraphs, a elements for anchor, etc. Using HTML according to its purpose is important for accessibility, reuse and code efficiency reasons.

> ###### Not Recommended:
>
> `<div onclick="goToRecommendations();">All recommendations</div>`
>
> ###### Recommended:
>
> `<a href="recommendations/">All recommendations</a>`



