---
layout: page
permalink: /publications/
title: Publications
description:
years: [2022, 2021]
---

<table>
{% for year in page.years %}
  lel
<!-- #### {{ year }} -->
  {% assign publications = site.publications | reverse %}
    {% for item in publications %}
      {% if item.year == year %}
        <tr class="noBorder">
          <td>{{ item.author }}</td>
          <td>{{ item.year }}</td>
          <td>{{ item.title  }}</td>
        </tr>
      {% endif %}
    {% endfor %}
{% endfor %}
</table>
