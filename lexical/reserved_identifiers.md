---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Lexical
section: Reserved Identifiers
excerpt: Language reserved words
group: DLang
tags: [dlang, dlangref, draft]
---

The language defines some identifiers as reserved identifiers that are globally defined.
They cannot be redefined anywhere in a source file.
These reserved identifiers are used as keywords in the 4th phase of compilation.

The following table lists the deprecated keywords.

| Keyword  | Remark |
|----------|--------|
| delete   | |
| typedef  | |
| volatile | |

The following table lists the language keywords in alphabetical order.

| Keyword         | Category    | Remark |
|:----------------|-------------|--------|
| {%raw%}__gshared{%endraw%} | attribute | Concurrency programming. |
| {%raw%}__traits{%endraw%}   | attribute   | Compile-time reflection. |
| {%raw%}__vector{%endraw%}  |           | SIMD. |
| abstract        | attribute   |        |
| alias           |             |        |
| align           | attribute   |        |
| asm             | statement   |        |
| assert          | function    |        |
| auto            | attribute   |        |
| &nbsp;          |             |        |
| body            |             | Function body block statement in contract programming. |
| bool            | data type   |        |
| break           | statement   |        |
| byte            | data type   |        |
| &nbsp;          |             |        |
| case            |             |        |
| cast            | expression  |        |
| catch           |             |        |
| cdouble         | data type   |        |
| cent            | data type   |        |
| cfloat          | data type   |        |
| char            | data type   |        |
| class           | declaration |        |
| const           | attribute   |        |
| continue        | statement   |        |
| creal           | data type   |        |
| &nbsp;          |             |        |
| dchar           | data type   |        |
| debug           |             |        |
| default         |             |        |
| delegate        |             |        |
| deprecated      | attribute   |        |
| do              | statement   |        |
| double          | data type   |        |
| &nbsp;          |             |        |
| else            | statement   |        |
| enum            | declaration |        |
| export          | attribute   | Same as keyword export in C/C++. Declares something to be visible outside of the library or application. |
| extern          | declaration |        |
| &nbsp;          |             |        |
| false           | constant    |        |
| final           | attribute, statement, declaration | parameter attribute, final switch statement, final class declaration |
| finally         |             |        |
| float           | data type   |        |
| for             | statement   |        |
| foreach         | statement   |        |
| foreach_reverse | statement   |        |
| function        |             |        |
| &nbsp;          |             |        |
| goto            | statement   |        |
| &nbsp;          |             |        |
| idouble         | data type   |        |
| if              | statement   |        |
| ifloat          | data type   |        |
| immutable       | attribute   |        |
| import          | expression  |        |
| in              | attribute, expression | parameter attribute, array expression |
| inout           | attribute   | member function attribute       |
| int             | data type   |        |
| interface       |             |        |
| invariant       |             |        |
| ireal           | data type   |        |
| is              | expression  |        |
| &nbsp;          |             |        |
| lazy            | attribute   |        |
| long            | data type   |        |
| &nbsp;          |             |        |
| macro (unused)  |             |        |
| mixin           | expression, statement |        |
| module          |             |        |
| &nbsp;          |             |        |
| new             | expression  |        |
| nothrow         | attribute   |        |
| null            | constant    |        |
| &nbsp;          |             |        |
| out             | attribute | parameter attribute |
| override        | attribute   |        |
| &nbsp;          |             |        |
| package         | attribute   | Module protection |
| pragma          | statement   |        |
| private         | attribute   | Module, class protection |
| protected       | attribute   | Module, class protection |
| public          | attribute   | Module, class protection |
| pure            | attribute   |        |
| &nbsp;          |             |        |
| real            | data type   |        |
| ref             | attribute   |        |
| return          | statement   |        |
| &nbsp;          |             |        |
| scope           | attribute, statement | parameter attribute, scope guard statement |
| shared          | attribute   |        |
| short           | data type   |        |
| static          | attribute   |        |
| struct          | declaration |        |
| super           | expression  |        |
| switch          | statement   |        |
| synchronized    | statement   |        |
| &nbsp;          |             |        |
| template        | declaration |        |
| this            | expression  |        |
| throw           |             |        |
| true            | constant    |        |
| try             | statement   |        |
| typeid          | expression  |        |
| typeof          | expression  |        |
| &nbsp;          |             |        |
| ubyte           | data type   |        |
| ucent           | data type   |        |
| uint            | data type   |        |
| ulong           | data type   |        |
| union           | declaration |        |
| unittest        |             |        |
| ushort          | data type   |        |
| &nbsp;          |             |        |
| version         |             |        |
| void            | data type   |        |
| &nbsp;          |             |        |
| wchar           | data type   |        |
| while           | statement   |        |
| with            | statement   |        |

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