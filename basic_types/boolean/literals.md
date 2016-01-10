---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Boolean Type
subsection: Literals
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Boolean literals use the built-in keywords `true` or `false`.
The integer literal zero (0) and one (1) is implicitly converted to a boolean type; one (1) is equal to `true` and zero (0) is equal to `false`.

{% highlight d linenos %}
bool a = 0;
bool b = 1;
writeln(a);
writeln(b);
{% endhighlight %}
