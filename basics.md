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

The following provides very brief and simplified explanation of each translation phase.

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
At this point, the program is basically executable.
In fact, this is how interpreters run programs.
The reference compiler has an option to do exactly that.
The next phase is an optional step which requires telling the compiler that you explicitly want the next step to be performed.

##### Optimization

Optimization is an optional process.
The compiler must be told explicitly that this step must be performed.
This is necessary because this process is a resource intensive operation.
The compiler will analyze the entire program and implement the fastest and most efficient way that the program can run.
The program is rewritten very efficiently without making any unintentional side effect.

##### Code Generation

Code generation is where the optimized or unoptimized code is translated into machine instructions for a target machine architecture [^machine architecture].
The result can then be fed into a linker.

##### Sections

{% include reference_dlang_section_links.html %}

[^sourcecode]: Program text file is also called or referred to as source file, source code file or source code. A program text file is usually written in a programming language that is fed into a compatible compiler.
[^compiler]: A compiler is commonly an executable program that does program compilation.
[^linker]: A linker is an executable program that converts the output of the compilation process into an executable file or a library file. Binary executable files are also called programs, executable files, applications, application files or shortly referred to as apps. Binary library files are special binary files in that they are used as building blocks for other libraries or executable files.
[^machine architecture]: In this context, machine architecture refers to the design, implementation and instruction sets of a processor. A few examples are x86, ARM, Alpha, Itanium, PowerPC and RISC.