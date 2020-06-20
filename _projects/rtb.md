---
title: RTB
---
{% assign project = site.data.projects.rtb %}
{% assign company = site.data.companies[project.company] %}

## What is it?
An {{ project.short_name}} server is a high throughput and low latency web server.

## How was done?
Using languages:
{% for language in project.languages %}
* {{ language }}
{% endfor %}

Using frameworks:
{% for framework in project.frameworks %}
* {{ framework }}
{% endfor %}

Using external systems:
{% for external_system in project.external_systems %}
* {{ external_system }}
{% endfor %}
