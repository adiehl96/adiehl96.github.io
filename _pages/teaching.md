---
layout: page
permalink: /teaching/
title: Teaching
description: Teaching Positions @ Radboud University
years: [2022, 2021]
---
{% for year in page.years %}
#### {{ year }}
  <table>
  {% assign teachings = site.teachings | reverse %}
  {% for item in teachings %}
    {% if item.year == year %}
      <tr class="noBorder">
        <td>{{ item.position }}</td>
        <td>{{ item.coursename  }}</td>
        <td>Semester {{ item.semester }}</td>
      </tr>
    {% endif %}
  {% endfor %}
  </table>
{% endfor %}
