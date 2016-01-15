---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Preliminaries
section: Output Functions
excerpt: write, writeln, writef and writefln functions
group: DLang
tags: [dlang, dguide, draft]
---

The standard library defines four (4) variations of its output function.

| Function | Description |
|----------|-------------|
| write    | writes all evaluated arguments to console |
| writeln  | same as above but sends a new line character after the last parameter |
| writef   | format output arguments and writes all evaluated arguments to the console |
| writefln | same as above but sends a new line character after the last parameter |

##### Syntax

<div markdown='1' class='syntax'>

`write` and `writef` Functions

    write[ln] ([argument [, ...]);
    writef[ln]([formatstring,] [argument [, ...]);
    
`formatstring`
: Is used with `writef` and `writefln` functions.
  It may contain text, a format string or a combination of both.
  The format string has the following syntax:

  ~~~
  %[flags][width][precision]formatcharacter
  ~~~
  
  A formatstring begins with a percent `%` character.
    
  `flags`
  : The flags are formatting features that can be turned on or off.
    Here are the most common flags:

    | Flags | Description |
    |:-----:|--------------|
    | -     | Left align |
    | +     | Prefix numbers with a plus sign if positive and minus sign if negative |
    | 0     | Prefix numbers with zeroes |
    | ' '   | Prefix with spaces |
  
  `width`
  : The width is an optional numeric value that specifies the number of characters with which the argument is to be displayed.
    If the width is specified then the output is padded with zeroes or spaces.
  
  `precision`
  : The precision is an optional numeric value for displaying floating-point types.
    It controls the number of digits to be displayed after the decimal point.
  
  `formatcharacter`
  : The formatcharacter is a letter that tells what kind of argument is concerned.
    Here are the most common format characters:

    | Character | Descriptionn |
    |:----------------:|--------------|
    | s               | Default format specifier. Converts the argument to string. |
    | d               | Argument is an integral type and formatted as an integer. |
    | f               | Argument is a floating point type and formatted in decimal notation. |

`argument [, ...]`
: One or more arguments.
  An argument may be a literal, variable or expression.
  If the formatted function is used, the number of arguments passed must correspond to the number of arguments specified in te format string.

</div>

##### write and writeln Functions

The `write` and `writeln` functions both accept any number of parameters to send to the output.
The difference is that `writeln` appends a new line after the last parameter.
The example below sends texts or string of characters (or simply _strings_) to the console.

{% highlight d linenos %}
write("first");                         // 1st line
write("second", " third", " fourth");   // goes to 1st line
writeln();                              // new line
writeln("first");                       // goes to 2nd line, new line
writeln("second", " third", " forth");  // goes to 3rd line, new line
write("last");                          // goes to 4th line
{% endhighlight %}

The code above will have the following output.

{% highlight text linenos %}
firstsecond third fourth
first
second third fourth
last
{% endhighlight %}

##### writef and writefln Functions

The `writef` and `writefln` functions both accept any number of parameters to send to the output but accepts a _format string_ as the first parameter.
A format string tells the function how to format the output or something like a template to follow.
Formatted output discussion is lengthy but we need only the basics now.
One way to explain formatted output is through examples.

First how the functions are used:

{% highlight d linenos %}
writef("first");                        // send string 'first' to output
writefln("second");                     // send string 'second' to output
writef("third");                        // send string 'third' to output
{% endhighlight %}

And here is the output of the above code assuming it is in a file `writef.d`:

{% highlight text linenos %}
firstsecond
third
{% endhighlight %}

As mentioned above, format specifiers begin with a percent character (`%`).
Here are examples showing how to specify format specifiers.

{% highlight d linenos %}
writefln("%s", "first");                // send string 'first' to output
writefln("%s", 100);                    // send integer 100 to output
writefln("%d", 100);
writefln("%d", -100);                   // send integer -100 to output
writefln("%+d", 100);                   // send positive sign and integer 100 to output
writefln("%s %s", "second", 100);       // send string 'second', a space, and 100 to output
writefln("%s-%s", "third", 100);        // send string 'second', a dash, and 100 to output
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

Here are examples using the _width_ format specifier, specifically width value is ten (10).
The period character is used as _terminators_ to show the start and the end of the output.

{% highlight d linenos %}
writefln("123456789012");
writefln("%010s", 100);                 // prefix 100 with zeroes
writefln("% 10s", 100);                 // prefix 100 with spaces
writefln("%010s", -100);                // prefix -100 with zeroes
writefln("%+010s", 100);                // prefix 100 with + and zeroes
writefln("%+ 10s", 100);                // prefix 100 with +, ingores space
writefln("%010s", "first");             // right align, ignores zero
writefln("%+010s", "second");           // right align, ignores +, ignores zero
writefln("%s%10s%s",  ".", "aaa", "."); // right align 'aaa'
writefln("%s%-10s%s", ".", "bbb", "."); // left align 'bbb'
writefln("%s%10s%s",  ".", "ccc", ".");
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
