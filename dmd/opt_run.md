---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Compilation Options
subsection: Run Option
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

###### Run Option

<div markdown='1' class='syntax'>
    dmd -run <source> [arg ...]

`-run <source> [arg ...]`
: Execute resulting program.
  If compilation is successful this executes the resulting program `-_run_ <_source_>`.
  Arguments to the program can be passed as command-line arguments `-_arg_ ...`.
  Compilation does not produce object or executable file.
</div>
