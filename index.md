---
layout: default
---

{% for cat in site.category-list %}
### {{ cat }}
<ul>
  {% for page in site.pages %}
    {% if page.categories contains cat %}
      <li><a href="{{ page.url | prepend:site.baseurl }}">{{ page.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
{% endfor %}
