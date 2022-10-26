---
layout: page
permalink: /publications/
title: Publications
description:
years: [2022, 2021]
types: [conference, software]
---

{% for type in page.types %}
  <table>
  {% if type == "conference" %}
    <b>Conference Publications</b>
  {% endif %}
  {% if type == "software" %}
    <b>Open Source Software</b>
  {% endif %}
  {% for year in page.years %}
  <!-- #### {{ year }} -->
    {% assign publications = site.publications | reverse %}
      {% for item in publications %}
        {% if item.type == type %}
          {% if item.year == year %}
            {% if type == "conference" %}
              <tr class="noBorder">
                <td>{{ item.author }} ({{ item.year }}). <i>{{ item.title }}</i>. {{ item.venue }}. <a href="https://doi.org/{{ item.doi }}">publication</a> | <a href="/assets/pdf/{{ item.pdf }}">pdf</a> | <a href="{{ item.code }}">code</a> | <a href="/assets/pdf/{{ item.poster }}">poster</a> | <a href="/assets/bibtex/{{ item.bib }}">bib</a> </td>
              </tr>
            {% endif %}
            {% if type == "software" %}
              <tr class="noBorder">
                <td><i>{{ item.title }}</i>. ({{ item.year }}). <a href="https://doi.org/{{ item.doi }}">doi</a> | <a href="{{ item.code }}">code</a> </td>
              </tr>
            {% endif %}
          {% endif %}
        {% endif %}
      {% endfor %}
  {% endfor %}
  </table>
{% endfor %}

