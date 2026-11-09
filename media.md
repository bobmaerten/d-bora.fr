---
layout: page
title: D-BORA — Média
description: "Écoutez les titres de D-BORA sur SoundCloud et regardez nos concerts et sessions de répétition en vidéo."
last_modified_at: 2024-11-29
---

# Média

<div class="media-section row row-cols-1 row-cols-md-2 g-4">
  {% for sound in site.data.soundclouds %}
    <div class="col">
      {% include soundcloud_embed.html id=sound.id title=sound.title %}
    </div>
  {% endfor %}
</div>

<div class="section-separator my-5"></div>

<div class="media-section row row-cols-1 row-cols-md-2 g-4">
  {% for video in site.data.videos %}
    <div class="col">
      {% include youtube_embed.html id=video.id title=video.title %}
    </div>
  {% endfor %}
</div>
