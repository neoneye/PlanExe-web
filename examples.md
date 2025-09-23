---
layout: planexe_empty_page
title: Examples
permalink: /examples/
---

<header class="post-header planexe-examples-header">
<h1 class="post-title">PlanExe Use Cases</h1>
<div class="header-description">
    <p class="subtitle">Describe your idea, budget, location. PlanExe turns it into a plan.</p>
    <p class="description">A starting point for those who’d rather not begin with a blank page.</p>
</div>
</header>

{% for item in site.data.examples %}
<div class="examples-card">
<h2>{{ item.title }}</h2>
<p>{{ item.description | markdownify }}</p>
<a class="examples-card-arrow-link" href="../{{ item.report_link }}">View Plan</a>
</div>
{% endfor %}


{% for item in site.data.examples_legacy %}
<div class="examples-card">
<h2>{{ item.title }}</h2>
<p>{{ item.description | markdownify }}</p>
<a href="{{ item.download_link }}">Download Plan</a>
</div>
{% endfor %}
