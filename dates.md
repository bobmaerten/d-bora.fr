---
layout: page
title: D-BORA — les dates
---

# Dates

<div class="row">
<div class="col-12 col-md-6 offset-md-3" markdown="1">

<div class="text-center" markdown="1">

<dd>
  {% for liveshow in site.data.liveshows %}
    <dt class="text-danger mt-3">{{ liveshow.when | date_to_string }}</dt>
    <dd>
      <span class="fs-4">{{ liveshow.title }}</span>
      {% if liveshow.subtitle %}
        <span class="d-block fst-italic">{{ liveshow.subtitle }}</span>
      {% endif %}
      {% if liveshow.address %}
        <span class="d-block text-muted">{{ liveshow.address }}</span>
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
