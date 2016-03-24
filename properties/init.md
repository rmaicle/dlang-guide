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
It is an error to use the `init` Property with the `void` type.
If the property is applied to a variable, then the value is the default initializer for the type of the variable.
If the property is used with an expression, that expression is evaluated first and the resulting type is used.

##### Basic Types and Variables

See the following sections for type specific `init` Property values:

* [boolean `init` Property](/dlang-guide/basic_types/boolean/properties.html)
* [integral `init` Property](/dlang-guide/basic_types/integral/properties.html)
* [floating point `init` Property](/dlang-guide/basic_types/floating_point/properties/init.html)

##### Enumerations

See [Enumeration `init` Property](/dlang-guide/enumerations/properties/init.html).

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
