---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Boolean Type
subsection: Properties
subsubsection: init Property
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

The boolean type `init` Property value is the boolean [literal] `false`.

{% highlight d linenos %}
import std.stdio;

void main() {
    writeln(bool.init);
}
{% endhighlight %}

[literal]: /dlang-guide/basic_types/boolean/literals.html
