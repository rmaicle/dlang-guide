---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Preliminaries
section: Conventions
subsection: Console and Output Block
excerpt: 
group: DLang
tags: [dlang, dguide, draft]
---

Console and program outputs are also displayed in a block but texts are displayed without syntax highlighting or color coding with an exception to comments or remarks.
Comments or remarks are not part of the actual console texts or program outputs but manually embedded to provide additional information.
Comments are colored for easy identification and begins with the hash (`#`) character followed by some text.
Line numbers may or may not be present.
If it is present, its purpose is to be able to refer to lines of text.

Here is an example of a console or output display.

{% highlight bash session linenos %}
$ ./console_output
D Programming Language
Line comment                            # line comment
Block comment                           # block comment
Nesting block comment                   # nesting block comment
{% endhighlight %}
