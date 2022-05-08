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
    {% if item.academicyear == academicyear %}
      {{ item.position }}, {{ item.coursename  }}, Semester {{ item.semester }}
    {% endif %}
  {% endfor %}
{% endfor %}
