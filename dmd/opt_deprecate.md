---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Compilation Options
subsection: Deprecation Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

###### Deprecation Options

<div markdown='1' class='syntax'>
    dmd files [...] -d
    dmd files [...] -dw
    dmd files [...] -de

Control deprecated feature reporting.

`-d`
: Silently allow deprecated features.

`-dw`
: Show deprecated features as warnings.
  This is the default setting.

`-de`
: Report deprecated features as errors.

See Output group about warnings and errors.
Deprecated features include symbols with the deprecated attribute or symbols within deprecated code blocks.
</div>
