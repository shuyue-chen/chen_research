---
layout: default
title: Home
---

# Shuyue Chen

<div class="hero">

<img src="https://images.unsplash.com/photo-1461360228754-6e81c478b882?auto=format&fit=crop&w=1600&q=80" alt="Historical library">

</div>

<div class="intro">

I write about history, culture, cities, historical memory, and theory.

This website is a space for essays, research notes, reading reflections, and unfinished ideas.

</div>

## Essays

{% for essay in site.essays reversed limit:3 %}

<div class="entry">

<h3>
<a href="{{ essay.url | relative_url }}">
{{ essay.title }}
</a>
</h3>

<div class="date">
{{ essay.date | date: "%B %-d, %Y" }}
</div>

<p>{{ essay.description }}</p>

</div>

{% endfor %}

[View all essays →]({{ '/essays/' | relative_url }})

## Recent Notes

{% for note in site.notes reversed limit:5 %}

<div class="entry">

<h3>
<a href="{{ note.url | relative_url }}">
{{ note.title }}
</a>
</h3>

<div class="date">
{{ note.date | date: "%B %-d, %Y" }}
</div>

</div>

{% endfor %}

[View all notes →]({{ '/notes/' | relative_url }})

## Research

My interests include:

- History
- Cultural Memory
- Urban History
- Historical Theory
- Modernity

[Learn more about my research →]({{ '/research/' | relative_url }})
