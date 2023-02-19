---
layout: page
title: Home
id: home
permalink: /
---

# Welcome! 🌱

 <p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  <b>Hey folks! Good to see you here!</b> <br>

  This website is designed to archive my recent blogs along with my study and research. Feel free to let me know if you have any comments or advice.:) <br>

  Feel free to visit <a href="https://bowwang.dev">my site</a> for more information. 😺
</p>

<hr>

<strong>Recently updated notes</strong>


<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes | limit: 10 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>


<hr>

## Project Related

#### [[3D Backend|3D Backend Design Flow]]

## Course Related


