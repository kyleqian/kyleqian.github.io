---
layout: default
---

{% for p in site.projects %}
* {{ p.title }}
{% endfor %}
