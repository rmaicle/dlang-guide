---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Code Generation Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

| Option | Description |
|--------|-------------|
| `-allinst` | [generate code for all template instantiations](./opt_allinst.html)
| `-boundscheck`=on | [turns on bounds checking](./opt_bounds_checking.html)
| `-boundscheck`=safeonly | [turns on bounds checking for `@safe` code only](./opt_bounds_checking.html)
| `-boundscheck`=off | [disable bounds checking](./opt_bounds_checking.html)
| `-fPIC` | [generate position independent code](./opt_shared.html)
| `-dip25` | implement http://wiki.dlang.org/DIP25 (experimental)
| `-g` | [add symbolic debug info](./opt_debug_info.html)
| `-gc` | [add symbolic debug info, optimize for non D debuggers](./opt_debug_info.html)
| `-gs` | [always emit stack frame](./opt_stack.html)
| `-gx` | [add stack stomp code](./opt_stack.html)
| `-inline` | [do function inlining](./opt_inline.html)
| `-lib` | [generate library rather than object files](.opt_lib.html)
| `-m32` | [generate 32-bit code](./opt_architecture.html)
| `-m64` | [generate 64-bit code](./opt_architecture.html)
| `-main` | [add default main() (e.g. for unittesting)](./opt_main.html)
| `-O` | [generate optimized code](./opt_optimize.html)
| `-shared` | [generate shared library](./opt_shared.html)