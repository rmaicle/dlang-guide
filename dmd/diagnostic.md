---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Diagnostic Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

| Option | Description |
|--------|-------------|
| `-cov` | [do code coverage analysis](./opt_coverage.html)
| `-cov`=nnn | [require at least `nnn`% code coverage](./opt_coverage.html)
| `-deps` | [print module dependencies (verbose)](./opt_deps.html)
| `-deps`=filename | [write module dependencies to `filename` (only imports)](./opt_deps.html)
| `-map` | [generate linker .map file](./opt_map.html)
| `-profile` | [profile runtime performance of generated code](./opt_profile.html)
| `-profile`=gc | [profile runtime allocations](./opt_profile.html)
| `-vgc` | [list all gc allocations including hidden ones](./opt_gc_alloc.html)
| `-vtls` | [list all variables going into thread local storage](./opt_thread_local.html)

Why is there no option where to put the map file? Like the options for generating documentation.

unit test blocks http://dlang.org/changelog/2.068.0.html#lex-only-unittest
