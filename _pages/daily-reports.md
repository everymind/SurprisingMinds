---
layout: archive
permalink: /blog/daily-reports
title: "Surprising Minds Exhibit: Daily Reports"
author_profile: false
sidebar: 
  nav: docs
---

For every day of data collection with the Surprising Minds exhibit, we wrote up a daily report.  

<div class="tiles">
{% for post in site.categories.daily-report %}
  {% include post-grid.html %}
{% endfor %}
</div>
