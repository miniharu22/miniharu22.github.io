---
title: "TCAD Practice"
layout: archive
excerpt: "Through MOSCAP and MOSFET simulations, Practice using Sentaurus TCAD tools. Also, analyze simulation results based on Device physics."
permalink: /TCAD_Practice
sidebar:
    nav: "sidebar-category"

header:
  overlay_image: /assets/images/post1.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
  actions:
    - label: "Github Repository"
      url: "https://github.com/miniharu22/TCAD_Practice"
---


{% assign posts = site.categories.TCAD_Practice %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}

