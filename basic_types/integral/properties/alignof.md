---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Integral Types
subsection: Properties
subsubsection: alignof Property
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

The integral types `alignof` Property values in bytes are shown in the following table.

| Type   | alignof |
|--------|:-------:|
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
    writeln(byte.alignof);
    writeln(ubyte.alignof);
    
    writeln(short.alignof);
    writeln(ushort.alignof);
    
    writeln(int.alignof);
    writeln(uint.alignof);
    
    writeln(long.alignof);
    writeln(ulong.alignof);
}
{% endhighlight %}
