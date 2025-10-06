---
layout: planexe_empty_page
title: Examples
permalink: /examples/
---

<header class="post-header planexe-examples-header">
<h1 class="post-title">Example Plans</h1>
<div class="header-description">
    <p class="subtitle">See what PlanExe can create from a project description.</p>
    <p class="description">A plan include tasks, timeline, risks, dependencies and staffing.</p>
</div>
</header>

{% for item in site.data.examples %}
<div class="examples-card">
<h2>{{ item.title }}</h2>
<p>{{ item.prompt | markdownify }}</p>
<a class="examples-card-arrow-link" href="../{{ item.report_link }}">View Plan</a>
</div>
{% endfor %}


{% for item in site.data.examples_legacy %}
<div class="examples-card">
<h2>{{ item.title }}</h2>
<p>{{ item.prompt | markdownify }}</p>
<a href="{{ item.download_link }}">Download Plan</a>
</div>
{% endfor %}
