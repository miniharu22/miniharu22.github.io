---
title: "Category"
layout: archive
permalink: /cv/
excerpt: "Classify all posts by category."
author_profile: true
sidebar_main: true
sidebar:
    nav: "sidebar-category"
header:
  overlay_image: /assets/images/post1.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
---

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My CV Viewer</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f7f7f7;
      margin: 0;
      padding: 20px;
      text-align: center;
    }

    .download-btn {
      background-color: #6a1b9a;
      color: white;
      padding: 12px 20px;
      border: none;
      border-radius: 8px;
      font-size: 16px;
      cursor: pointer;
      text-decoration: none;
      margin-bottom: 20px;
      display: inline-block;
    }

    .pdf-viewer {
      width: 80%;
      height: 80vh;
      border: none;
      box-shadow: 0 0 10px rgba(0,0,0,0.2);
    }
  </style>
</head>
<body>

  <!-- Download Button -->
  <a class="download-btn" href="/assets/CV.pdf" download>📄 Download current CV</a>

  <!-- Embedded PDF Viewer -->
  <embed class="pdf-viewer" src="/assets/CV.pdf#toolbar=1&navpanes=0&scrollbar=1" type="application/pdf">

</body>
</html>