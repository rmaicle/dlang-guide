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
| writeln  | same as above but sends a new line character after the last parameter |
| writef   | format output arguments and writes all evaluated arguments to the console |
| writefln | same as above but sends a new line character after the last parameter |

The basic syntax of the write functions is:

{% highlight text %}
write[f][ln]([format,] [parameter...]);
{% endhighlight %}

* items inside square brackets are optional.
* _format_ is used for the formatted output variation of the function.
* _parameter_ is any literal, variable or expression.
* _..._ more than one parameter can be passed to the function provided they are separated by a _comma_.
* function calls are terminated with a _semicolon_.

##### write and writeln Functions

The `write` and `writeln` functions both accept any number of parameters to send to the output.
The difference is that `writeln` appends a new line after the last parameter.
The example below sends texts or string of characters (or simply _strings_) to the console.

{% highlight d linenos %}
{% include_relative write_function.ds %}
{% endhighlight %}

The code above will have the following output.

{% highlight console linenos %}
firstsecond third fourth
first
second third fourth
last
{% endhighlight %}

##### writef and writefln Functions

The `writef` and `writefln` functions both accept any number of parameters to send to the output but accepts a _format string_ as the first parameter.
A format string tells the function how to format the output or something like a template to follow.

    writef(format_string, [parameter]...);

A format string _can_ have _escape sequences_ and _format specifiers_.

###### Escape Sequences

For simplicity, escape sequences are sequences of characters used to perform special actions or append special characters.
Escape sequences begin with a backslash character (`\`).
Here are the most common escape sequences:

| Escape Sequence | Description |
|:---------------:|-------------|
| \n              | Add a new line character. This is the same as calling the `writeln` function. |
| \'              | Add a single quote character. |
| \"              | Add a double quote character. This is typically used to 'quote' something inside a string. Because strings are written inside double quotes, there must be a way to place a double quote inside the string without terminating or ending the string. This scenario will be shown in an example. |
| \\\             | Add a backslash character. Because escape sequences start with a backslash character, there must be a way to add a backslash character in a string. |

###### Format Specifiers

Format specifiers are a sequence of characters that describes how a parameter is to be displayed.
Format specifiers begin with a percent character (`%`).
Here is the syntax for format specifiers although the simplest forms will be used in examples.

    %[flags][width][precision]format_character

* _flags_ are formatting features that can be turned on or off.
* _width_ is the number of characters withi which the parameter is to be displayed.
The parameter is either padded with spaces or not if the width is not specified.
The sign determines how padding is applied.
A negative sign means to align the output to the left and a positive sign means to align the output to the right.
This is primarily used in displaying column-like output.
* _precision_ is for floating-point types that control the number of digits to be displayed after the decimal point.
* _format_character_ is a letter that tells what kind of parameter is concerned.

Here are the most common flags:

| Flags | Descriptionn |
|:-----:|--------------|
| -     | Left align |
| +     | Prefix positive numbers with a plus character |
| 0     | Prefix numbers with zeroes |
| ' '   | Prefix with spaces |


Here are the most common format characters:

| Format Specifier | Descriptionn |
|:----------------:|--------------|
| s               | Default format specifier. Converts the parameter to a string representation. |
| d               | Parameter is an integral type and formatted as an integer. |
| f               | Parameter is a floating point type and formatted in decimal notation. |

###### Using writef and writefln Functions

Formatted output discussion can span an entire chapter but we need only the basics now.
One way to explain formatted output is through examples.

First how the functions are used:

{% highlight d linenos %}
{% include_relative writef_function1.ds %}
{% endhighlight %}

As mentioned above, format specifiers begin with a percent character (`%`).
Here is an example showing the use of format specifiers.

{% highlight d linenos %}
{% include_relative writef_function2.ds %}
{% endhighlight %}

Output:

{% highlight console linenos %}
first
100
100
-100
+100
second 100
third-100
{% endhighlight %}

Here is an example using the _width_ format specifier, specifically width value is ten (10).
The period character is used as _terminators_ to show the start and the end of the output.

{% highlight d linenos %}
{% include_relative writef_function3.ds %}
{% endhighlight %}

Output:

{% highlight console linenos %}
123456789012
0000000100
       100
-000000100
+000000100
      +100
     first
    second
.       aaa.
.bbb       .
.       ccc.
{% endhighlight %}
