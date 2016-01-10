---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Integral Types
subsection: Integral Properties
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

The following Type Propertes are defined for integral types:

* __stringof__ - 
* __mangleof__ -
* __sizeof__ -
* __alignof__ - 
* __init__ - initial value the language assigns to the type
* __min__ - minimum or smallest value the type can accommodate
* __max__ - maximum or largest value the type can accommodate

{% comment %}
| Property | Description |
|:--------:|-------------|
| init	   | initial value the language assigns to the type |
| min	   | minimum or smallest value the type can accommodate |
| max	   | maximum or largest value the type can accommodate |
{% endcomment %}

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

{% comment %}
The following table shows the integral properties of all integral types.

| stringof        | mangleof | sizeof (bytes) | alignof (bytes) | init | min (from)                 | max (to)                   |
|-----------------|:--------:|:--------------:|:---------------:|:----:|---------------------------:|---------------------------:|
| byte            |    g     |   1            |   1             |  0   | -128                       | +127                       |
| ubyte           |    h     |   1            |   1             |  0   | 0                          | 255                        |
| short           |    s     |   2            |   2             |  0   | -32,768                    | 32,767                     |
| ushort          |    t     |   2            |   2             |  0   | 0                          | 65,535                     |
| int             |    i     |   4            |   4             |  0   | -2,147,483,648             | 2,147,483,647              |
| uint            |    k     |   4            |   4             |  0   | 0                          | 4,294,967,295              |
| long            |    l     |   8            |   8             |  0L  | -9,223,372,036,854,775,808 | 9,223,372,036,854,775,807  |
| ulong           |    m     |   8            |   8             |  0UL | 0                          | 18,446,744,073,709,551,615 |
| cent            |          |                |                 |      |                            |                            |
| ucent           |          |                |                 |      |                            |                            |
{% endcomment %}
