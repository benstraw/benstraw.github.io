---
title: Dogs
---
<h1>My Dogs</h1>

<ul>
  {% for dog in site.dogs %}
    <li>
      <h2><a href="{{ dog.url }}">{{ dog.name }}</a></h2>
      <h3>Born: {{ dog.dob | date_to_string }}</h3>
      {{ dog.excerpt | markdownify }}
    </li>
  {% endfor %}
</ul>