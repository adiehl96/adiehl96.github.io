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
          <td>{{ item.author }} ({{ item.year }}). {{ item.title }}. doi: [{{ item.title }}](https://doi.org/{{ item.title }})</td>
        </tr>
      {% endif %}
    {% endfor %}
{% endfor %}
</table>
