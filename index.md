---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Index
excerpt:
group: DLang
tags: [dlang, dguide, draft]
---

This is my experimental Guide to the [D Programming Language](http://dlang.org/).
This is a _work in progress_.
Information presented here possibly _contain errors_ and _may not be up-to-date_.
This guide is initially based on the official language specification as of [_version 2.068.2_](http://dlang.org/changelog/2.068.2.html).

## Status = Work in Progress

I will be posting here about updates.
So stay tuned.

## Organization

The following is the list of major topics for this guide.

<ol>
{% for item in site.data.dguide %}
    {% if item.href == 'divider' %}
        <hr class="thin compact darker">
    {% else %}
        <li class="padding_left_5"><a class="no_underline" href="{{ item.href }}">{{ item.chapter }}</a></li>
    {% endif %}
{% endfor %}
</ol>

{% comment %}
#### Conventions
The following are the coventions used throughout.
{% endcomment %}