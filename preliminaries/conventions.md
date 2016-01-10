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

##### Syntax Format Display

Syntax formats are displayed in a block and displayed in monochrome.
The following describes what goes into a syntax format display:

* Required items are enclosed in angle brackets `<>`. Used in commands.
* Optional items are enclosed in square brackets `[]`. Used in commands.
* The pipe symbol `|` means _or_, meaning one of the items listed. Used in commands.
* Ellipses `...` means one or _more_ of the parameter. Used in command and function signatures.

Here are some examples of a syntax display:

{% highlight text %}
dmd <source...> [-debug | -release]
int function(T...)(T args);
{% endhighlight %}

##### Generic Display

It is sometimes necessary to display something in monospace format which are not necessarily source codes or program outputs.
These texts are displayed in a block without highlighting or color coding but may be displayed with or without line numbers.

{% highlight text linenos %}
Here is an example of a generic display             
The texts are intentionally not highlighted         # or no syntax coloring
{% endhighlight %}

There is one extra thing to note here.
Although not common, some texts displayed using the generic display format requires some little explanation within the text block.
This is sometimes necessary to achieve compactness and provide a more direct and focused information to the reader regarding.
To achieve this, the use of the hash (`#`) symbol to denote that the text following it are meant to be a comment or remark for the reader.
The comment is usually at the right hand side of the text and are aligned to be easier to distinguish and read.

##### Source Code Display

Source codes are displayed in a block as shown below with syntax highlighting and sometimes with line numbers.
Syntax highlighting helps readers to easily identify parts of the language and line numbers help when referring to concerned source code lines.

Here is an example of a source code block displaying texts to the console.

{% highlight d linenos %}
writeln("D Programming Language");
writeln("Line comment");                // line comment
writeln("Block comment");               /* block comment */
writeln("Nesting block comment");       /+ nesting block comment +/
{% endhighlight %}

Also, to make source code displays a little shorter some common source codes lines are not included.
This avoids syntactic noise that does not necessarily contribute to the actual code being discussed and helps to focus the reader.
The most common candidates for omission are:

* import module statements
* program entry point or the function `main()`

Here is a full blown hello world example that is common.

{% highlight d linenos %}
import std.stdio;                       // omitted

void main() {                           // omitted
    writeln("Hello world!");
}                                       // omitted
{% endhighlight %}

The following code is the result of the omissions made from the above code.
Those are four (4) lines removed.

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
2. Use of `...` in program source code means that 'other code goes here'.


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
