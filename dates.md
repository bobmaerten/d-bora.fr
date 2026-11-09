---
layout: page
title: D-BORA — les dates
last_modified_at: 2026-11-09
photos:
  - name: jp-bob-scene
    alt: JP et Bob sur scène
  - name: jp-bob-harmonica
    alt: JP à l'harmonica, Bob à la basse, en plein air
  - name: fred-bar
    alt: Fred à la guitare dans un bar
  - name: jp-bar
    alt: JP au chant et à la guitare dans un bar
---

<h1>Dates</h1>

<div class="row g-5">
<div class="col-12 col-lg-7">

<h2 class="h3 text-gold mt-5 mb-3">Prochains concerts</h2>
{% include upcoming_shows.html detailed=true %}

<h2 class="h3 text-gold mt-5 mb-3">Concerts passés</h2>
<ul class="list-unstyled">
  {% for show in site.data.past_liveshows %}
  {% include show_row.html show=show %}
  {% endfor %}
</ul>

</div>

<div class="col-12 col-lg-5">
<div class="row row-cols-2 g-3 sticky-lg-top dates-gallery">
  {% for photo in page.photos %}
  <div class="col">
    <div class="photo-frame ratio ratio-3x4">
      <img src="assets/img/live/{{ photo.name }}.jpg" srcset="assets/img/live/{{ photo.name }}-sm.jpg 300w, assets/img/live/{{ photo.name }}.jpg 600w" sizes="(min-width: 1400px) 260px, (min-width: 992px) 20vw, 45vw" width="600" height="800" class="object-fit-cover" loading="lazy" alt="{{ photo.alt }}" />
    </div>
  </div>
  {% endfor %}
</div>
</div>

</div>
