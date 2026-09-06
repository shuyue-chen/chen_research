---
layout: default
title: Essays
---

# Essays

{% for essay in site.essays reversed %}

<div class="entry">

<h3>

<a href="{{ essay.url | relative_url }}">
{{ essay.title }}
</a>

</h3>

<div class="date">
{{ essay.date | date: "%B %-d, %Y" }}
</div>

<p>
{{ essay.description }}
</p>

</div>

{% endfor %}
