<!-- ---
layout: default
title: Photos
permalink: /photos/
# description: "ENTER HERE"
nav: true
nav_order: 4
---

<h1>Photo Gallery</h1>
<div class="photo-gallery">
  {% assign photos = site.static_files | where: "directory", "/assets/images/photos/" %}
  {% for photo in photos %}
    <div class="photo-item">
      <img src="{{ site.url }}/assets/images/photos/{{photo.name}}" alt="{{ photo.name }}">
      <p>{{ photo.name | replace: '-', ' ' | replace: '.jpg', '' }}</p>
    </div>
  {% endfor %}
</div>

<style>
.photo-gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.photo-item {
  flex: 1 1 calc(50% - 20px);
  box-sizing: border-box;
}

.photo-item img {
  width: 100%;
  height: auto;
}

.photo-item p {
  text-align: center;
  font-size: 14px;
  color: #555;
}
</style> -->