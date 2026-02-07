---
layout: page
title: Portfolio
icon: fas fa-laptop-code
order: 1
permalink: /portfolio/
---

{% assign sorted_portfolio = site.portfolio | sort: "date" | reverse %}
{% assign categories = "" | split: "" %}

{% for post in sorted_portfolio %}
  {% unless categories contains post.category %}
    {% assign categories = categories | push: post.category %}
  {% endunless %}
{% endfor %}

{% for category in categories %}
## {{ category }}
  
  {% for post in sorted_portfolio %}
    {% if post.category == category %}
### [{{ post.title }}]({{ post.url | relative_url }})
{{ post.excerpt }}
    {% endif %}
  {% endfor %}
{% endfor %}
