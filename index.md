---
layout: home
title: Transform your ideas into actionable plans
---

PlanExe is a free and open-source planning assistant.

Describe your project, run PlanExe for 10-20 minutes and read the generated plan.

---

# Featured Use Case

{% for item in site.data.usecases %}
{% if item.featured %}
<div class="use-case-card">
<h2>{{ item.title }}</h2>
<p>{{ item.description | markdownify }}</p>
<a class="use-case-card-arrow-link" href="{{ item.report_link }}">View Plan</a>
</div>
{% endif %}
{% endfor %}

---

# Latest News
