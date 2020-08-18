---
layout: archive
title: "Publication List"
permalink: /conferences/
author_profile: true
---

{% if site.author.googlescholar %}
  You can also find my articles on <u><a href="https://scholar.google.com/citations?user=8B0t8AYAAAAJ&hl=en">my Google Scholar profile</a>.</u>
{% endif %} 

{% include base_path %}

{% assign yearArray = "2020, 2019, 2018" | split: ", " %}

{% for i in yearArray %}
### {{i}}
<table>
{% for post in site.conferences reversed %}
  {% if post.year == i %}
  <tr>{% include publication.html %}</tr>
  {% endif %}
{% endfor %}
</table>
{% endfor %}
