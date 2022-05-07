---
layout: page
permalink: /misc/
title: Teaching
description: Teaching Assistant Positions @ Radboud University
years: [2021, 2020]
---
{% for year in page.years %}
#### {{ year }}
  <table>
  {% assign teachings = site.teachings | reverse %}
  {% for item in teachings %}
    {% if item.year == year %}
      <tr class="noBorder">
        <td class="date">{{ item.date | date: "%b %-d, %Y" }}</td>
        <td class="announcement">
          {% if item.inline %}
            {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
          {% else %}
            <a class="news-title" href="{{ item.url | prepend: site.baseurl }}">{{ item.title }}</a>
          {% endif %}
        </td>
      </tr>
    {% endif %}
  {% endfor %}
  </table>
{% endfor %}
