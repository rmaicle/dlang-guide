---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Preliminaries
section: Conventions
subsection: Source Code Block
excerpt: 
group: DLang
tags: [dlang, dguide, draft]
---

Source codes are displayed in a block as shown below with syntax highlighting and sometimes with line numbers.
Syntax highlighting helps the reader to easily identify parts of the language while line numbers help when referring to specific source code lines.

Here is an example of a source code block displaying texts to the console.

{% highlight d linenos %}
writeln("D Programming Language");
writeln("Line comment");                // line comment
writeln("Block comment");               /* block comment */
writeln("Nesting block comment");       /+ nesting block comment +/
{% endhighlight %}

Also, to make source code block texts a little shorter, some common source code lines are not included.
This avoids syntactic noise that does not necessarily contribute to the actual code being discussed.
The most common candidates for omission are:

* import module statements
* program entry point or the function `main()`

Here is a small hello world program source code text example showing how to print the text 'Hello world!' to the standard output.

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

###### A Note on Source Code Texts

Source code texts are meant to present a program snippet for teaching and learning.
The convention used here is not a recommendation on how to write real programs.
Experienced programmers might therefore see violations and/or divergence from common and proper coding practices.

1. Comments are used to explain some code even though the code is discussed in the text.
   This is intentional.
   Comments are meant to be a summary or a quick note to the reader of what is happening on a piece of source code.
2. Use of ellipses (`...`) in program source code means that _'other code goes here'_.
