---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Conventions
excerpt: 
group: DLang
tags: [dlang, dguide, draft]
---

This section introduces the reader to the conventions used throughout the guide.

###### Syntax Format Display

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

###### Source Code Display

Source codes are displayed in a block as shown below with syntax highlighting and sometimes with line numbers.
Syntax highlighting helps readers to easily identify parts of the language and line numbers help when referring to concerned source code lines.

Here is an example of a source code block displaying texts to the console.

{% highlight d linenos %}
writeln("D Programming Language");
writeln("Line comment");                // line comment
writeln("Block comment");               /* block comment */
writeln("Nesting block comment");       /+ nesting block comment +/
{% endhighlight %}

###### Console and Output Display

Console and program output is also displayed in a block but texts are displayed in monochrome or without syntax highlighting with an exception to comments or remarks.
Comments or remarks are not part of the actual console texts or program outputs but embedded by the author so as to provide information on the actual console text or program output.
They are colored for easy identification and begins with the hash (`#`) character followed by some comment text.
Line numbers will also be present with the same purpose as source code displays.

Here is an example of a console or output display.

{% highlight bash session linenos %}
D Programming Language
Line comment                            # line comment
Block comment                           # block comment
Nesting block comment                   # nesting block comment
{% endhighlight %}

###### Source Code Conventions

The following are concerned with how source code is written or presented to the reader.
Note that this source code convention is not how the author actually writes code and is not a recommended practice for the user.
The source codes presented here are meant for teaching and learning.
Experienced programmers might therefore see violations and/or divergence from common and proper programming practice.

1. Comments are used to explain some code even though the code is discussed in the text.
This is intentional.
The source code comments are meant to be a summary or a quick note to the reader of what is happening on a line of code.
2. Use of `...` in program source code means that 'other code goes here'.


{% comment %}
###### Quotes

A quoted material is presented as follows:

> This is a sample quote - Anonymously Simple

{% endcomment %}
