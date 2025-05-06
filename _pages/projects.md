---
layout: archive
permalink: /projects/
title: "Archive"
excerpt: "Summary of all the research, project, study, and practice I have did."
author_profile: true
sidebar:
    nav: "sidebar-category"
toc: true
toc_sticky: true
header:
  overlay_image: /assets/images/post1.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
---

<div class="grid__wrapper">
  {% assign collection = 'tcad' %}
  {% assign posts = site[collection] | reverse %}
  {% for post in posts %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>

<div class="grid__wrapper">
  {% assign collection = 'fab' %}
  {% assign posts = site[collection] | reverse %}
  {% for post in posts %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>


