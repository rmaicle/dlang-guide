---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Enumerations
section: Properties
subsection: min Property
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

The value of the `min` property of an enumeration is the same as the `init` property value; that is the first member of the enumeration.

{% highlight d linenos %}
import std.stdio;

enum State { On, Unknown, Off }

void main() {
    writeln(State.min);                     // On
}
{% endhighlight %}