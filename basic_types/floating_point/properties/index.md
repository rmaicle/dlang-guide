---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Floating Point Types
subsection: Properties
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

The following common [Type Properties] are defined for floating point types:

* `alignof`     - alignment in bytes
* `mangleof`    - text representation
* `sizeof`      - size in bytes
* `stringof`    - string representation

As with other numeric types, the following Type Properties are defined for floating point types:

* `init`        - initial value
* `max`         - largest representable value
* `min`         - smallest representable value

The following Properties are specific to floating point types only.
Using them with other types will result into a compile error.

* `dig`         - number of decimal digits of precision                                                       
* `epsilon`     - smallest increment to the value 1                                                           
* `im`          - imaginary part                                                                              
* `infinity`    - infinity value                                                                              
* `mant_dig`    - number of bits in mantissa                                                                  
* `max_10_exp`  - maximum int value such that 10 <sup>max_10_exp</sup> is representable                       
* `max_exp`     - maximum int value such that 2 <sup>max_exp-1</sup> is representable                         
* `min_10_exp`  - minimum int value such that 10 <sup>min_10_exp</sup> is representable as a normalized value 
* `min_exp`     - minimum int value such that 2 <sup>min_exp-1</sup> is representable as a normalized value   
* `min_normal`  - smallest representable normalized value that's not 0                                        
* `nan`         - NaN value                                                                                   
* `re`          - real part                                                                                   

{% comment %}
The following table shows the floating point type property values.

| Type    | sizeof | prec | epsilon      | mantissa (bits) | max            | 10<sup>max</sup> | 2<sup>max-1</sup> | min (normal)   | 10<sup>min</sup> | 2<sup>min-1</sup> |
|---------|:------:|:----:|--------------|:---------------:|----------------|:----------------:|:-----------------:|----------------|:----------------:|:-----------------:|
| float   | 4      | 6    | 1.19209e-07  | 24              | 3.40282e+38    | 38               | 128               | 1.17549e-38    | -37              | -125              |
| double  | 8      | 15   | 2.22045e-16  | 53              | 1.79769e+308   | 308              | 1024              | 2.22507e-308   | -307             | -1021             |
| real    | 16     | 18   | 1.0842e-19   | 64              | 1.18973e+4932  | 4932             | 16384             | 3.3621e-4932   | -4931            | -16381            |
| ifloat  | 4      | 6    | 1.19209e-07i | 24              | 3.40282e+38i   | 38               | 128               | 1.17549e-38i   | -37              | -125              |
| idouble | 8      | 15   | 2.22045e-16i | 53              | 1.79769e+308i  | 308              | 1024              | 2.22507e-308i  | -307             | -1021             |
| ireal   | 16     | 18   | 1.0842e-19i  | 64              | 1.18973e+4932i | 4932             | 16384             | 3.3621e-4932i  | -4931            | -16381            |

##### Sections
{% include reference_dlang_subsubsection_links.html %}
{% endcomment %}

[Type Properties]: /dlang-guide/properties/index.html