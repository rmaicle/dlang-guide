---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Output Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

| Category | Options |
|----------|:--------|
| Warnings | -__w__[__i__] &nbsp; Options on how warnings are reported. <p>Treat warnings as errors [-_w_] and compilation halts on error. Or treat warnings as ordinary message [-_wi_] and compilation proceeds when a warning is encountered.</p> |
| Console | -__color__[=__on__&nbsp;&#124;&nbsp;__off__] &nbsp; Force a colored or uncolored console output. <p>Options:</p> <ul><li>_on_ forces colored console output if it is supported. Equivalent to -_color_.</li><li>_off_ forces a non-colored console output (default).</li></ul> |
|         | -__quiet__&nbsp;&#124;&nbsp;-__v__ \(lowercase v\) &nbsp; Amount or quality of compiler output messages. <p>Suppress non-essential compiler output [-_quiet_] or verbose output [-_v_].
|         | -__vcolumns__ &nbsp; Column number display in diagnostic messages. <p>Display the column number in diagnostic messages. If this option is not used (default) the diagnostic messages display only the line number after the filename.</p> |
