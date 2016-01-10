---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basics
section: Line Splicing
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Backslash line splicing is used in programming languages like C++ to join two or more lines using the backslash character (`\`).
Line splicing treats the concerned lines as if they are a single line.

{% highlight d linenos %}
Hello \
world!
{% endhighlight %}

Lines 1 and 2 will be joined to form `Hello world!`.

D does not recognize backslash line splicing but the language does not limit the number of characters in a source code line.
