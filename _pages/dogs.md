---
title: Dogs
layout: categories
permalink: /dogs/
---

<ul>
  {% for dog in site.dogs %}
    <li>
      <h3><a href="{{ dog.url }}">{{ dog.name }}</a></h3>
      Born: {{ dog.dob | date_to_string: "ordinal", "US" }}  
      {{ dog.excerpt | markdownify }}
    </li>
  {% endfor %}
</ul>