---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Compilation Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

| Option | Description |
|--------|-------------|
| `-c` | [compile only, do not link](./opt_compile.html)
| `-conf`=path | [use config file at `path`](./opt_config.html)
| `-d` | [silently allow deprecated features](./opt_deprecate.html)
| `-dw` | [deprecated features as warnings (default)](./opt_deprecate.html)
| `-de` | [deprecated features as errors (halt compilation)](./opt_deprecate.html)
| `-debug` | [compile in debug code](./opt_debug.html)
| `-debug`=level | [compile in debug code <= `level`](./opt_debug.html)
| `-debug`=ident | [compile in debug code identified by `ident`](./opt_debug.html)
| `-debuglib`=name | [set symbolic debug library to `name`](./opt_library.html)
| `-defaultlib`=name | [set default library to `name`](./opt_library.html)
| `-Ipath` | [`path` where to look for imports](./opt_import.html)
| `-ignore` | [ignore unsupported pragmas](./opt_pragma.html)
| `-Jpath` | [`path` where to look for string imports](./opt_import.html)
| `-Llinkerflag` | [pass `linkerflag` to linker](./opt_linker.html)
| `-release` | [compile release version](./opt_release.html)
| `-run` <srcfile> [args...] | [run resulting program, passing args](./opt_run.html)
| `-unittest` | [compile in unit tests](./opt_unit_test.html)
| `-version`=level | [compile in version code >= `level`](./opt_version_id.html)
| `-version`=ident | [compile in version code identified by `ident`](./opt_version_id.html)
| `-w` | [warnings as errors (compilation will halt)](./opt_warnings.html)
| `-wi` | [warnings as messages (compilation will continue)](./opt_warnings.html)
