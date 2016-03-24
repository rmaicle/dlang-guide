---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Void Type
subsection: Properties
subsubsection: alignof Property
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

The void type `alignof` Property value is 1 byte or 8 bits.

{% highlight d linenos %}
import std.stdio;

void main() {
    writeln(void.alignof);
}
{% endhighlight %}
