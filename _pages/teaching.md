---
layout: page
permalink: /teaching/
title: Teaching
description: Teaching Positions @ Radboud University
academicyears: [2022-2023, 2021-2022, 2020-2021]
---
<table>
{% for academicyear in page.academicyears %}
<!-- #### {{ academicyear }} -->
  {% assign teachings = site.teachings | reverse %}
    {% for item in teachings %}
      {% if item.academicyear == academicyear %}
        <tr class="noBorder">
          <td>{{ item.academicyear }}</td>
          <td>{{ item.position }}</td>
          <td>{{ item.coursename  }}</td>
        </tr>
      {% endif %}
    {% endfor %}
{% endfor %}
</table>
