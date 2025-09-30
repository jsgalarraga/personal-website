---
layout: page
title: Home
id: home
permalink: /
---

## Hola

Aquí encontraras algunas de mis reflexiones, ideas que en algún momento me apeteció escribir y publicar en este rincón de internet.

<hr>

<strong>Reflexiones</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "created_at" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.created_at | date: "%Y-%m-%d" }} — {{ note.title }}</a>
    </li>
  {% endfor %}
</ul>
