---
title: "TCAD_Practice"
layout: archive
permalink: /TCAD_Practice
sidebar:
    nav: "sidebar-category"

header:
  overlay_image: /assets/images/post1.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
---
{{ content }}

{% if paginator %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}



{% assign posts = site.categories.TCAD_Practice %}
<div class="entries-{{ entries_layout }}">
  {% for post in posts %}
    {% include archive-single.html type=page.entries_layout %}
  {% endfor %}
</div>

{% include paginator.html %}