# Frontend Nanodegree Style Guide - HTML
---
## General Formatting Rules

### Capitalization
Use only lowercase.

All code has to be lowercase. This applies to HTML element names, attributes, attribute values (unless text/CDATA).

Not Recommended

    <A HREF="/">Home</A>

> Recommended

    <a href="/">Home</a>  

### Trailing Whitespace
Remove trailing white spaces.

Trailing white spaces are unnecessary and can complicate diffs.

Not Recommended:

    <p>What?</p>__

Recommended

    <p>What?</p>

If using Sublime Text, this can be done automatically each time you save a file by adding the following to your User Settings JSON file (you should be able to find this within Sublime Text's menu):

    "trim_trailing_white_space_on_save": true

