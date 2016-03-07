---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Integral Types
subsection: Properties
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

The following Type Propertes are defined for integral types:

* __stringof__ - string representation
* __mangleof__ - text representation.
* __sizeof__ - size of the integral type in bytes.
* __alignof__ - alignmen to the integral type in bytes.
* __init__ - initial value the language assigns to the type.
* __min__ - smallest value that the integral type can accommodate (the size of the type affects this value).
* __max__ -  largest value the type can accommodate (the size of the type affects this value).

The following table shows the integral type property values.
The `min` and `max` property values are formatted for convenience using the comma symbol for digit grouping.

| Type   | sizeof | alignof | init | min                        | max                         |
|--------|:------:|:-------:|:----:|---------------------------:|----------------------------:|
| byte   |   1    |   1     |  0   | -128                       | +127                        |
| ubyte  |   1    |   1     |  0   | 0                          | +255                        |
| short  |   2    |   2     |  0   | -32,768                    | +32,767                     |
| ushort |   2    |   2     |  0   | 0                          | +65,535                     |
| int    |   4    |   4     |  0   | -2,147,483,648             | +2,147,483,647              |
| uint   |   4    |   4     |  0   | 0                          | +4,294,967,295              |
| long   |   8    |   8     |  0L  | -9,223,372,036,854,775,808 | +9,223,372,036,854,775,807  |
| ulong  |   8    |   8     |  0UL | 0                          | +18,446,744,073,709,551,615 |
| cent   |        |         |      |                            |                             |
| ucent  |        |         |      |                            |                             |

The following code demonstrates the use of the integral properties.

{% highlight d linenos %}
writeln(typeof(128).stringof);              // int
writeln(typeof(0b_1000_0000).stringof);     // int
writeln(typeof(0x80).stringof);             // int

writeln(typeof(128u).stringof);             // uint
writeln(typeof(0b_1000_0000u).stringof);    // uint
writeln(typeof(0x80u).stringof);            // uint
{% endhighlight %}

[Type Properties]: /dlang-guide/types/properties/index.html
