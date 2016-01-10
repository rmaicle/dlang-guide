---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Identifiers and Tokens
section: Reserved Identifiers
subsection: Categorized
excerpt: Language reserved words
group: DLang
tags: [dlang, dguide, draft]
---

The following table lists the categorized language keywords.

##### Constant (3)

| Keyword           | Remark |
|:-----------------:|--------|
| false             |        |
| null              |        |
| true              |        |

##### Data Type (24)

| Keyword           | Remark |
|:-----------------:|--------|
| bool              |        |
| byte              |        |
| cdouble           |        |
| cent              |        |
| cfloat            |        |
| char              |        |
| creal             |        |
| dchar             |        |
| double            |        |
| float             |        |
| idouble           |        |
| ifloat            |        |
| int               |        |
| ireal             |        |
| long              |        |
| real              |        |
| short             |        |
| ubyte             |        |
| ucent             |        |
| uint              |        |
| ulong             |        |
| ushort            |        |
| void              |        |
| wchar             |        |

##### Attribute (25)

| Keyword           | Remark |
|:-----------------:|--------|
| &#95;&#95;gshared | Concurrency programming. |
| &#95;&#95;traits  | Compile-time reflection. |
| abstract          |        |
| align             |        |
| auto              |        |
| const             |        |
| deprecated        |        |
| export            | Same as export keyword in C/C++. Declares something to be visible outside of the library or application. |
| final             | parameter attribute |
| immutable         |        |
| in                | parameter attribute |
| inout             | member function attribute |
| lazy              |        |
| nothrow           |        |
| out               | parameter attribute |
| override          |        |
| package           | Module protection |
| private           | Module, class protection |
| protected         | Module, class protection |
| public            | Module, class protection |
| pure              |        |
| ref               |        |
| scope             | parameter attribute |
| shared            |        |
| static            |        |

##### Declaration (7)

| Keyword           | Remark |
|:-----------------:|--------|
| class             |        |
| enum              |        |
| extern            |        |
| final             | final class declaration |
| struct            |        |
| template          |        |
| union             |        |

##### Expression (10)

| Keyword           | Remark |
|:-----------------:|--------|
| cast              |        |
| import            |        |
| in                | array expression |
| is                |        |
| mixin             |        |
| new               |        |
| super             |        |
| this              |        |
| typeid            |        |
| typeof            |        |

##### Statement (20)

| Keyword           | Remark |
|:-----------------:|--------|
| asm               |        |
| break             |        |
| continue          |        |
| do                |        |
| else              |        |
| final             | final switch statement |
| for               |        |
| foreach           |        |
| foreach_reverse   |        |
| goto              |        |
| if                |        |
| mixin             |        |
| pragma            |        |
| return            |        |
| scope             | scope guard statement |
| switch            |        |
| synchronized      |        |
| try               |        |
| while             |        |
| with              |        |

##### Uncategorized (20)

| Keyword           | Remark |
|:-----------------:|--------|
| &#95;&#95;parameters |          | Parameter tuple of a function, delegate, or function pointer. |
| &#95;&#95;vector  | SIMD. |
| alias             |        |
| body              | Function body block statement in contract programming. |
| case              |        |
| catch             |        |
| debug             |        |
| default           |        |
| delegate          |        |
| finally           |        |
| function          |        |
| interface         |        |
| invariant         |        |
| macro (unused)    |        |
| module            |        |
| throw             |        |
| unittest          |        |
| version           |        |

{% comment %}
http://dlang.org/traits.html.

Traits are language extensions for compile time reflection designed to be extensible to allow easier addition of new capabilities.
Traits keywords are not reserved words in a sense that users can define the same Traits keywords in their program but it does not affect the original Traits keywords.
Traits keywords are local only to the Traits language extension.

The following lists the Traits keywords.

| Keyword         | Category    | Remark |
|:----------------|-------------|--------|
| isAbstractClass
| isArithmetic
| isAssociativeArray
| isFinalClass
| isPOD
| isNested
| isFloating
| isIntegral
| isScalar
| isStaticArray
| isUnsigned
| isVirtualFunction
| isVirtualMethod
| isAbstractFunction
| isFinalFunction
| isStaticFunction
| isOverrideFunction
| isTemplate
| isRef
| isOut
| isLazy
| hasMember
| identifier
| getAliasThis
| getAttributes
| getFunctionAttributes
| getMember
| getOverloads
| getPointerBitmap
| getProtection
| getVirtualFunctions
| getVirtualMethods
| getUnitTests
| parent
| classInstanceSize
| getVirtualIndex
| allMembers
| derivedMembers
| isSame
| compiles
{% endcomment %}


{% comment %}
[abstract]:
[alias]:
[align]:
[asm]:
[assert]:
[auto]:

[body]:
[bool]:
[break]:
[byte]:

[case]:
[cast]:
[catch]:
[cdouble]:
[cent]:
[cfloat]:
[char]:
[class]:
[const]:
[continue]:
[creal]:

[dchar]:
[debug]:
[default]:
[delegate]:
[deprecated]:
[do]:
[double]:

[else]:
[enum]:
[export]:
[extern]:

[false]:
[final]:
[finally]:
[float]:
[for]:
[foreach]:
[foreach_reverse]:
[function]:

[goto]:

[idouble]:
[if]:
[ifloat]:
[immutable]:
[import]:
[in]:
[inout]:
[int]:
[interface]:
[invariant]:
[ireal]:
[is]:

[lazy]:
[long]:

[macro (unused)]:
[mixin]:
[module]:

[new]:
[nothrow]:
[null]:

[out]:
[override]:

[package]:
[pragma]:
[private]:
[protected]:
[public]:
[pure]:

[real]:
[ref]:
[return]:

[scope]:
[shared]:
[short]:
[static]:
[struct]:
[super]:
[switch]:
[synchronized]:

[template]:
[this]:
[throw]:
[true]:
[try]:
[typeid]:
[typeof]:

[ubyte]:
[ucent]:
[uint]:
[ulong]:
[union]:
[unittest]:
[ushort]:

[version]:
[void]:

[wchar]:
[while]:
[with]:
{% endcomment %}


{% comment %}
| &nbsp;     | &nbsp;            | &nbsp;           | &nbsp;         | &nbsp;       |
|------------|-------------------|------------------|----------------|--------------|
| `abstract` | `dchar`           | `idouble`        | `out`          | `template`   |
| `alias`    | `debug`           | `if`             | `override`     | `this`       |
| `align`    | `default`         | `ifloat`         |                | `throw`      |
| `asm`      | `delegate`        | `immutable`      | `package`      | `true`       |
| `assert`   | `delete**`        | `import`         | `pragma`       | `try`        |
| `auto`     | `deprecated`      | `in`             | `private`      | `typedef**`  |
|            | `do`              | `inout`          | `protected`    | `typeid`     |
| `body`     | `double`          | `int`            | `public`       | `typeof`     |
| `bool`     |                   | `interface`      | `pure`         |              |
| `break`    | `else`            | `invariant`      |                | `ubyte`      |
| `byte`     | `enum`            | `ireal`          | `real`         | `ucent`      |
|            | `export`          | `is`             | `ref`          | `uint`       |
| `case`     | `extern`          |                  | `return`       | `ulong`      |
| `cast`     |                   | `lazy`           |                | `union`      |
| `catch`    | `false`           | `long`           | `scope`        | `unittest`   |
| `cdouble`  | `final`           |                  | `shared`       | `ushort`     |
| `cent`     | `finally`         | `macro (unused)` | `short`        |              |
| `cfloat`   | `float`           | `mixin`          |                | `version`    |
| `char`     | `for`             | `module`         | `static`       | `void`       |
| `class`    | `foreach`         |                  | `struct`       | `volatile**` |
| `const`    | `foreach_reverse` | `new`            | `super`        |              |
| `continue` | `function`        | `nothrow`        | `switch`       | `wchar`      |
| `creal`    |                   | `null`           | `synchronized` | `while`      |
|            | `goto`            |                  |                | `with`       |
{% endcomment %}

{% comment %}
~~~
 [abstract]       dchar             idouble           out             template
 alias          debug             if                override        this
 align          default           ifloat                            throw
 asm            delegate          immutable         package         true
 assert         deprecated        import            pragma          try
 auto           do                in                private         typeid
                double            inout             protected       typeof
 body                             int               public
 bool           else              interface         pure            ubyte
 break          enum              invariant                         ucent
 byte           export            ireal             real            uint
                extern            is                ref             ulon
 case                                               return          union
 cast           false             lazy                              unittest
 catch          final             long              scope           ushort
 cdouble        finally                             shared
 cent           float             macro (unused)    short           version           
 cfloat         for               mixin                             void
 char           foreach           module            static
 class          foreach_reverse                     struct          wchar
 const          function          new               super           while
 continue                         nothrow           switch          with
 creal          goto              null              synchronized
~~~
{% endcomment %}