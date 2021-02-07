---
layout: page
title: Archives
permalink: /archives/
---

{% assign years = site.posts | group_by_exp:"post", "post.date | date: '%Y'" %}
{% for year in years %}
  <ul>
  <li>{{year.name}}</li>
  {% assign months = year.items | group_by_exp:"post", "post.date | date: '%B'" %}
  {% for month in months %}
  <ul>
    <li>{{month.name}}</li>
    <ul>
    {% for post in month.items %}
      <li>
        <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
      </li>
    {% endfor %}
    </ul>
  </ul>
  {% endfor %}
  </ul>
{% endfor %}