---
layout: page
title: Home
id: home
permalink: /
---

# Welcome! 🌱

<!-- <p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  Take a look at <span style="font-weight: bold">[[Your first note]]</span> to get started on your exploration.
</p>
 --><p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  <b>Hey folks! Good to see you here!</b>

  This website is designed to archive my recent blogs along with my study and research. Feel free to let me know if you have any comments or advice.:)

  Take a look at <span style="font-weight: bold">[[Your first note]]</span> to have an overview of the topic and related blogs.
</p>


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

<p>Here are all the notes in this garden, along with their links, visualized as a graph.</p>

<main>{% include notes_graph.html %}</main>


<hr>
