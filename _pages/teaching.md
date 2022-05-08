---
layout: page
permalink: /teaching/
title: Teaching
description: Teaching Positions @ Radboud University
academicyears: [21-22, 20-21, 21-22]
---
{% for academicyear in page.academicyears %}
#### {{ academicyear }}
  <table>
  {% assign teachings = site.teachings | reverse %}
  {% for item in teachings %}
    {% if item.academicyear == academicyear %}
      <tr class="noBorder">
        <td>{{ item.position }}</td>
        <td>{{ item.coursename  }}</td>
        <td>Semester {{ item.semester }}</td>
      </tr>
    {% endif %}
  {% endfor %}
  </table>
{% endfor %}
