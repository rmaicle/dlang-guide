---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Diagnostic Options
subsection: Module Dependency Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

###### Module Dependency Options

<div markdown='1' class='syntax'>
    dmd files [...] -deps
    dmd files [...] -deps=filename

`-deps`
: Display module dependencies in verbose format (imports/file/version/debug/lib).

`-deps=filename`
: Write module dependencies to `filename` in imports-only format.
</div>
