---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Type Properties
section: alignof Property
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

The `alignof` property gives the alignment in bytes of a type or expression.
Because the type or expression is only evaluated lexically, a struct or class does not need to be instantiated to use its `alignof` property.

{% highlight d linenos %}
import std.stdio;

struct A {
    int a;
    float f;
}

void main() {
    writeln(A.a.alignof);           // 4
	writeln(A.f.alignof);           // 4
    writeln(A.alignof);             // 4
}
{% endhighlight %}