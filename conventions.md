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

1. Syntax format is displayed in a block.
Optional parameters are enclosed in square brackets `[]`.
Required parameters are enclosed in angle brackets `<>`.
When the ellipses symbol `...` is used, it means can be _more_ than one.
Commands or other items are shown in plain text.
2. Comments are used to explain some code even though the code is discussed in the text.
This is intentional.
The source code comments are meant to be a summary or a quick note to the reader of what is happening on a line of code.
3. Use of `...` in program source code means that 'other code goes here'.


{% comment %}
###### Quotes

A quoted material is presented as follows:

> This is a sample quote - Anonymously Simple

{% endcomment %}
