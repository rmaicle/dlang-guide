---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Common Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

| Category | Options |
|----------|:--------|
| Configuration | -__conf__=&lt;__path__&gt; &nbsp; Use configuration file at specified path. |
| General | -__allinst__ &nbsp; Generate code for all template instantiations. |
|         | -__boundscheck__=<__on__&nbsp;&#124;&nbsp;__safeonly__&nbsp;&#124;&nbsp;__off__> &nbsp; Bounds checking. <p>Options:</p> <ul><li>_on_ enables bounds checking. This is the default for debug builds.</li><li>_safeonly_ enables bounds checking in `@safe` code only. This is the default for release builds.</li><li>_off_ disables bounds checking in all code.</li> |
|         | -__c__ \(lowercase c\) &nbsp; Compile only. Do not link. |
|         | -__dip25__ &nbsp; Implement http://wiki.dlang.org/DIP25 (experimental). |
|         | -__gs__ &nbsp; Always emit stack frame. |
|         | -__gx__ &nbsp; Add stack stomp code. |
|         | -__ignore__ &nbsp; Ignore unsupported pragmas. |
|         | -__inline__ &nbsp; Do function inlining. |
|         | -__main__ &nbsp; Add default main() (e.g. for unittesting). |
| Imports | -__I__&lt;__path__&gt; \(uppercase i\) &nbsp; Specify path where compiler will look for imports. |
|         | -__J__&lt;__path__&gt;&nbsp;... &nbsp; Specify path where compiler will look for string imports. |
| Libraries | -__debuglib__=&lt;__name__&gt; &nbsp; Set symbolic debug library to _name_. |
|           | -__defaultlib__=&lt;__name__&gt; &nbsp; Set default library to _name_.|
| Library Type | -__shared__ [-__fPIC__] &nbsp; Create shared library. <p>Create as shared library [-_shared_] and optionally generate Position Independent Code [-_fPIC_]. Note that PIC is available on Linux only.</p> |
| Debug Info | -__g__[__c__] \(lowercase c\) &nbsp; Symbolic debug information. <p>Added symbolic debug information for D debuggers [-_g_]. Optionally, for non-D debuggers, use [-_gc_].</p> |
| Build | -__debug__[=&lt;__level__&nbsp;&#124;&nbsp;__identifier__&gt;]&nbsp;... &nbsp; Include `debug` code blocks. <p>Compile in `debug` code blocks that satisfy one or both conditions: <= _level_ and/or == _identifier_. Specifying [-_debug_] is equivalent to [-_debug_=1]. Multiple _levels_ and _identifiers_ may be set as in  [-_debug_=1 -_debug_=2 -_debug_=beta]\).</p> |
|       | -__release__ [-__O__] \(uppercase o\) &nbsp; Compile a release build. <p>Compile code for release build and optionally generate optimized code [-_O_]. Release versions do not include internal run-time checks for contracts and assertions; array bounds checking is not done for `@system` and `@trusted` functions. Assertion failures will result to undefined behaviour.</p> |
| Architecture | -__m__[__32__&nbsp;&#124;&nbsp;__64__] &nbsp; Generate target binary architecture. <p>Options:</p> <ul><li>-_m32_ generates 32-bit machine code (32-bit compiler default).</li><li>-_m64_ generates 64-bit machine code (64-bit compiler default).</li></ul> <p>Regardless of host architecture and compiler binary build, a 32-bit or a 64-bit machine code can be generated. Although, generating the target binary architecture requires a binary compatible `druntime`, `phobos` library and linker.</p> |
| Version | -__version__=&lt;__level__&nbsp;&#124;&nbsp;__identifier__&gt;&nbsp;... &nbsp; Include `version` code blocks. <p>Compile in `version` code blocks that satisfy one or both conditions: <= _level_ and/or == _identifier_. Multiple _levels_ and _identifiers_ may be set as in  [-_version_=1 -_version_=2 -_version_=beta]\).</p> |
| Deprecation | -__d__[__w__&nbsp;&#124;&nbsp;__e__] &nbsp; Control deprecated feature reporting. <p>Either silently allow deprecated features [-_d_], show them as warnings [-_dw_] or report as errors [-_de_]. See Output group about warnings and errors.</p> <p>Deprecated features include symbols with the `deprecated` attribute or symbols within `deprecated` code blocks.</p> |
| Linker | -__L__&lt;__linkerflag__&gt;&nbsp;... &nbsp; Pass _linkerflag_ to the linker. <p>Please see documentation of your linker program.</p> |
| Unit Test | -__unittest__ &nbsp; Include `unittest` code blocks. <p>Compile in unit test code blocks and incorporate them into the resulting executable. This option turns on asserts and defines the `unittest` version identifier.</p> |
| Run Program | -__run__ <__source__> [__arg__&nbsp;...] &nbsp; Execute resulting program. <p>If compilation is successful this executes the resulting program [-_run_ <_source_>]. Arguments to the program can be passed as command-line arguments [-_arg_&nbsp;...]. Compilation does not produce object or executable file.</p> |
| Documentation | -__D__[__d__&lt;__path__&gt;&nbsp;&#124;&nbsp;__f__&lt;__filename__&gt;] &nbsp; Generate documentation. <p>The documentation may be written to _filename_ [-_Df_&lt;_filename_&gt;]. The generated documentation file may optionally be written to _path_ [-_Dd_&lt;_path_&gt;].</p> |
