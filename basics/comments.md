---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basics
section: Comments
excerpt: Language comment-styles
group: DLang
tags: [dlang, dguide, draft]
---

A comment is a kind of program annotation. It is primarily used to add _comments_ or _remarks_ on a piece of code.
As in other programming languages, comments are ignored or discarded by the D compiler and may be placed anywhere in the source text.
D inherits the C and C++ style comments; _block_ and _line_ comments.
D has added its own comment style, the _nesting block_ comment, which is also present in the _Free Pascal_ language although, of course, with a different syntax.

| Begin | End   | Name |
|:-----:|:-----:|------|
| `//`  | none  | Line Comment |
| `/*`  | `*/`  | Block Comment |
| `/+`  | `+/`  | Nesting Block Comment |

##### Line Comment

Also sometimes called inline comments are comments that span only in the line it is on.
A line comment starts with double slash (`//`) characters. Any characters on the same line after it is ignored.
It is used as an alternative to the block comment when commenting or remarking with only a single line.
Programmers sometimes prefer to type less for single line comments.

{% highlight d %}
// This is a line comment
{% endhighlight %}

##### Block Comment

Also sometimes called multi-line comments are comments that span multiple lines which means it requires begin and end comment terminators.
A block comment begins with the slash asterisk (`/*`) characters and terminates or ends with the asterisk slash (`*/`) characters.
Anything between the begin and end comment terminators are ignored.
It is often used as a paragraph-like comment or remark.
It can be used as an alternative to the _line comment_.

{% highlight d %}
/* This is a block comment in one line */

/*
 * This is a block comment spanning three (3) lines
 */
{% endhighlight %}

##### Nesting Block Comment

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

{% highlight d linenos %}
/+
/+
/+ nesting block comment +/
+/
/+ nesting block comment +/
+/
{% endhighlight %}

Lines 1 and 6 is the outer block.
Lines 2 and 4 is the inner block.
Line 3 is another inner block within lines 2 and 4.
Line 5 is another inner block within lines 1 and 6.


{% comment %}
Here is another use for this comment style.
In this example, the compiler will process the line numbers 1, 3 and 4 and will ignore line number 2.

{% highlight d linenos %}
a
/* block comment */
b
c
{% endhighlight %}

If we want to _comment out_ line numbers 1-3, we cannot use the _block comment_ style to do that (see example below).
Because when the compiler scans the text and sees the beginning of the _block comment_ at line 1, it will ignore everything until it sees the closing block comment at line 3.
The ending block comment at line 5 will result in an error.

{% highlight d linenos %}
/*
a
/* block comment */
b
*/                      <--- error: no matching opening block comment
c
{% endhighlight %}

To solve it, the _nesting block comment_ is used instead of the C-style _block comment_.
The compiler will see the beginning _nesting block comment_ at line 1 and will scan the text until it sees the closing _nesting block comment_ terminators at line 5.

{% highlight d linenos %}
/+
a
/* block comment */
b
+/
c
{% endhighlight %}

##### Why Is the C-Style Block Comment Still Present?

{% comment %}
The _nesting block comment_ was brought about by necessity to solve the problem presented above.
There was no _nesting block comment_ in the early days of D.
As the language grew, the reasonable need to add a new comment style emerged and is now a very convenient feature of the language.
Because it allows reusing C code without modifications and because the _nesting block comment_, solves the nesting problem if you need to do it.
{% endcomment %}

The simple reason of being able to compile C source files without modification.
{% endcomment %}
