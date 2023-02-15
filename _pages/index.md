---
layout: page
title: Home
id: home
permalink: /
---

# Welcome! 🌱

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  Take a look at <span style="font-weight: bold">[[Your first note]]</span> to get started on your exploration.
</p>


<content>
This digital garden template is free, open-source, and [available on GitHub here](https://github.com/maximevaillancourt/digital-garden-jekyll-template).

The easiest way to get started is to read this [step-by-step guide explaining how to set this up from scratch](https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll).
</content>

<h1>{{ Hiking Plan }}</h1>
<iframe src="https://www.komoot.com/tour/959755370/embed?share_token=aIdCqgWBsEWLcVgZIU1far4ijUgnleZe8rQzCLJQOe7ovG4Ypi&profile=1" width="100%" height="700" frameborder="0" scrolling="no"></iframe>

<side style="font-size: 0.9em">
  <strong>Recently updated notes</strong>
</side> 

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes | limit: 5 %}
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
