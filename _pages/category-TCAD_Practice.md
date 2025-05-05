---
title: "TCAD_Practice"
layout: archive
permalink: /TCAD_Practice
sidebar:
    nav: "sidebar-category"
redirect_from:
    - /projects/2020-10-01-COVIDDEEPNET/
header:
  overlay_image: /assets/images/post1.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
---


{% assign posts = site.categories.TCAD_Practice %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}