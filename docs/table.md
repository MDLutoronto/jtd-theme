---
title: Read a table from CSV
layout: page
nav_order: 2
description: 
last_modified_date: 2025-10-14
parent: Home
---
# Data from CSV

{% assign csv_data = site.data.data %}

<table>
  <thead>
    <tr>
      {% for header in csv_data.first %}
        <th>{{ header[0] }}</th>
      {% endfor %}
    </tr>
  </thead>
  <tbody>
    {% for row in csv_data %}
      <tr>
        {% for cell in row %}
          <td>{{ cell[1] }}</td>
        {% endfor %}
      </tr>
    {% endfor %}
  </tbody>
</table>