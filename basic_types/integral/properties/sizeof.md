---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Integral Types
subsection: Properties
subsubsection: sizeof Property
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

The integral types `sizeof` Property values in bytes are shown in the following table.

| Type   | sizeof |
|--------|:------:|
| byte   | 1
| ubyte  | 1
| short  | 2
| ushort | 2
| int    | 4
| uint   | 4
| long   | 8
| ulong  | 8

{% highlight d linenos %}
import std.stdio;

void main() {
    writeln(byte.sizeof);
    writeln(ubyte.sizeof);
    
    writeln(short.sizeof);
    writeln(ushort.sizeof);
    
    writeln(int.sizeof);
    writeln(uint.sizeof);
    
    writeln(long.sizeof);
    writeln(ulong.sizeof);
}
{% endhighlight %}