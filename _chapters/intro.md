---
title: Introduction
subtitle: An overview of the book in 5 minutes
layout: tsi-chapter
---

This book is about 

Three core ideas:

1) Networks are how you get work. We'll explore how to cultivate your networks

2) Changing clients requires a lightness of touch and improvisation

3) Crafting a sustainable independent consulting practice. Requires managing your identity, energy and time.

{% assign total = 0 %}
{% for post in site.chapters %}
  {% capture words1 %}{{post.content | number_of_words}}{% endcapture %}
  {% assign words = words | plus: words1 %}
{% endfor %}
{{ words }}