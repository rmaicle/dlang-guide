---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Enumerations
section: Properties
subsection: init Property
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

The value of the `init` property of an enumeration is the first member of the enumeration.

{% highlight d linenos %}
import std.stdio;

enum State { On, Unknown, Off }

void main() {
    writeln(State.init);                    // On
}
{% endhighlight %}