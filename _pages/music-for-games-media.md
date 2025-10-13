---
title: "Music for Games and Media"
layout: single
permalink: /music-for-games-media/
author_profile: true
---
{% assign latest = -1 %}
{% for release in site.releases %}
  {% if release.category == 'media' %}
    {% if latest == -1 or latest.release_date < release.release_date %}
      {% assign latest = release %}
    {% endif %}
  {% endif %}
{% endfor %}
## {{ latest.title }} ({{ latest.release_date | date: "%Y" }})
{% include video id=latest.video_id provider=latest.video_provider %}
{{ latest.short_description }}

{% assign release_text = "Released" %}
{{ release_text }}: {{ latest.release_date | date: "%Y-%m-%d" }}

### Available here:
<ul>
{% for link in latest.links %}
  {% if link.url %}
    <li><a href = "{{ link.url }}">{{ link.platform }}</a></li>
  {% else %}
    <li>{{ link.platform }}</li>
  {% endif %}
{% endfor %}
</ul>