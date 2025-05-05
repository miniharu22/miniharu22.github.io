---
title: "MOSFET Process Simulation"
layout: archive
excerpt: "Design a 180nm MOSFET with Sentaurus Process and check its characteritics using Sentaurus Device."
permalink: /MOSFET_Process_Simulation
sidebar:
    nav: "sidebar-category"
header:
  overlay_image: /assets/images/post1.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
  actions:
    - label: "Github Repository"
      url: "https://github.com/miniharu22/TCAD_Project/tree/main/180nm_MOSFET"
---


{% assign posts = site.categories.MOSFET_Process_Simulation %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}