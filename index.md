---
layout: default
redirect_from:
  - /projects
---

{% for p in site.projects %}
* [{{ p.title }}]({{p.url}})
{% endfor %}
