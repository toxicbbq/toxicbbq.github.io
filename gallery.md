---
layout: page
title: Image Gallery
permalink: /gallery/
---

<div class="gallery">
  {% for image in site.static_files %}
    {% if image.path contains 'assets/gallery' %}
      <img src="{{ image.path | relative_url }}" alt="Gallery image" />
    {% endif %}
  {% endfor %}
</div>

<style>
.gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}
.gallery img {
  width: auto;
  height: auto;
  border-radius: 8px;
}
</style>