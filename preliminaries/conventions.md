---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Preliminaries
section: Conventions
excerpt: 
group: DLang
tags: [dlang, dguide, draft]
---

This section introduces the reader to the conventions used throughout the guide.

##### Syntax Display

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

##### Generic Display

It is sometimes necessary to display something in monospace format which are not necessarily source codes or program outputs.
These texts are displayed in a block without highlighting or color coding but may be displayed with or without line numbers.

Although not common, some texts displayed using the generic display format may need some explanation.
This is sometimes necessary to achieve compactness and provide a more direct and focused information for the reader.
To achieve this, the use of the hash (`#`) symbol to denote that the text following the symbol is meant to be a comment or remark.

{% highlight text linenos %}
Here is an example of a generic display             
The texts are intentionally not highlighted         # this is a comment
{% endhighlight %}

##### Source Code Display

Source codes are displayed in a block as shown below with syntax highlighting and sometimes with line numbers.
Syntax highlighting helps the reader to easily identify parts of the language while line numbers help when referring to specific source code lines.

Here is an example of a source code block displaying texts to the console.

{% highlight d linenos %}
writeln("D Programming Language");
writeln("Line comment");                // line comment
writeln("Block comment");               /* block comment */
writeln("Nesting block comment");       /+ nesting block comment +/
{% endhighlight %}

Also, to make source code displays a little shorter, some common source code lines are not included.
This avoids syntactic noise that does not necessarily contribute to the actual code being discussed.
The most common candidates for omission are:

* import module statements
* program entry point or the function `main()`

Here is a small hello world example.

{% highlight d linenos %}
import std.stdio;                       // omitted
                                        // omitted
void main() {                           // omitted
    writeln("Hello world!");
}                                       // omitted
{% endhighlight %}

Compare the following code with the one above.

{% highlight d linenos %}
writeln("Hello world!");
{% endhighlight %}

##### Source Code Text

The following are concerned with how source code is written or presented to the reader.
The source codes presented here are meant to present information for teaching and learning.
The convention used here is not recommended as a convention to follow.
Experienced programmers might therefore see violations and/or divergence from common and proper coding practices.

1. Comments are used to explain some code even though the code is discussed in the text.
   This is intentional.
   The source code comments are meant to be a summary or a quick note to the reader of what is happening on a line of code.
2. Use of ellipses (`...`) in program source code means that _'other code goes here'_.

##### Console and Output Display

Console and program outputs are also displayed in a block but texts are displayed in monochrome or without syntax highlighting with an exception to comments or remarks.
Comments or remarks are not part of the actual console texts or program outputs but manually embedded so as to provide information on the actual console text or program output.
Comments are colored for easy identification and begins with the hash (`#`) character followed by some comment text.
Line numbers may or may not be present. If it is present its purpose is the same as source code displays.

Here is an example of a console or output display.

{% highlight bash session linenos %}
$ ./console_output
D Programming Language
Line comment                            # line comment
Block comment                           # block comment
Nesting block comment                   # nesting block comment
{% endhighlight %}

##### Quotes and Quotations

A quoted material is presented as follows:

> This is a sample quote - Anonymously Simple

{% comment %}
{% highlight text %}
┌─┐
│ │
└─┘
◀ ▶ ▲ ▼
{% endhighlight %}
{% endcomment %}