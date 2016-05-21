---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Compilation Options
subsection: Version Identifier Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

###### Version Identifier Options

<div markdown='1' class='syntax'>
    dmd files [...] -version=level ...
    dmd files [...] -version=identifier ...

`-version=level ...`
: Compile in _version code blocks_ that satisfy the condition <= `level`.
  Multiple levels may be set as in `-version=1 -version=2`.

`-version=identifier ...`
: Compile in _version code blocks_ that satisfy the condition == `identifier`.
  Multiple identifiers may be set as in `-version=alpha -version=beta`.
</div>
