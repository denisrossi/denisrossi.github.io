---
title: RTB
---
{% assign project = site.data.projects.rtb %}
{% assign company = site.data.companies[project.company] %}
At [{{ company.name }}]({{ company.url }})
> {{ company.date_start }} - {{ company.date_end }}

## What is it?
{{ project.description }}

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
