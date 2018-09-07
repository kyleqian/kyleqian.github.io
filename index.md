---
layout: default
redirect_from:
  - /projects
---

{% assign sorted_projects = site.projects | sort:"order_" %}

{% for p in sorted_projects %}
  <div class="project-preview">
    <a href="{{ p.url }}"><img class="index-img" src="{{ site.url }}{{ p.prev_img_ }}"></a>
    <center>
      <strong>{{ p.title }}</strong>
      <br>
      <small class="prev-desc">{{ p.prev_desc_ }}</small>
    </center>
  </div>
{% endfor %}
