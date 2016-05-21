---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Intermediate Options
subsection: Object File Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

###### Object File Options

<div markdown='1' class='syntax'>
    dmd files [...] -o-
    dmd files [...] -od<path>
    dmd files [...] -of<filename>
    dmd files [...] -op

`-o-`
: Do not write object file.

`-od<path>`
: Write object and library files to `path`.

`-of<filename>`
: Write object to `filename`.

`-op`
: Preserve source path for output files.
</div>
