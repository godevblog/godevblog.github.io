---
title: Liczniki
date: 2019-01-28
author: Krzysztof Owsiany
layout: author/page
permalink: liczniki
---

{% assign currentYear = 0 %}
{% assign counterAllPost = 0 %}
{% assign counter = 0 %}
{% for post in site.posts %}
{% assign thisyear = post.date | date: "%Y" %}
{% assign thisyearWithMonth = post.date | date: "%B %Y" %}
{% assign prevyearWithMonth = post.previous.date | date: "%B %Y" %}
{% assign counter = counter | plus: 1 %}
{% assign counterAllPost = counterAllPost | plus: 1 %}

{% if thisyear != currentYear %}
## {{ thisyear }}:
{% assign currentYear = thisyear %}
{% endif %}

{% if thisyearWithMonth != prevyearWithMonth %}
* {{ post.date | date: "%B" }} - **{{ counter }}**
{% assign counter = 0 %}
{% endif %}
{% endfor %}

**Wszystkich postów: {{ counterAllPost }}**{:.h-1}