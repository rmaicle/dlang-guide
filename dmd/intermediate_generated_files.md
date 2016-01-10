---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Intermediate and Generated Files
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

| Category | Options |
|----------|:--------|
| Source Path | -__op__ &nbsp; Source path in output files. <p>Preserve the source path information for output files. Normally the path for `.d` source files is stripped off when generating an object, interface, or Ddoc file.</p> |
| Compiler Output | -__o__[__-__&nbsp;&#124;&nbsp;__d__&lt;__path__&gt;&nbsp;&#124;&nbsp;__f__&lt;__filename__&gt;] &nbsp; Object file generation. <p>Do not write object file or write the object file to _path_ [-_od_&lt;_path_&gt;] and name the object output file as _filename_ [-_of_&lt;_filename_&gt;]. By default, the compiler outputs the object file as source file with `.o` extesion.</p> |
|                 | -__lib__ [-__od__&lt;__path__&gt;] &nbsp; Library file generation. <p>Generate library file instead of object files  [-_lib_]. Optionally tell the compiler to write the library file to _path_ [-_od_&lt;_path_&gt;]. By default, the compiler outputs the library file as source file with `.a` extension.</p> |
| Interface File | -__H__[__d__&lt;__path__&gt;&nbsp;&#124;&nbsp;__f__&lt;__filename__&gt;] &nbsp; Interface ('header') file generation. <p>Generate interface file [-_H_]. The interface file may be written to _path_ [-_Hd_&lt;_path_&gt;] and set the interface file output as _filename_ [-_Hf_&lt;_filename_&gt;]. By default, the compiler outputs the interface file as source file with `.di` extension.</p> |
| JSON | -__X__[__f__&lt;__filename__&gt;] &nbsp; Generate JSON file. <p>Generate a JSON file [-_X_] and optionally name the file as _filename_ [-_Xf_&lt;_filename_&gt;]. By default, the compiler outputs the JSON file as source file with `.json` extension.</p> |
