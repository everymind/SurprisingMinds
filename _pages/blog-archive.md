---
layout: archive
permalink: /blog/
title: "Surprising Minds Project Blog"
author_profile: true
---

This blog serves as a shared, online open lab notebook for the Surprising Minds exhibit. Posts are organized by tag below. 

{% include group-by-array collection=site.posts field="categories" %}

{% for category in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h1 id="{{ category | slugify }}" class="archive__subtitle">{{ category }}</h1>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
