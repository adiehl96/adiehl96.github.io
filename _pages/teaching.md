---
layout: page
permalink: /misc/
title: Teaching
description: Teaching Assistant Positions @ Radboud University
---

To be updated soon

<div class="news">
  {% if site.teachings  %}
    <table>
    {% assign news = site.news | reverse %}
    {% for item in news limit: site.news_limit %}
      <tr>
        <td class="date">{{ item.date | date: "%b %-d, %Y" }}</td>
        <td class="announcement">
          {% if item.inline %}
            {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
          {% else %}
            <a class="news-title" href="{{ item.url | prepend: site.baseurl }}">{{ item.title }}</a>
          {% endif %}
        </td>
      </tr>
    {% endfor %}
    </table>
  {% else %}
    <p>No teaching positions so far...</p>
  {% endif %}
</div>
