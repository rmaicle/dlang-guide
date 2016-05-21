---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Code Generation Options
subsection: Bounds Checking Option
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

###### Bounds Checking

<div markdown='1' class='syntax'>
    dmd files [...] -boundscheck=on
    dmd files [...] -boundscheck=safeonly
    dmd files [...] -boundscheck=off

`-boundscheck=on`
: Turn on bounds checking. This is the default for debug builds.
  
`-boundscheck=safeonly`
: Enable bounds checking of `@safe` code only.
  
`-boundscheck=off`
: Disable bounds checking.
</div>
