---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Type Properties
section: stringof Property
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

The __stringof__ property is an immutable (read-only) string representing the type or expression that comes before it.
The type or expression is not semantically evaluated at compiler time.
If applied to a built-in type, then the result is the language-defined string representation for that type.
If applied to an expression, then the result is the representation of that expression because the expression is only lexically evaluated.

{% highlight d linenos %}
import std.stdio;

uint square(ubyte n) { return n * n; }

void main() {
    writeln(int.stringof);                      // int
    writeln(uint.stringof);                     // uint
    writeln(128u.stringof);                     // 128u
    writeln((128 + 1).stringof);                // 128 + 1
    float f = 3.14159;
    writeln(f.stringof);                        // f
    ubyte b = 255;
    writeln(square(b).stringof);                // square(b)
    writeln(main.stringof);                     // main()
}
{% endhighlight %}

Although it is possible to use the `stringof` property for code generation, it is not advisable to do so because the internal representation of types and expressions may change between compiler versions.
For such code generation purposes, the language offers _Traits_ and other library helper functions.
