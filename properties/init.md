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

See the following for type-specific `init` property:

* [boolean `init` Property](/dlang-guide/basic_types/boolean/properties.html)
* [integral `init` Property](/dlang-guide/basic_types/integral/properties.html)
* [floating point `init` Property](/dlang-guide/basic_types/floating_point/properties/init.html)
* [Enumeration `init` Property](/dlang-guide/enumerations/properties/init.html)
* [Structure `init` Property](/dlang-guide/structs/properties/init.html)

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
