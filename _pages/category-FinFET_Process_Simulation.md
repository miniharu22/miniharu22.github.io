---
title: "FinFET Process Simulation"
layout: archive
excerpt: "Design a 22nm FinFET and compare its perfomance with 180nm MOSFET. Explore Body biasing and Fin height variation as methods to improve performance."
permalink: /FinFET_Process_Simulation
sidebar:
    nav: "sidebar-category"
header:
  overlay_image: /assets/images/post1.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
  actions:
    - label: "Github Repository"
      url: "https://github.com/miniharu22/TCAD_Project/tree/main/22nm%20FinFET"
---


{% assign posts = site.categories.FinFET_Process_Simulation %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}