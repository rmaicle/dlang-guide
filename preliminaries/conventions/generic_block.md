---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Preliminaries
section: Conventions
subsection: Generic Block
excerpt: 
group: DLang
tags: [dlang, dguide, draft]
---

It is sometimes necessary to display some texts in monospace format which are not necessarily source codes or program outputs.
These texts are displayed in a block without highlighting or color coding and may be displayed with line numbers.

Although not common, some texts displayed using the generic display format may need a short explanation or remark.
This is sometimes necessary to achieve compactness and provide a more direct and focused information for the reader.
To achieve this, the use of the hash (`#`) symbol to mark the beginning of a comment or remark.

{% highlight text linenos %}
Here is an example of a generic display             
The texts are intentionally not highlighted         # this is a comment
{% endhighlight %}
