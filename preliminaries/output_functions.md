---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Preliminaries
section: Output Functions
excerpt: write, writeln, writef and writefln functions
group: DLang
tags: [dlang, dguide, draft]
---

It is common to send output to the console and D has _write_ functions from its standard library.
The write functions have four (4) variations:

| Function | Description |
|----------|-------------|
| write    | writes all evaluated arguments to console |
| writeln  | writes all evaluated arguments to console and a new line |
| writef   | format output arguments and writes all evaluated arguments to the console |
| writefln | format output arguments and writes all evaluated arguments to the console and a new line |

The following describes the functions in the simplest way to provide the basic information on how it is used.
Note that function calls are terminated with a _semicolon_ as all D language statements should.
The basic syntax of the write functions is:

{% highlight text %}
write[f][ln]([format,] [parameter...]);
{% endhighlight %}

* All enclosed in square brackets are optional.
* _format_ is used for the formatted output variation of the function.
* _parameter_ is any literal, variable or expression.
* _..._ more than one parameter can be passed to the function provided they are separated by a _comma_.

###### write and writeln Functions

The `write` and `writeln` functions are almost the same.
They both accept any number of parameters to evaluate and send the output to the console.
The difference is that `writeln` appends a new line at the end of the output.
The example below sends 'texts' or string of characters (or simply _strings_) to the console.

{% highlight d linenos %}
{% include_relative write_function.ds %}
{% endhighlight %}

* _Line 1_ calls `write` with one (1) parameter and sends it to the output.
* _Line 2_ calls `write` with three (3) parameters and sends them all to the output on the same line as the previous call to `write`.
* _Line 3_ calls `writeln` without a parameter. Sends a new line character to the output.
* _Line 4_ calls `writeln` with one (1) parameter and sends it to the output on a new line (because of Line 3) and then sends a new line character to the output.
* _Line 5_ calls `writeln` with three (3) parameters and sends them all to the output on a new line and then sends a new line character to the output.

The code above will have the following output.

{% highlight console linenos %}
Hello world!Hello world again!
Hello world!
Hello world again!
{% endhighlight %}

###### writef and writefln Functions

These functions are cousins of the `write` functions above except that the `writef` functions requires a _format string_ as the first parameter.
The format string is used to format the output.
The format string has more details but for simplicity the entire format string syntax will not be discussed here.

    writef(format_string, [parameter]...);

The format string _can_ contain what is called _format specifiers_.
Let us repeat that.
Format strings can have or not have _format specifiers_.
Here is an example showing that.

{% highlight d linenos %}
{% include_relative writef_function1.ds %}
{% endhighlight %}

The compiler recognizes a format specifier when it encounters a percent (`%`) sign that follows the format specifier syntax below.
The format specifier controls how the output is composed and formatted.

For now, the most common format specifier will be used (`%s`) which simply says, just put the parameter output here.
The simplest rule is that the number of parameters must be equal to the number of format specifiers.
Here are a few examples:

{% highlight d linenos %}
{% include_relative writef_function2.ds %}
{% endhighlight %}

Let us see that column-like output using the `wrietfln`.

{% highlight d linenos %}
{% include_relative writefln_function.ds %}
{% endhighlight %}

Here is the output:

{% highlight console linenos %}
12345678901234567890
        Hello world!
                 100
Hello world!         2
100                  2
{% endhighlight %}

Let us dissect what happened.

* _Line 2_: %20s specifier means 20 characters wide (width) and right-aligned of type string. The padding is computed as the width less the length of the parameter which is the length of the string 'Hello world!' or 12. The padding is applied as a prefix to the parameter. Therefore, the padding is 20 less 12 or 8 spaces.
* _Line 3_: %20s specifier means 20 characters wide (width) and right-aligned of type decimal. The rest of the operation is the same as Line 2.
* _Line 4_: %-20s specifier means 20 characters wide (width) and left-aligned (-) of type string, space and decimal. The padding is computed the same but applied as a suffix to the first parameter which is the string 'Hello world!'. Then a space is sent to the output, then the decimal number 2.
* _Line 5_: %-20s specifier means 20 characters wide (width) and left-aligned (-) of type decimal, space and decimal. The rest is the same as Line 4.

{% comment %}
###### Format Specifier

Just for completeness here is the complete syntax of a format specifier.
Items in square brackets are _optional_.

    %[flags][width][precision]format_character
    
* _flags_ are formatting features that can be turned on or off.
* _width_ is the number of characters withi which the parameter is to be displayed.
The parameter is either padded with spaces or not if the width is not specified.
The sign determines how padding is applied.
A negative sign means to align the output to the left and a positive sign means to align the output to the right.
This is primarily used in displaying column-like output.
* _precision_ is for floating-point types that control the number of digits to be displayed after the decimal point.
* _format_character_ is a letter that tells what kind of parameter is concerned.
The following format characters are the most common ones and will be used here.
{% endcomment %}
