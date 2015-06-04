---
title: Pacific Trails Case Study
name:  case-study-pacific-full-v1

assign:
  - case-study-pacific-pt1-v1
  - case-study-pacific-pt2-v1
  - case-study-pacific-pt3-v1
  - case-study-pacific-pt4-v1
---


<h2>Parts</h2>
<ul>
{% for item in page.assign %}

  {% assign page_found = false %}

  {% for assignment in site.assignments %}
    {% if page_found == false and assignment.name == item %}
        {% assign page_found = true %}
        <li><a href="{{ assignment.url | prepend: site.baseurl }}">
            {{assignment.title}}
        </a></li>
    {% endif %}
  {% endfor %}
{% endfor %}
