---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Type Properties
section: init Property
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

The `init` property is the default initializer for the corresponding type.
The `init` property can only be used with boolean and numeric types, enumerations, and structures.
If the property is used with an expression, that expression is evaluated first and the resulting type is used.
It is an error to use it with any other types.

##### Types and Variables

The value of the `init` property is the default initializer for the type.
If `init` is applied to a variable, then the value is the default initializer for the variable type.

Here is an example of using the `init` property with boolean and some numeric types.
Lines 1-5 assigns values to the variables just to show that the `init` property values are not affected by the value of a variable.

{% highlight d linenos %}
bool b = true;
int  n = 1;
double d = 2.0;

writefln("%s %s", bool.init, b.init);       // false false
writefln("%s %s", int.init, n.init);        // 0 0
writefln("%s %s", double.init, d.init);     // nan nan
{% endhighlight %}

Notice that the value of `init` is the same whether it is applied to a type or to a variable.

##### Enumerations

The value of `init` property is the first member of the enumeration.

{% highlight d linenos %}
enum State { On, Off }

void main() {
    writeln(State.init);                    // Left
}
{% endhighlight %}

##### Struct

Using the `init` property for a structure means `init` produces a default initialized structure.
All structure members are initialized via their default initializer or via explicit initialization.

{% highlight d linenos %}
struct S {
    int a;                                  // default initialization
    int b = 7;                              // explicit initialization
}

void main() {
    writeln(S.init);                        // S(0, 7)
}
{% endhighlight %}

The output of line 7 is a built in formatted output.
Zero is the first structure member (`a`).
Seven is the second structure member (`b`).

##### TODO Nested Structs

When is `init` not usable?

##### Expression

As mentioned, if an expression is applied with the `init` property, the expression is only lexically evaluated to determine the type and uses the resulting type with the property.
To illustrate:

{% highlight d linenos %}
writeln((1 + 2).init);                      // 0   - type is evaluated to int
writeln((1.00 + 2).init);                   // nan - type is evaluated to a double
{% endhighlight %}

{% comment %}
The `init` property can also be used with unnamed (voldemort) types.
{% endcomment %}
