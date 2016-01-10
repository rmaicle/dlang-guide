---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Comments
section: Block Comment
excerpt: Language comment-styles
group: DLang
tags: [dlang, dguide, draft]
---

Also sometimes called multi-line comments are comments that span multiple lines which means it requires begin and end comment terminators.
A block comment begins with the slash asterisk (`/*`) characters and terminates or ends with the asterisk slash (`*/`) characters.
Anything between the begin and end comment terminators are ignored.
It is often used as a paragraph-like comment.
It is also used as an alternative to the _line comment_.

{% highlight d %}
/* This is a block comment in one line */

/*
 * This is a block comment spanning three (3) lines
 */
{% endhighlight %}

Careful with multiple terminating block comments (`*/`).
The compiler recognizes only the first block comment terminator that it finds after a beginning block comment.
That means that in the following code, line 4 onwards will not be treated as comments and the second (2nd) block comment terminator will cause an error.

{% highlight d linenos %}
/*
This is a block comment spanning three (3) lines
*/
writeln("hello");
*/
{% endhighlight %}
