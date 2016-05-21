---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Code Generation Options
subsection: Architecture Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

###### Architecture

<div markdown='1' class='syntax'>
    dmd files [...] -m32
    dmd files [...] -m64

Generate target binary architecture.

`-m32`
: Generate target as 32-bit machine code.
  This is the default when building on a 32-bit host machine.

`-m64`
: Generate target as 64-bit machine code.
  This is the default when building on a 64-bit host machine.

Regardless of host architecture and compiler binary build, a 32-bit or a 64-bit machine code can be generated.
Although, generating the target binary architecture requires a binary compatible druntime, phobos library and linker.
</div>
