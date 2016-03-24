---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Enumerations
section: Properties
subsection: max Property
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

The value of the `max` property of an enumeration is the last member of the enumeration.

{% highlight d linenos %}
import std.stdio;

enum State { On, Unknown, Off }

void main() {
    writeln(State.max);                     // Off
}
{% endhighlight %}