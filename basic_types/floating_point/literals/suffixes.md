---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Floating Point Types
subsection: Literals
subsubsection: Suffixes
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

> Floating literals with no suffix are of type double.
> Floats can be followed by one f, F, or L suffix.
> The f or F suffix means it is a float, and L means it is a real.
> If a floating literal is followed by i, then it is an ireal (imaginary) type.

> Complex literals are not tokens, but are assembled from real and imaginary expressions during semantic analysis:
>
>     4.5 + 6.2i  // complex number (phased out)
