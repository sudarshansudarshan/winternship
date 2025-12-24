---
layout: page
title: Case Studies
permalink: /case-studies/
---

{% assign modules = "TypeScript,React,MongoDB,Express" | split: "," %}

{% for module in modules %}

<details style="margin-bottom: 2rem; border: 1px solid #e1e4e8; border-radius: 6px; padding: 1rem;">
  <summary style="cursor: pointer; font-size: 1.5rem; font-weight: bold; margin: -1rem; padding: 1rem; background-color: #f6f8fa; border-radius: 6px;">
    {{ module }}
  </summary>
  
  <div style="margin-top: 1rem;">
    {% assign module_items = site.case_studies | where: "module", module | sort: "order" %}
    
    {% if module_items.size > 0 %}
      <ul style="list-style-type: none; padding-left: 0;">
        {% for cs in module_items %}
          <li style="margin-bottom: 1rem; padding: 0.5rem; border-left: 3px solid #0366d6;">
            <a href="{{ cs.url | relative_url }}" style="font-weight: bold; font-size: 1.1rem;">{{ cs.title }}</a>
            {% if cs.summary %}<div style="color: #586069; margin-top: 0.25rem;">{{ cs.summary }}</div>{% endif %}
          </li>
        {% endfor %}
      </ul>
    {% else %}
      <p style="color: #888; font-style: italic;">No case studies available yet.</p>
    {% endif %}
  </div>
</details>

{% endfor %}
