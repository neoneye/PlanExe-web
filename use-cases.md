---
layout: planexe_empty_page
title: Use Cases
permalink: /use-cases/
---

<div class="use-cases-header">
    <h1>Transform Your Vision Into Reality</h1>
    <p>PlanExe transforms abstract ideas into comprehensive, actionable plans. From <span class="highlight">lunar bases</span> to <span class="highlight">sustainable food systems</span>, we help you navigate complex challenges with confidence and precision.</p>
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
