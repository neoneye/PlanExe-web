---
layout: planexe_empty_page
title: Use Cases
permalink: /use-cases/
---

<div class="use-cases-header">
    <h1>The most recent use cases of PlanExe</h1>
    <p>Click <strong>View Report</strong> to see the comprehensive plans.</p>
</div>

{% for item in site.data.usecases %}
<div class="use-case-card">
<h2>{{ item.title }}</h2>
<p>{{ item.description | markdownify }}</p>
<a class="use-case-card-arrow-link" href="../{{ item.report_link }}">View Report</a>
</div>
{% endfor %}


{% for item in site.data.usecases_legacy %}
<div class="use-case-card">
<h2>{{ item.title }}</h2>
<p>{{ item.description | markdownify }}</p>
<a href="{{ item.download_link }}">Download zip</a>
</div>
{% endfor %}
