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

The following Type Propertes are defined for floating point types:

* __alignof__    -
* __dig__         - number of decimal digits of precision                                                       
* __epsilon__    - smallest increment to the value 1                                                           
* __im__          - imaginary part                                                                              
* __init__        - initial value                                                                               
* __infinity__   - infinity value                                                                              
* __mangleof__   -
* __mant_dig__   - number of bits in mantissa                                                                  
* __max__         - largest representable value that's not infinity                                             
* __max_10_exp__ - maximum int value such that 10 <sup>max_10_exp</sup> is representable                       
* __max_exp__     - maximum int value such that 2 <sup>max_exp-1</sup> is representable                         
* __min__         - minimum or smallest value the type can accommodate                                          
* __min_10_exp__ - minimum int value such that 10 <sup>min_10_exp</sup> is representable as a normalized value 
* __min_exp__    - minimum int value such that 2 <sup>min_exp-1</sup> is representable as a normalized value   
* __min_normal__ - smallest representable normalized value that's not 0                                        
* __nan__         - NaN value                                                                                   
* __re__          - real part                                                                                   
* __sizeof__     -
* __stringof__   -

The following table shows the floating point type property values.

| Type    | sizeof | prec | epsilon      | mantissa (bits) | max            | 10<sup>max</sup> | 2<sup>max-1</sup> | min (normal)   | 10<sup>min</sup> | 2<sup>min-1</sup> |
|---------|:------:|:----:|--------------|:---------------:|----------------|:----------------:|:-----------------:|----------------|:----------------:|:-----------------:|
| float   | 4      | 6    | 1.19209e-07  | 24              | 3.40282e+38    | 38               | 128               | 1.17549e-38    | -37              | -125              |
| double  | 8      | 15   | 2.22045e-16  | 53              | 1.79769e+308   | 308              | 1024              | 2.22507e-308   | -307             | -1021             |
| real    | 16     | 18   | 1.0842e-19   | 64              | 1.18973e+4932  | 4932             | 16384             | 3.3621e-4932   | -4931            | -16381            |
| ifloat  | 4      | 6    | 1.19209e-07i | 24              | 3.40282e+38i   | 38               | 128               | 1.17549e-38i   | -37              | -125              |
| idouble | 8      | 15   | 2.22045e-16i | 53              | 1.79769e+308i  | 308              | 1024              | 2.22507e-308i  | -307             | -1021             |
| ireal   | 16     | 18   | 1.0842e-19i  | 64              | 1.18973e+4932i | 4932             | 16384             | 3.3621e-4932i  | -4931            | -16381            |
