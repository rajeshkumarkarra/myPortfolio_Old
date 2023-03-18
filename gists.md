---
layout: default
title: "Gists"
---

{% if site.show_excerpts %}
  {% include gists.html %}
{% else %}
  {% include archive2.html title="Gists" %}
{% endif %}
