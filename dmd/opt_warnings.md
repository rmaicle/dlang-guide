---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Compilation Options
subsection: Warning Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

###### Warning Options

<div markdown='1' class='syntax'>
    dmd files [...] -w
    dmd files [...] -wi

`-w`
: Warnings as errors; compilation will halt when the compiler encounters a warning or an error.

`-wi`
: Warnings as messages; compilation continues when the compiler encounters a warning.
</div>
