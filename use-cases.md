---
layout: planexe_empty_page
title: Use Cases
permalink: /use-cases/
---

<header class="post-header">
<h1 class="post-title">The most recent use cases of PlanExe</h1>
<div class="header-description">
    <p class="subtitle">You provide a description of your idea. PlanExe transforms your idea into a plan.</p>
    <p class="description">Below are examples plans made with PlanExe.</p>
</div>
</header>

<div class="use-cases-header">
    <h1>The most recent use cases of PlanExe</h1>
    <!-- <p>These are AI generated plans.</p> -->
    <p>These are the prompts, the report is the corrsponding AI generated plans.</p>
</div>

{% for item in site.data.usecases %}
<div class="use-case-card">
<h2>{{ item.title }}</h2>
<p>{{ item.description | markdownify }}</p>
<a class="use-case-card-arrow-link" href="../{{ item.report_link }}">View Plan</a>
</div>
{% endfor %}


{% for item in site.data.usecases_legacy %}
<div class="use-case-card">
<h2>{{ item.title }}</h2>
<p>{{ item.description | markdownify }}</p>
<a href="{{ item.download_link }}">Download zip</a>
</div>
{% endfor %}
