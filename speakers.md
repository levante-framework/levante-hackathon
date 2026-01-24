---
layout: default
title: Speakers
permalink: /speakers/
---

<h1>Speakers</h1>

<div class="speakers-grid">
  {% for s in site.speakers %}
    <article class="speaker-card">
      <a href="{{ s.url }}">
        <img src="{{ s.photo | default: '/assets/images/speakers/default.jpg' }}" alt="Photo of {{ s.name }}" class="speaker-photo" />
      </a>
      <h2 class="speaker-name"><a href="{{ s.url }}">{{ s.name }}</a></h2>
      <p class="speaker-title">{{ s.title }}</p>
      <p class="speaker-institution">{{ s.institution }}</p>
    </article>
  {% endfor %}
</div>

<style>
/* simple styles you can paste into your main CSS instead */
.speakers-grid{
  display:grid;
  grid-template-columns: repeat(auto-fit,minmax(200px,1fr));
  gap:1rem;
  margin-top:1rem;
}
.speaker-card{
  text-align:center;
  padding:0.75rem;
  border:1px solid #eee;
  border-radius:8px;
  background: #fff;
}
.speaker-photo{
  width:120px;
  height:120px;
  object-fit:cover;
  border-radius:50%;
  display:block;
  margin:0 auto 0.5rem;
}
.speaker-name{ font-size:1.05rem; margin:0.2rem 0; }
.speaker-title, .speaker-institution{ margin:0; font-size:0.9rem; color:#555; }
</style>
