---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Compilation Options
subsection: Library Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

###### Library Options

<div markdown='1' class='syntax'>
    dmd files [...] -g -debuglib=<name>
    dmd files [...] -defaultlib=<name>

`-debuglib=<name>`
: Set symbolic debug library to `name`.
  Can only be used when symbolic debug information `-g` is used.

`-defaultlib=<name>`
: Set default library to `name`.
</div>
