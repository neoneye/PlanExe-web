---
layout: page
title: Use Cases
permalink: /use-cases/
---

PlanExe transforms abstract ideas into comprehensive, actionable plans.

{% for use_case in site.data.usecases %}
## {{ use_case.title }}

{{ use_case.description | markdownify }}

[View Report](../{{ use_case.report_link }})

{% endfor %}


{% for use_case in site.data.usecases_legacy %}
## {{ use_case.title }}

{{ use_case.description | markdownify }}

[Download zip]({{ use_case.download_link }})

{% endfor %}
