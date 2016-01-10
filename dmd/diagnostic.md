---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Diagnostic Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

| Category | Options |
|----------|:--------|
| Map | -__map__ &nbsp; Generate linker .map file. |
| Coverage | -__cov__[=&lt;__nnn__&gt;] &nbsp; Code coverage analysis tool. <p>Compiling with [-_cov_] will embed code coverage analysis tool. Optionally, a minimum code coverage percentage _nnn_% can be specified [-_cov_=&lt;_nnn_&gt;]. Running the application will generate a `.lst` text file or an error if code coverage result did not reach the minimum code coverage.</p> |
| Profile | -__profile__[=__gc__] &nbsp; Compile in runtime performance profiling code. <p>Include runtime performance profiling code [-_profile_] and optionally include profiling of runtime memory allocations [-_profile_=_gc_] and writes a report to `profilegc.log` file.</p> |
| Garbage Collector Allocations | -__vgc__ &nbsp; List all Garbage Collector allocation points including hidden ones. Analysis will follow the semantics of the @nogc attribute. |
| Thread Local Storage | -__vtls__ &nbsp; List all variables going into thread local storage. |
| Transition | -__transition__=[__?__&nbsp;&#124;&nbsp;__identifier__] &nbsp; Language changes information. <p>Show addditional information about all language changes [-_transition_=_?_] or changes identified by _identifier_ [-_transition_=&lt;_identifier_&gt;].</p> |

Why is there no option where to put the map file? Like the options for generating documentation.

unit test blocks http://dlang.org/changelog/2.068.0.html#lex-only-unittest
