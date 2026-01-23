---
layout: default
title: Speakers
permalink: /speakers/
---

<link rel="stylesheet" href="{{ '/assets/css/speakers.css' | relative_url }}">

<div class="speakers-grid">
  {% for speaker in site.data.speakers %}
    <div class="speaker-card">
      <img class="speaker-photo" src="{{ speaker.img | relative_url }}" alt="{{ speaker.alt | default: speaker.name }}">
      <div class="speaker-name">{{ speaker.name }}</div>
      <div class="speaker-title">{{ speaker.title }}</div>
      <div class="speaker-affil">{{ speaker.affil }}</div>
    </div>
  {% endfor %}
</div>
