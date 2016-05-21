---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Compilation Options
subsection: Unit Test Option
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

###### Unit Test Option

<div markdown='1' class='syntax'>
    dmd files [...] -unittest

`-unittest`
: Compile in _unit test code blocks_ and incorporate them into the resulting executable.
  This option turns on asserts and defines the `unittest` version identifier.
</div>
