---
layout: default
title: Home
---

## Legislative Repository by Country

Browse the official acts published across different jurisdictions:

<div style="margin-top: 20px;">
  {% assign countries = site.categories | sort %}
  
  {% for category in countries %}
    <h3 style="margin-top: 24px; color: #0b0c0c; border-bottom: 2px solid #b1b4b6; padding-bottom: 4px; text-transform: uppercase;">
      {{ category[0] }}
    </h3>
    
    <ul style="list-style-type: none; padding-left: 0; margin-top: 10px;">
      {% for post in category[1] %}
        <li style="margin-bottom: 10px; padding-left: 12px;">
          <a href="{{ post.url | relative_url }}" style="color: #1d70b8; text-decoration: none; font-weight: 600; font-size: 1.1rem;">
            {{ post.title }}
          </a>
          <div style="font-size: 0.85rem; color: #505a5f;">Published on {{ post.date | date_to_string }}</div>
        </li>
      {% endfor %}
    </ul>
  {% endfor %}
</div>
