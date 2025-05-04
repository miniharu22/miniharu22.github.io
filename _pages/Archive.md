---
layout: archive
permalink: /Archive/
title: "Archive"
author_profile: true
sidebar_main: true
header:
  overlay_image: /assets/images/post1.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
---

<div class="grid__wrapper">
  {% assign collection = 'projects' %}
  {% assign posts = site[collection] | reverse %}
  {% for post in posts %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>
