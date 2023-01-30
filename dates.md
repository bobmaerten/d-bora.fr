---
layout: page
title: D-BORA — les dates
---

# Nos dates de concerts

<div class="row">
<div class="col-12 col-md-6 offset-md-3" markdown="1">

<div class="text-center" markdown="1">

<dd class="mb-5">
  {% for liveshow in site.data.upcoming_liveshows %}
    <dt class="text-danger mt-3">
      {{ liveshow.when | localize: '%d %B %Y', 'fr' }}
    </dt>
    <dd class="border-bottom border-light-subtle pb-3">
      <span class="fs-4">{{ liveshow.title }}</span>
      {% if liveshow.subtitle %}
        <span class="d-block fst-italic">{{ liveshow.subtitle }}</span>
      {% endif %}
      {% if liveshow.address %}
        <span class="d-block text-secondary">{{ liveshow.address }}</span>
      {% endif %}
      <span class="d-block fw-bold text-info">{{ liveshow.when | date: '%H h %M' }}</span>
      {% if liveshow.price %}
        <span class="d-block text-danger">{{ liveshow.price }}</span>
      {% endif %}
    </dd>
  {% endfor %}
</dd>

<dd class="mt-5">
  {% for liveshow in site.data.past_liveshows %}
    <dt class="text-danger mt-3">{{ liveshow.when | localize: '%d %B %Y', 'fr' }}</dt>
    <dd>
      <span class="fs-4">{{ liveshow.title }}</span>
      {% if liveshow.subtitle %}
        <span class="d-block fst-italic">{{ liveshow.subtitle }}</span>
      {% endif %}
      {% if liveshow.address %}
        <span class="d-block text-secondary">{{ liveshow.address }}</span>
      {% endif %}
      {% if liveshow.price %}
        <span class="d-block text-danger">{{ liveshow.price }}</span>
      {% endif %}
    </dd>
  {% endfor %}
</dd>

</div>
</div>
</div>
