---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Code Generation Options
subsection: Shared Library Option
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

###### Shared Library Option

<div markdown='1' class='syntax'>
    dmd files [...] -shared
    dmd files [...] -shared -fPIC

`-shared`
: Create a `shared` library.

`-shared -fPIC`
: Create a `shared` library and generate Position Independent Code (PIC).
  Note that PIC is available on Linux only.
</div>
