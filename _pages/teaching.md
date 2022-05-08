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
    {% if item.year == year %}
      <tr class="noBorder">
        <td>Semester {{ item.semester }}</td>
        <td>{{ item.position }}</td>
        <td>{{ item.coursename  }}</td>
      </tr>
    {% endif %}
  {% endfor %}
  </table>
{% endfor %}
