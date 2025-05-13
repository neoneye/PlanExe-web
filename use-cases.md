---
layout: page
title: Use Cases
permalink: /use-cases/
---

PlanExe transforms abstract ideas into comprehensive, actionable plans.

{% for item in site.data.usecases %}
<div class="use-case-card">
<h2>{{ item.title }}</h2>
<p>{{ item.description | markdownify }}</p>
<a href="../{{ item.report_link }}">View Report</a>
</div>
{% endfor %}


{% for item in site.data.usecases_legacy %}
<div class="use-case-card">
<h2>{{ item.title }}</h2>
<p>{{ item.description | markdownify }}</p>
<a href="{{ item.download_link }}">Download zip</a>
</div>
{% endfor %}
