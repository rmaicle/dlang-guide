---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Compilation Options
subsection: Debug Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

###### Debug Options

<div markdown='1' class='syntax'>
    dmd files [...] -debug
    dmd files [...] -debug=level ...
    dmd files [...] -debug=identifier ...

`-debug`
: Compile a debug build and include _debug code blocks_.
  Specifying `-debug` is equivalent to specifying `-debug=1`.

`-debug=level ...`
: Compile in _debug code blocks_ that satisfy the condition <= `level`.
  Multiple levels may be set as in `-debug=1 -debug=2`.

`-debug=identifier ...`
: Compile in _debug code blocks_ that satisfy the condition == `identifier`.
  Multiple identifiers may be set as in `-debug=alpha -debug=beta`.
</div>
