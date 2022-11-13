---
layout: page
title: D-BORA — Média
---

# Media

<div class="row row-cols-1 row-cols-md-2 g-4">
  {% for video in site.data.videos %}
    <div class="col">
      {% include youtube_embed.html id=video.id title=video.title %}
    </div>
  {% endfor %}
</div>
