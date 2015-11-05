---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basics
section: Script Line
excerpt: Script execution
group: DLang
tags: [dlang, dguide, draft]
---

The first source text character of an ASCII text file is the character at offset 0x00.
The first source text character of a Unicode text file is the character after the _Byte Order Mark_ (BOM).
If the first two source text characters are the hash (`#`) and exclamation (`!`) characters then the rest of the line is ignored.

| Name    | Unicode          | ASCII           | Char   |
|---------|------------------|-----------------|:------:|
| Shebang | U+0023 + U+0021  | 35+33 0x23+0x21 |  #!  |

The _shebang_ character sequence in Unix-like operating systems is generally used to run a script.
The _shebang_ interpreter/script directive syntax is shown below. Note that `script` must include the absolute path.

    #!script [optional-arg]

In D, this can be used to execute a D program.
Although, of course some extra work is required.
The example D source file (`hello.d`) below illustrates the use of the _shebang_.

{% highlight d linenos %}
{%raw%}#{%endraw%}!/usr/bin/dmd -run
import std.stdio;
void main() {
    writeln("Hello, world!");
}
{% endhighlight %}

To be able to make this file executable, it is required in Unix-like machines to change the access permissions to the file and make it executable.
The command to do that is `chmod` and is shown below how to accomplish that.

    $ chmod u+x hello.d
    
The arguments `u+x` tells `chmod` to make the owner of the file to have execute permission on `hello.d`.
Once done, typing the following in the command-line will run the file as if it has been compiled.

    $ ./hello.d
    Hello, world!

Follow this link to learn more about [compiler command-line options](/dlang-guide/compiler.html).
