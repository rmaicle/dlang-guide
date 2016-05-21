---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

The D programming language reference compiler is __Digital Mars D__ commonly known by its acronym __DMD__.
It can be downloaded from http://dlang.org/download.html.
There are also other D compiler implementations like _GDC_ and _LDC_.
Links to the other implementations can be found in the download page above.

###### Filenames
Filenames are either treated as case sensitive or not depending on the platform you are in.
_Microsoft Windows_ filenames are case insensitive. _Linux_ and _Mac OS_ filenames are case sensitive.
However, it has been good practice not to rely on filename case sensitivity when dealing with multi-platform projects.
Passing multiple filenames to the compiler requires that they be separated by a space character.

###### Options
Options cannot be 'combined'.
Each option is specified and separated by a space character.
Options are case sensitive, meaning `-d` and `-D` are treated differently.
You can specify different options in any order.
If conflicting options are encountered, the last parsed option takes precedence (ex. dmd test.d -m32 -m64 builds test.d in 64-bit architecture).
Specifying the same option multiple times, as in the case of Import Path (`-Ipath`) option, will treat the search order of the paths as they are specified.

###### Reference Compiler Command-line Syntax

The Digital Mars Compiler has the following command-line syntax:

<div markdown='1' class='syntax'>
    dmd files [...] [@cmdfile] [option [...]]

`files [...]`
: Could be one or more of the following separated by space:

  * D source files; with or without .d extension name
  * Ddoc files; .dd
  * D interface files; .di
  * Object files to link in; .o
  * Object code libraries to search; .a
  
`@cmdfile`
: A command file is a text file where the compiler reads _commands_ from and uses those commands to compile the specified D source file(s).

`option [...]`
: One or more _options_ passed to the compiler to perform specific actions.
</div>

Here is the list of all Digital Mars D (DMD) compiler options.
This table is a reproduction of the actual output of the command `dmd --help`.

| Option | Description | Topic |
|--------|-------------|-------|
| `-allinst` | [generate code for all template instantiations](./opt_allinst.html) | [Code Generation]
| `-boundscheck`=on | [turns on bounds checking](./opt_bounds_checking.html) | [Code Generation]
| `-boundscheck`=safeonly | [turns on bounds checking for `@safe` code only](./opt_bounds_checking.html) | [Code Generation]
| `-boundscheck`=off | [disable bounds checking](./opt_bounds_checking.html) | [Code Generation]
| `-c` | [compile only, do not link](./opt_compile.html) | [Compilation]
| `-color`=on | [force colored console output](./opt_color.html) | [Console]
| `-color`=off | [no colored console output](./opt_color.html) | [Console]
| `-conf`=path | [use config file at `path`](./opt_config.html) | [Compilation]
| `-cov` | [do code coverage analysis](./opt_coverage.html) | [Diagnostic]
| `-cov`=nnn | [require at least `nnn`% code coverage](./opt_coverage.html) | [Diagnostic]
| `-D` | [generate documentation](./opt_documentation.html) | [Documentation]
| `-Dd`path | [write documentation file to `path`](./opt_documentation.html) | [Documentation]
| `-Df`filename | [write documentation to `filename`](./opt_documentation.html) | [Documentation]
| `-d` | [silently allow deprecated features](./opt_deprecate.html) | [Compilation]
| `-dw` | [deprecated features as warnings (default)](./opt_deprecate.html) | [Compilation]
| `-de` | [deprecated features as errors (halt compilation)](./opt_deprecate.html) | [Compilation]
| `-debug` | [compile in debug code](./opt_debug.html) | [Compilation]
| `-debug`=level | [compile in debug code <= `level`](./opt_debug.html) | [Compilation]
| `-debug`=ident | [compile in debug code identified by `ident`](./opt_debug.html) | [Compilation]
| `-debuglib`=name | [set symbolic debug library to `name`](./opt_library.html) | [Compilation]
| `-defaultlib`=name | [set default library to `name`](./opt_library.html) | [Compilation]
| `-deps` | [print module dependencies (verbose)](./opt_deps.html) | [Diagnostic]
| `-deps`=filename | [write module dependencies to `filename` (only imports)](./opt_deps.html) | [Diagnostic]
| `-fPIC` | [generate position independent code](./opt_shared.html) | [Code Generation]
| `-dip25` | implement http://wiki.dlang.org/DIP25 (experimental) |
| `-g` | [add symbolic debug info](./opt_debug_info.html) | [Code Generation]
| `-gc` | [add symbolic debug info, optimize for non D debuggers](./opt_debug_info.html) | [Code Generation]
| `-gs` | [always emit stack frame](./opt_stack.html) | [Code Generation]
| `-gx` | [add stack stomp code](./opt_stack.html) | [Code Generation]
| `-H` | [generate _header_ file](./opt_header.html) | [Intermediate]
| `-Hd`path | [write _header_ file to `path`](./opt_header.html) | [Intermediate]
| `-Hf`filename | [write _header_ file to `filename`](./opt_header.html) | [Intermediate]
| `--help` | [display compiler arguments and options](./opt_help.html) | [Information]
| `-I`path | [`path` where to look for imports](./opt_import.html) | [Compilation]
| `-ignore` | [ignore unsupported pragmas](./opt_pragma.html) | [Compilation]
| `-inline` | [do function inlining](./opt_inline.html) | [Code Generation]
| `-J`path | [`path` where to look for string imports](./opt_import.html) | [Compilation]
| `-L`linkerflag | [pass `linkerflag` to linker](./opt_linker.html) | [Compilation]
| `-lib` | [generate library rather than object files](.opt_lib.html) | [Code Generation]
| `-m32` | [generate 32-bit code](./opt_architecture.html) | [Code Generation]
| `-m64` | [generate 64-bit code](./opt_architecture.html) | [Code Generation]
| `-main` | [add default main() (e.g. for unittesting)](./opt_main.html) | [Code Generation]
| `-man` | [open web browser on manual page](./opt_man.html) | [Information]
| `-map` | [generate linker .map file](./opt_map.html) | [Diagnostic]
| `-O` | [generate optimized code](./opt_optimize.html) | [Code Generation]
| `-o-` | [do not write object file](./opt_object.html) | [Intermediate]
| `-od`path | [write object & library files to `path`](./opt_object.html) | [Intermediate]
| `-of`filename | [name output file to `filename`](./opt_object.html) | [Intermediate]
| `-op` | [preserve source path for output files](./opt_object.html) | [Intermediate]
| `-profile` | [profile runtime performance of generated code](./opt_profile.html) | [Diagnostic]
| `-profile`=gc | [profile runtime allocations](./opt_profile.html) | [Diagnostic]
| `-release` | [compile release version](./opt_release.html) | [Compilation]
| `-run` <srcfile> [args...] | [run resulting program, passing args](./opt_run.html) | [Compilation]
| `-shared` | [generate shared library](./opt_shared.html) | [Code Generation]
| `-transition`=id | show info about language changes identified by `id` | [Information]
| `-transition`=? | list all language changes | [Information]
| `-unittest` | [compile in unit tests](./opt_unit_test.html) | [Compilation]
| `-v` | [verbose](./opt_verbose.html) | [Console]
| `-vcolumns` | [print character (column) numbers in diagnostics](./opt_column.html) | [Console]
| `-verrors`=num | [limit the number of error messages (0 means unlimited)](./opt_errors.html) | [Console]
| `-vgc` | [list all gc allocations including hidden ones](./opt_gc_alloc.html) | [Diagnostic]
| `-vtls` | [list all variables going into thread local storage](./opt_thread_local.html) | [Diagnostic]
| `--version` | [display compiler version](./opt_version.html) | [Information]
| `-version`=level | [compile in version code >= `level`](./opt_version_id.html) | [Compilation]
| `-version`=ident | [compile in version code identified by `ident`](./opt_version_id.html) | [Compilation]
| `-w` | [warnings as errors (compilation will halt)](./opt_warnings.html) | [Compilation]
| `-wi` | [warnings as messages (compilation will continue)](./opt_warnings.html) | [Compilation]
| `-X` | [generate JSON file](./opt_json.html) | [Intermediate]
| `-Xf`filename | [write JSON to `filename`](./opt_json.html) | [Intermediate]

##### Sections
{% include reference_dlang_section_links.html %}

[Code Generation]: ./codegen.html
[Compilation]: ./compilation.html
[Console]: ./console.html
[Documentation]: ./documentation.html
[Diagnostic]: ./diagnostic.html
[Information]: ./info.html
[Intermediate]: ./intermediate.html