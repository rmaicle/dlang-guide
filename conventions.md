---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Conventions
excerpt: 
group: DLang
tags: [dlang, dguide, draft]
---

This section introduces the reader to the conventions used throughout the guide.

###### Source Code Display

Source codes are displayed in a block like the following with syntax highlighting and sometimes line numbers.
The line numbers are displayed to help refer the reader to important parts in the source code.
Also, comments are sometimes included in the source code to aid both the author and the reader.
Comments are also color coded to easily distinguish it from the source code.

Here is an example of a source code block that displays the texts to the console.

{% highlight d linenos %}
writeln("D Programming Language");
writeln("Line comment");                // line comment
writeln("Block comment");               /* block comment */
writeln("Nesting block comment");       /+ nesting block comment +/
{% endhighlight %}

###### Output Display

Source code ouput is displayed in a block like the following.
Output text will be displayed in monochrome which may differ from the actual output in your computer or terminal.
Output will sometimes have line numbers to refer the reader to important parts of the output.
Sometimes the output will have some kind of comment associated with it in the output display.
Comments are displayed with the hash (`#`) character and is color coded to distinguish it from the rest of the output.

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

2. Use of `...` means that 'other code goes here'.


{% comment %}
###### Quotes

A quoted material is presented as follows:

> This is a sample quote - Anonymously Simple

{% endcomment %}
