---
layout: page
title: "Notes"
eyebrow: "Notes"
description: "Short essays, observations, reading notes, and working thoughts."
permalink: /notes/
---

{% assign notes = site.posts | sort: "date" | reverse %}

{% for note in notes %}

<article class="list-item">

    <p class="item-meta">

        {{ note.date | date: "%B %-d, %Y" }}

        {% if note.type %}
            · {{ note.type }}
        {% endif %}

    </p>

    <h3>
        <a href="{{ note.url | relative_url }}">
            {{ note.title }}
        </a>
    </h3>

    {% if note.description %}

        <p>
            {{ note.description }}
        </p>

    {% else %}

        <p>
            {{ note.excerpt | strip_html | truncate: 180 }}
        </p>

    {% endif %}

    <a href="{{ note.url | relative_url }}">
        Read note →
    </a>

</article>

{% endfor %}
