---
layout: page
title: D-BORA — Média
last_modified_at: 2023-10-16
---

# Media

<div class="row row-cols-1 row-cols-md-2 g-4">
  {% for video in site.data.videos %}
    <div class="col">
      {% include youtube_embed.html id=video.id title=video.title %}
    </div>
  {% endfor %}
</div>
