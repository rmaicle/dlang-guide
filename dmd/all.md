---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: All Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

Here is the list of all Digital Mars D (DMD) compiler options.
This table is a reproduction of the actual output of the command `dmd --help`.

| Option | Description |
|--------|-------------|
| `-allinst` | generate code for all template instantiations |
| `-boundscheck`=[on&#124;safeonly&#124;off] | bounds checks on, in @safe only, or off |
| `-c` | do not link |
| `-color`=[on&#124;off] | force colored console output on or off |
| `-conf`=path | use config file at path |
| `-cov` | do code coverage analysis |
| `-cov`=nnn | require at least nnn% code coverage |
| `-D` | generate documentation |
| `-Dd`docdir | write documentation file to docdir directory |
| `-Df`filename | write documentation file to filename |
| `-d` | silently allow deprecated features |
| `-dw` | show use of deprecated features as warnings (default) |
| `-de` | show use of deprecated features as errors (halt compilation) |
| `-debug` | compile in debug code |
| `-debug`=level | compile in debug code <= level |
| `-debug`=ident | compile in debug code identified by ident |
| `-debuglib`=name | set symbolic debug library to name |
| `-defaultlib`=name | set default library to name |
| `-deps` | print module dependencies (imports/file/version/debug/lib) |
| `-deps`=filename | write module dependencies to filename (only imports) |
| `-fPIC` | generate position independent code |
| `-dip25` | implement http://wiki.dlang.org/DIP25 (experimental) |
| `-g` | add symbolic debug info |
| `-gc` | add symbolic debug info, optimize for non D debuggers |
| `-gs` | always emit stack frame |
| `-gx` | add stack stomp code |
| `-H` | generate 'header' file |
| `-Hddirectory` | write 'header' file to directory |
| `-Hffilename` | write 'header' file to filename |
| `--help` | print help and exit |
| `-Ipath` | where to look for imports |
| `-ignore` | ignore unsupported pragmas |
| `-inline` | do function inlining |
| `-Jpath` | where to look for string imports |
| `-Llinkerflag` | pass linkerflag to link |
| `-lib` | generate library rather than object files |
| `-m32` | generate 32 bit code |
| `-m64` | generate 64 bit code |
| `-main` | add default main() (e.g. for unittesting) |
| `-man` | open web browser on manual page |
| `-map` | generate linker .map file |
| `-O` | optimize |
| `-o-` | do not write object file |
| `-odobjdir` | write object & library files to directory objdir |
| `-offilename` | name output file to filename |
| `-op` | preserve source path for output files |
| `-profile` | profile runtime performance of generated code |
| `-profile`=gc | profile runtime allocations |
| `-property` | enforce property syntax |
| `-release` | compile release version |
| `-run` srcfile args... | run resulting program, passing args |
| `-shared` | generate shared library (DLL) |
| `-transition`=id | show additional info about language change identified by 'id' |
| `-transition`=? | list all language changes |
| `-unittest` | compile in unit tests |
| `-v` | verbose |
| `-vcolumns` | print character (column) numbers in diagnostics |
| `-verrors`=num | limit the number of error messages (0 means unlimited) |
| `-vgc` | list all gc allocations including hidden ones |
| `-vtls` | list all variables going into thread local storage |
| `--version` | print compiler version and exit |
| `-version`=level | compile in version code >= level |
| `-version`=ident | compile in version code identified by ident |
| `-w` | warnings as errors (compilation will halt) |
| `-wi` | warnings as messages (compilation will continue) |
| `-X` | generate JSON file |
| `-Xffilename` | write JSON file to filename |