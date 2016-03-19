---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Preliminaries
section: Conventions
subsection: Syntax Display
excerpt: 
group: DLang
tags: [dlang, dguide, draft]
---

Syntax display is presented in a block in monochrome color with three (3) inner blocks; the _heading block_, _syntax block_ and the _definition block_.

Heading Block
: Usually a label or a some description. It can have paragraphs and tables.

Syntax Block
: The syntax format block displays the actual use of a command or function which is displayed in monospace font.

  * Can have multiple syntax specifications
  * Required items are enclosed in angle brackets (`<>`).
  * Optional items are enclosed in square brackets (`[]`).
  * The pipe symbol (`|`) means _or_, meaning one of the items listed.
  * Ellipses (`...`) means one or _more_ of the parameter.

Definition Block
: The definition block contains, well, the definition and/or description of the command, function or arguments in the syntax format block.
It can have paragraphs and tables.

  * Required arguments is formatted as `normal monospaced text`.
  * Optional arguments is formatted as _`italic monospaced text`_.

Here is a simplified example of a _syntax display_ for the reference compiler command-line syntax.

<div markdown='1' class='syntax linenos'>
Optional syntax label or description.

This is an optional paragraph in the heading block.

    dmd --version | --help | -man
    dmd <source[, ...]> [-debug|-release]

This is the start of the definition block.

`source[, ...]`
: One or more source code files separated by a comma.

_`-debug`_
: Description of commmand-line argument.

_`-release`_
: Description of commmand-line argument.
</div>

Here is a mockup example of a function syntax for the `write[f][ln]` functions.

<div markdown='1' class='syntax'>
Syntax of `write` and `writef` Functions

    write[ln] ([argument [, ...]);
    writef[ln]([formatstring,] [argument [, ...]);
    
###### Parameters:    
`formatstring`
: description of `formatstring`.
  
`argument [, ...]`
: One or more arguments.
  
###### Return Value:
None.
</div>
