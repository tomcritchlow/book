---
title: wordcount
---

{% assign total = 0 %}
{% for post in site.chapters %}
  {% capture words1 %}{{post.content | number_of_words}}{% endcapture %}
  {% assign words = words | plus: words1 %}
{% endfor %}
{{ words }}