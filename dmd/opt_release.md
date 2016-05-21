---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Compilation Options
subsection: Release Option
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

###### Release Option

<div markdown='1' class='syntax'>
    dmd files [...] -release

`-release`
: Compile a release build with unoptimized code.
  Release versions do not include internal run-time checks for contracts and assertions; array bounds checking is not done for `@system` and `@trusted` functions.
  Assertion failures will result to undefined behaviour.
</div>

See [Optimize Option](./opt_optimize.html).
