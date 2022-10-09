---
layout: page
permalink: /publications/
title: Publications
description:
years: [2022, 2021]
---

<table>
{% for year in page.years %}
<!-- #### {{ year }} -->
  {% assign publications = site.publications | reverse %}
    {% for item in publications %}
      {% if item.year == year %}
        <tr class="noBorder">
          <td>{{ item.author }} ({{ item.year }}). {{ item.title }}. doi: <a href="https://doi.org/{{ item.doi }}">{{ item.doi }}</a> | <a href="/assets/pdf/{{ item.pdf }}">pdf</a> | <a href="{{ item.code }}">code</a> </td>
        </tr>
      {% endif %}
    {% endfor %}
{% endfor %}
</table>

