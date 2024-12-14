---
layout: archive
permalink: /news/
---

<h1>Latest from the lab</h1>

<ul class="news-list">
  {% assign sorted_news = site.news | sort: 'date' | reverse %}
  {% for news in sorted_news %}
    <li class="news-item">
      <h2><a href="{{ news.url }}">{{ news.title }}</a></h2>
      {% if news.photo %}
        <img src="{{ news.photo | relative_url }}" alt="{{ news.title }}" class="news-thumbnail">
      {% endif %}
      <p>{{ news.excerpt | markdownify }}</p>
    </li>
  {% endfor %}
</ul>