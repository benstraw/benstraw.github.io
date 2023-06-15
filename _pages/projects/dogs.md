---
title: Dogs
layout: single 
permalink: /projects/dog-gallery/
tag: dogs
---

<ul>
{% comment %}
*
*  This loop loops through a collection called `dogs`
*  and sorts it by the front matter variable `dob` and than filters
*  the collection with `reverse` in reverse order
*
*  To make it work I first assigned the data to a new string
*  called `sorted_dogos`.
*
{% endcomment %}
  {% assign sorted_dogos = site.dogs | sort: "dob" %}
  {% for dog in sorted_dogos %}
    <li>
      <h3><a href="{{ dog.url }}">{{ dog.name }}</a></h3>
      Born: {{ dog.dob | date_to_string: "ordinal", "US" }}  
      {{ dog.excerpt | markdownify }}
    </li>
  {% endfor %}
</ul>