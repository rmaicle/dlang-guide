---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basics
section: Script Line
excerpt: Script execution
group: DLang
tags: [dlang, dguide, draft]
---

If the first two text characters in the file are the hash (`#`) and exclamation (`!`) characters, the line is treated as a _script line_.
(See the [Source Text section](source_text.html) for a brief description of accepted source files.)

| Name    | Unicode          | ASCII   | Hexadecimal   | Char   |
|---------|------------------|---------|---------------|:------:|
| Shebang | U+0023 + U+0021  | 35 + 33 | 0x23 + 0x21   | #!  |

The _shebang_ character sequence in the first line of a file in Unix-like operating systems is generally used to run a script.
This is an alternative way of running a D source file in Unix-like operating systems.

##### Syntax

The _shebang_ interpreter/script directive syntax is shown below.

    #!interpreter [arg(s)]

| Item        | Description |
|:-----------:|-------------|
| interpreter | interpreter name must not contain spaces and must include the absolute path (the environment `$PATH` variable is not searched for the location of _interpreter_) |
| arg(s)      | optional arguments |

There are two (2) ways to use the script line to execute a D source file.
The first one is simple but limited, the second is a more capable modern alternative.
    
##### Run the Source File Using dmd -run
    
The example D source file (`hello.d`) below shows the script line using `dmd -run`.

{% highlight d linenos %}
{%raw%}#{%endraw%}!/usr/bin/dmd -run
import std.stdio;

void main()
{
    debug writeln("(debug)");   // this line is not sent to the output
    writeln("Hello, world!");
}
{% endhighlight %}

One major limitation using this is that no other compiler option can be used.
You cannot, for example, pass a debug option so the code is always executed in release build.
Because of that, only one source file can be compiled and executed.
Importing other source files other than the standard library is not possible.
This is mainly the issue with the _shebang_ which treats all the arguments as one single argument.

If the source you are going to execute is a simple, one-file program then this is one possible way to do it.

##### Run the Source File Using rdmd --shebang

Using `rdmd --shebang` in the script line solves the limitations of `dmd -run` and more.
For more information see the [`rdmd` chapter](/dlang-guide/rdmd.html).

Here is an example that imports another D source file and runs the source files in _debug_ build.
The first source file argument must be the file that contains the program entry point otherwise the compiler will report an `undefined reference to 'main' error`.
The code below is the content of the file `hello.d`.

{% highlight d linenos %}
{%raw%}#{%endraw%}!/usr/bin/rdmd --shebang -debug hello.d hello_import.d
import std.stdio;
import hello_import;

void main(string[] args)
{
    debug writeln("(debug)");   // this line IS sent to the output
    writeln("Hello, world!");
    from_import();              // defined in hello_import.d
}
{% endhighlight %}

Using `rdmd` has a lot to offer and is by far a better alternative to run a D source file using the script line.
 
##### Make the Source File Executable

To make a D source file with script line an executable file, it is required in Unix-like machines to change the access permissions to the file using `chmod`.
The following shows how to use `chmod` and make the D source file an executable file.

    $ chmod u+x <source>
    
The arguments `u+x` tells `chmod` to make the owner of the file `source` to have execute permission.
Once done, the following command-line will run (execute) the file as if it is an executable binary file.

    $ ./<source>


    
{% comment %}

| Script Line                        | Description |
|------------------------------------|-------------|
| #!/usr/bin/dmd -run                | simple and limited (old way) |
| #!/usr/bin/rdmd --shebang [arg(s)] | adds more capabilities (new way) |

Here are some of the limitations using `dmd -run` in the script line:

* Using the script line does not allow passing any other arguments to the compiler other than the `-run` argument.
Also, it does not allow passing arguments to the program.

* Always execute release build.
This is the same as if the `-release` option is passed to the compiler.

###### Note on Compilation

The compiler does not produce an object or any intermediate file for `hello.d`.
Everything happens in memory.
This was mentioned in the description of _Semantic Analysis_ in the _Basics_ chapter backround on the compilation processes.
{% endcomment %}

