---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Comments
section: Nesting Comment
excerpt: Language comment-styles
group: DLang
tags: [dlang, dguide, draft]
---

Is almost the same as _block comments_.
It spans multiple lines which requires a begin and end comment terminators.
A _nesting block comment_ begins with the slash plus (`/+`) characters and terminates or ends with the plus slash (`+/`) characters.
Anything between the begin and end comment terminators are also ignored as in _block comments_.
It is also used as a pararaph-like comment or remark or as an alternative to the _line comment_.

{% highlight d %}
/+ This is a block comment in one line +/

/+
 + This is a block comment spanning three (3) lines
 +/
{% endhighlight %}

Its difference from the _block comment_ is that it nests.
Meaning, it can appear inside another _nesting block comment_.
It does not matter how many levels of nesting there is as long as the beginning and ending comment terminators match.
The following example using the _block comment_ will produce an error but not when a _nesting block comment_ is used.
The following example uses _nesting block comment_ compiles but not when _block comments_ are used.

~~~
/+                              <-----------------------------+
/+                              <---------------+             |
/+ nesting block comment +/     <--- inner      |  outer      | outer
+/                              <---------------+             |
/+ nesting block comment +/     <--- inner                    |
+/                              <-----------------------------+
~~~

Lines 1 and 6 is the outer block.
Lines 2 and 4 is the inner block.
Line 3 is another inner block within lines 2 and 4.
Line 5 is another inner block within lines 1 and 6.
