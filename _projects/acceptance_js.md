---
title: JavaScript Acceptance Tests
---
{% assign project = site.data.projects.acceptance_js %}
{% if project.company %}
{% assign company = site.data.companies[project.company] %}
At [{{ company.name }}]({{ company.url }})
> {{ company.date_start }} - {{ company.date_end }}
{% else %}
At [home]({{project.url}})
{% endif %}

## What is it?
{{ project.description }}

{% unless project.company %}
Check the deliverable <a href="{{ project.deliverable }}" target="_blank">here</a>
{% endunless %}

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
