---
layout: default
title: Home
---

## Welcome to AfricanLaw

Select a legislative document from the sidebar index or browse the published acts below:

<ul>
  {% for post in site.posts %}
    <li style="margin-bottom: 10px;">
      <a href="{{ post.url | relative_url }}" style="font-size: 1.1rem; font-weight: 600; color: #1d70b8; text-decoration: none;">{{ post.title }}</a>
      <div style="font-size: 0.85rem; color: #505a5f;">Published on {{ post.date | date_to_string }}</div>
    </li>
  {% endfor %}
</ul>
