---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Lexical
section: Digraphs and Trigraphs
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

There are no digraphs or trigraphs in the D programming language.

Digraphs and trigraphs are sequences of two and three characters in a source file which are treated by certain programming languages as a single character.
The ANSI C committee created _trigraphs_ as a way to map certain character combinations in European national ISO-646 character sets to the equivalent ASCII characters.
The C standard included _digraphs_ in the 1999 standard of the language. Digraphs were created to make some trigraphs more readable.

| Triraph | Digraph | ASCII character equivalent |
|:-------:|:-------:|----------------------------|
| ??=     | %:      | #
| ??/     |         | \
| ??'     |         | ^
| ??(     | <:      | [
| ??)     | :>      | ]
| ??!     |         | |
| ??<     | <%      | {
| ??>     | %>      | }
| ??-     |         | ~

Curious how the hello world C program looks like using trigraphs?

{% highlight c linenos %}
??=include<stdio.h>

int main(void)
??<
  printf("Hello, world!??/n");
  return 0;
??>
{% endhighlight %}

Now, using digraphs:

{% highlight c linenos %}
%:include<stdio.h>
int main()
<%
  printf("Hello, world!\n");
  return 0;
%>
{% endhighlight %}
