---
layout: page
title: Categories
permalink: /Categories/
---

{% for category in site.categories %}
  <li id="category"><h4>{{ category | first | capitalize }}</h4>
    <ul>
    {% for posts in category %}
      {% for post in posts %}
        {% if post.url %}
          <li>
            <a href="{{ post.url }}">
              {{ post.title }}
            </a>
          </li>
        {% endif %}
      {% endfor %}
    {% endfor %}
    </ul>
  </li>
{% endfor %}
