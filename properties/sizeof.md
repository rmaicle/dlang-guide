---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Type Properties
section: sizeof Property
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

The `sizeof` property gives the size in bytes that the type or expression occupies in memory.

##### Class

When the `sizeof` property is applied to a class reference, the value is the size of the class reference, not the class instantiation.
Because the type or expression is only evaluated lexically, a struct or class does not need to be instantiated to use its `sizeof` property.

{% highlight d linenos %}
import std.stdio;

struct A {
    int a;
    float f;
}

class B {
    int b;
    float f;
}

void main() {
    A a;
    auto aa = new A();
    writeln(A.sizeof);              // 8
    writeln(a.sizeof);              // 8
    writeln(aa.sizeof);             // 8
    
    B b;                            // no reference, null instance
    auto bb = new B();
    writeln(B.sizeof);              // 8
    writeln(b.sizeof);              // 8
    writeln(bb.sizeof);             // 8
}
{% endhighlight %}

##### Structure Member

Like all other Type Properties, the type or expression is only lexically evaluated.
Because the type or expression is only evaluated lexically, a struct or class does not need to be instantiated to use the `sizeof` property of a member.

{% highlight d linenos %}
import std.stdio;

struct A { int a; }
class B { int b; }

void main() {
    writeln(A.a.sizeof);            // 4
    writeln(B.b.sizeof);            // 4
    A a;
    B b;
    writeln(a.a.sizeof);            // 4
    writeln(b.b.sizeof);            // 4
}
{% endhighlight %}

