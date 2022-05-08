---
layout: page
permalink: /teaching/
title: Teaching
description: Teaching Positions @ Radboud University
academicyears: [2021-2022, 2020-2021]
---
{% for academicyear in page.academicyears %}
#### {{ academicyear }}
  {% assign teachings = site.teachings | reverse %}
  {% for item in teachings %}
    <table>
      {% if item.academicyear == academicyear %}
        <tr class="noBorder">
        <td>{{ item.position }}</td>
        <td>{{ item.coursename  }}</td>
        <td>Semester {{ item.semester }}</td>
      {% endif %}
    </table>
  {% endfor %}
{% endfor %}
