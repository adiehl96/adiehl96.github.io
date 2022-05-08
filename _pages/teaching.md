---
layout: page
permalink: /teaching/
title: Teaching
description: Teaching Positions @ Radboud University
years: [2021, 2020]
---
{% for year in page.years %}
#### {{ year }}
  <table>
  {% assign teachings = site.teachings | reverse %}
  {% for item in teachings %}
  {{ item.coursename }}
    {% if item.year == year %}
      {{ item.position }}
      <tr class="noBorder">
        <td>{{ item.position }}</td>
        <td>{{ item.coursename  }}</td>
        <td>Semester {{ item.semester }}</td>
      </tr>
    {% endif %}
  {% endfor %}
  </table>
{% endfor %}
