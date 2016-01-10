---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: rdmd
excerpt: Reference compiler Digital Mars D tool
group: DLang
tags: [dlang, dguide, draft]
---

> [rdmd](http://dlang.org/rdmd.html) is a companion to the dmd compiler that simplifies the typical edit-compile-link-run or edit-make-run cycle to a rapid edit-run cycle.
> Like make and other tools, rdmd uses the relative dates of the files involved to minimize the amount of work necessary.
> Unlike make, rdmd tracks dependencies and freshness without requiring additional information from the user.
> 
> * shields its user from the notion that producing a running program from D programming language files may entail several concerted steps against different source files producing various intermediate files;
> * automatically infers and builds dependent files, transitively, by following import directives;
> * recognizes and passes down all of dmd's command-line options;
> * understands how various dmd compiler options (e.g. -release vs. -debug) affect generation of intermediate files, and avoids conflations (e.g., does not unwittingly run a debug executable when the release executable is asked for);
> * recompiles files only on a needed basis, e.g. two invocations of rdmd in sequence without an intervening change to any relevant source file does not produce the executable again.

##### Syntax

        #!/usr/bin/rdmd --shebang [arg(s)]

##### Usage

rdmd [dmd and rdmd options] progfile[.d] [program arguments]

In addition to dmd's options, rdmd recognizes the following options:

| Option       | Description |
|--------------|-------------|
| `--build-only` | just build the executable, don't run it
| `--chatty` | write dmd commands to stdout before executing them
| `--compiler`=path_to_compiler | use the specified compiler (e.g. gdmd) instead of dmd
| `--dry-run` | do not compile, just show what commands would be run (implies --chatty)
| `--eval`=code | evaluate code including it in void main(char[][] args) { ... } (multiple --eval allowed, will be evaluated in turn)
| `--exclude`=package | exclude a package from the build (multiple --exclude allowed)
| `--force` | force a rebuild even if apparently not necessary
| `--help` | show a help message and exit
| `--loop`=code | like --eval, but code will be additionally included in a loop foreach (line; stdin.byLine()) { ... }
| `--main` | add an empty void main() {} function (useful for running unittests)
| `--makedepend` | print dependencies in makefile format and exit
| `--man` | open web browser on manual page
| `--shebang` | rdmd is in a shebang line (put as first argument)
