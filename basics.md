---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basics
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

{% comment %}
This chapter introduces the reader to the basics of compilations processes and the language lexical tokens.
{% endcomment %}

Compilation [^compiler] is the process converting or translating a program text file [^sourcecode] into a binary file which is fed to a linker. [^linker]
Program compilation is a multi-step process or sometimes called translaton phases.
These translation phases are big topics on their own and are subjects in active research.

The following are very brief and simplified explanation of each translation phase.
The output of each translation phase is the input to the next.

##### Lexical Analysis

Lexical means 'pertaining to words'.
In programming languages, the term 'words' also known as tokens refer to the basic components of the language.
These tokens can be identifiers, literals, keywords and special tokens.
The lexical analyzer scans the program text file for these tokens and extracts them and then fed to the syntax analyzer.

##### Syntax Analysis

Syntax analysis, also known as parsing, is the process of converting the tokens into a data structure efficiently suited for fast and easy analysis.
This structure is called a syntax tree.
From this syntax tree, the syntax analyzer can analyze whether the program conforms to the language grammar specification.
If something in the input does not conform to the language grammar then a 'syntax error' occurs.
Otherwise, the syntax-validated tokens are fed to the semantic analyzer.

##### Semantic Analysis

Semantic analysis analyses the tokens from the syntax tree and determine their meaning.
At this stage, the program can be executed.
Although commonly it is fed to an optional phase called optimization phase.

##### Optimization

Optimization is a where the program is rewritten in a way that the unoptimized and optimized program is semantically equivalent.
The main purpose of rewriting the program is to optimize it which oftentimes translates to making it execute faster.

##### Code Generation

Code generation is where the optimized or unoptimized code is translated into machine instructions for a target machine architecture [^machine architecture].
The result can then be fed into a linker.

##### Sections

{% include reference_dlang_section_links.html %}

[^sourcecode]: Program text file is also called or referred to as source file, source code file or source code. A program text file is usually written in a programming language that is fed into a compatible compiler.
[^compiler]: A compiler is commonly an executable program that does program compilation.
[^linker]: A linker is an executable program that converts the output of the compilation process into an executable file or a library file. Binary executable files are also called programs, executable files, applications, application files or shortly referred to as apps. Binary library files are special binary files in that they are used as building blocks for other libraries or executable files.
[^machine architecture]: In this context, machine architecture refers to the design, implementation and instruction sets of a processor. A few examples are x86, ARM, Alpha, Itanium, PowerPC and RISC.
