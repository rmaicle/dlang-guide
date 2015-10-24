---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Introduction
excerpt: Introduction to the D Programming Language
group: DLang
tags: [dlang, dlangref]
---

D programming language is a general purpose [systems programming language] which belongs to the [C-family languages].
It is a rich programming language supporting multiple powerful [programming paradigms]; imperative, object-oriented, functional and meta-programming.
It is an expressive language integrating pragmatic features and making them cohesively elegant to write and understand.

The D programming language design goals has a tall order.
D combines competing requirements for efficiency, control, modeling power, safety and productivity.
D promotes the principle of make correct code easier to write and wrong code harder.

Here are several things to highlight from the D programming language.

* Modules
* Conditional Compilation
* Contract Programming
* Unit Testing
* Scope-Based RAII
* First Class Arrays
* Associative Arrays
* Dynamic Arrays
* Array slicing
* Nested Functions
* Inner Classes
* Closures
* Anonymous Functions (Lambda Functions)
* Compile-Time Function Execution
* Lazy Evaluation
* Mixins
* Inline Assembler

## A Very Short History

[Walter Bright] started working on a new programming language back in the 1990s.
For Walter, this is nothing new.
He has been implementing compilers for many years.
He called it __Mars__ but people keep referring to it as __D__, a successor to the [C Programming Language].
<span class="hide">Walter named his new programming language __Mars__ but the community around it keeps calling it __D__.</span>

D was [first released](http://www.digitalmars.com/d/1.0/changelog1.html#new000) in December 2001.
[Andrei Alexandrescu] joined the language design team in 2006 and has contributed much to what the language is now.
Andrei left Facebook this year to work on D full-time, which, I think, is a very bold move.
And following that, the D Language Foundation is now incorporated.

What an exciting time for D!

[C-family languages]: https://en.wikipedia.org/wiki/List_of_C-family_programming_languages
[systems programming language]: https://en.wikipedia.org/wiki/System_programming_language
[programming paradigms]: https://en.wikipedia.org/wiki/Programming_paradigm#Multi-paradigm

[Walter Bright]: http://www.walterbright.com/
[Andrei Alexandrescu]: https://en.wikipedia.org/wiki/Andrei_Alexandrescu
[C Programming Language]: https://en.wikipedia.org/wiki/C_%28programming_language%29

{% comment %}
Show/describe general overvew of syntax.
{% endcomment %}
