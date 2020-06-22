{% assign project = site.data.projects[include.project] %}
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

## Tools
{% if project.tools.languages %}
### Languages
{% for language in project.tools.languages %}
* {{ site.data.tools.languages[language].name }}
{% endfor %}
{% endif %}

{% if project.tools.libraries %}
### Libraries
{% for library in project.tools.libraries %}
* {{ site.data.tools.libraries[library].name }}
{% endfor %}
{% endif %}

{% if project.tools.external_systems %}
### External systems
{% for external_system in project.tools.external_systems %}
* {{ site.data.tools.external_systems[external_system].name }}
{% endfor %}
{% endif %}