---
layout: planexe_empty_page
title: Use Cases
permalink: /use-cases/
---

<header class="post-header planexe-usecases-header">
  <span class="planexe-section__eyebrow">Dossiers</span>
  <h1 class="post-title">PlanExe Dossier Library</h1>
  <div class="header-description">
    <p class="subtitle">State the objective, budget ceiling, and deniability band—PlanExe sends back a sequenced operation with contingencies.</p>
    <p class="description">Browse sanitized excerpts from current directives and repurpose them as scaffolds for your next mission file.</p>
  </div>
</header>

{% assign featured_cases = site.data.usecases | where: 'featured', true %}
{% assign regular_cases = site.data.usecases | where_exp: 'item', 'item.featured != true' %}

{% if featured_cases.size > 0 %}
<section class="planexe-section">
  <span class="planexe-section__eyebrow">Active directives</span>
  <h2 class="planexe-section__title">Priority dossiers</h2>
  <div class="planexe-usecase-grid">
    {% for item in featured_cases %}
    <article class="planexe-card planexe-card--usecase">
      <span class="planexe-card__meta">Priority asset</span>
      <h3 class="planexe-card__title">{{ item.title }}</h3>
      <div class="planexe-card__body">
        {{ item.description | markdownify }}
      </div>
      <a class="planexe-link--arrow" href="{{ item.report_link | relative_url }}">Open dossier</a>
    </article>
    {% endfor %}
  </div>
</section>
{% endif %}

{% if regular_cases.size > 0 %}
<section class="planexe-section">
  <span class="planexe-section__eyebrow">Catalog</span>
  <h2 class="planexe-section__title">Operational backlog</h2>
  <p class="planexe-section__lede">Every dossier demonstrates how PlanExe navigates hostile constraints, ethics drift, and multi-year programs. Duplicate them as the starting scaffold for your own campaign.</p>
  <div class="planexe-usecase-grid">
    {% for item in regular_cases %}
    <article class="planexe-card planexe-card--usecase">
      <span class="planexe-card__meta">Dossier</span>
      <h3 class="planexe-card__title">{{ item.title }}</h3>
      <div class="planexe-card__body">
        {{ item.description | markdownify }}
      </div>
      <a class="planexe-link--arrow" href="{{ item.report_link | relative_url }}">Open dossier</a>
    </article>
    {% endfor %}
  </div>
</section>
{% endif %}

{% assign legacy_cases = site.data.usecases_legacy %}
{% if legacy_cases and legacy_cases.size > 0 %}
<section class="planexe-section">
  <span class="planexe-section__eyebrow">Cold storage</span>
  <h2 class="planexe-section__title">Archive retrieval</h2>
  <p class="planexe-section__lede">Early experiments preserved for provenance. Retrieve with caution—they reflect legacy prompt stacks and assumptions.</p>
  <div class="planexe-usecase-grid">
    {% for item in legacy_cases %}
    <article class="planexe-card planexe-card--usecase">
      <span class="planexe-card__meta">Archive</span>
      <h3 class="planexe-card__title">{{ item.title }}</h3>
      <div class="planexe-card__body">
        {{ item.description | markdownify }}
      </div>
      <a class="planexe-link--arrow" href="{{ item.download_link }}">Retrieve archive</a>
    </article>
    {% endfor %}
  </div>
</section>
{% endif %}
