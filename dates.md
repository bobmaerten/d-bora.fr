---
layout: page
title: D-BORA — les dates
last_modified_at: 2024-02-08
---

<div class="row">
<div class="col-12 col-md-8 col-lg-6 mx-auto" markdown="1">

<div class="text-center" markdown="1">
<dl class="date-upcoming mb-5">
  {% for liveshow in site.data.upcoming_liveshows %}
    <dt class="mt-4">
      {{ liveshow.when | localize: '%d %B %Y', 'fr' }}
    </dt>
    <dd>
      <span class="fs-4">{{ liveshow.title }}</span>
      {% if liveshow.subtitle %}
        <span class="d-block fst-italic">{{ liveshow.subtitle }}</span>
      {% endif %}
      {% if liveshow.address %}
        <span class="d-block text-muted-warm">{{ liveshow.address }}</span>
      {% endif %}
      <span class="d-block fw-bold text-accent">{{ liveshow.when | date: '%H h %M' }}</span>
      {% if liveshow.tickets %}
        <span class="d-block"><a href="{{ liveshow.tickets }}">Billets</a></span>
      {% endif %}
      {% if liveshow.price %}
        <span class="d-block text-gold">PAF : {{ liveshow.price }} €</span>
      {% endif %}
    </dd>
  {% endfor %}
</dl>

<div class="section-separator my-5"></div>

<dl class="date-past">
  {% for liveshow in site.data.past_liveshows %}
    <dt class="mt-3">{{ liveshow.when | localize: '%d %B %Y', 'fr' }}</dt>
    <dd>
      <span class="fs-5">{{ liveshow.title }}</span>
      {% if liveshow.subtitle %}
        <span class="d-block fst-italic">{{ liveshow.subtitle }}</span>
      {% endif %}
      {% if liveshow.address %}
        <span class="d-block text-muted-warm">{{ liveshow.address }}</span>
      {% endif %}
    </dd>
  {% endfor %}
</dl>

</div>
</div>
</div>
