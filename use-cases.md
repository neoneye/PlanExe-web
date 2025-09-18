---
layout: planexe_empty_page
title: Use Cases
permalink: /use-cases/
---

<header class="post-header planexe-usecases-header">
  <span class="planexe-section__eyebrow">Use cases</span>
  <h1 class="post-title">PlanExe Use Cases</h1>
  <div class="header-description">
    <p class="subtitle">Describe your idea, budget, and constraints. PlanExe turns it into a plan with milestones, risks, and resources.</p>
    <p class="description">Explore a growing library of scenarios—from ambitious moonshots to pragmatic business plays—and reuse them as starting points for your own projects.</p>
  </div>
</header>

{% assign featured_cases = site.data.usecases | where: 'featured', true %}
{% assign regular_cases = site.data.usecases | where_exp: 'item', 'item.featured != true' %}

{% if featured_cases.size > 0 %}
<section class="planexe-section">
  <span class="planexe-section__eyebrow">Spotlight</span>
  <h2 class="planexe-section__title">Featured scenarios</h2>
  <div class="planexe-usecase-grid">
    {% for item in featured_cases %}
    <article class="planexe-card planexe-card--usecase">
      <span class="planexe-card__meta">Featured</span>
      <h3 class="planexe-card__title">{{ item.title }}</h3>
      <div class="planexe-card__body">
        {{ item.description | markdownify }}
      </div>
      <a class="planexe-link--arrow" href="{{ item.report_link | relative_url }}">View plan</a>
    </article>
    {% endfor %}
  </div>
</section>
{% endif %}

{% if regular_cases.size > 0 %}
<section class="planexe-section">
  <span class="planexe-section__eyebrow">Current library</span>
  <h2 class="planexe-section__title">Active scenarios</h2>
  <p class="planexe-section__lede">These plans showcase how PlanExe handles complex mandates, ethical trade-offs, and long-term programs. Use them as a template for your own planning sessions.</p>
  <div class="planexe-usecase-grid">
    {% for item in regular_cases %}
    <article class="planexe-card planexe-card--usecase">
      <span class="planexe-card__meta">Scenario</span>
      <h3 class="planexe-card__title">{{ item.title }}</h3>
      <div class="planexe-card__body">
        {{ item.description | markdownify }}
      </div>
      <a class="planexe-link--arrow" href="{{ item.report_link | relative_url }}">View plan</a>
    </article>
    {% endfor %}
  </div>
</section>
{% endif %}

{% assign legacy_cases = site.data.usecases_legacy %}
{% if legacy_cases and legacy_cases.size > 0 %}
<section class="planexe-section">
  <span class="planexe-section__eyebrow">Legacy</span>
  <h2 class="planexe-section__title">Archived downloads</h2>
  <p class="planexe-section__lede">Early experiments packaged as downloadable reports. They are preserved for reference and inspiration.</p>
  <div class="planexe-usecase-grid">
    {% for item in legacy_cases %}
    <article class="planexe-card planexe-card--usecase">
      <span class="planexe-card__meta">Download</span>
      <h3 class="planexe-card__title">{{ item.title }}</h3>
      <div class="planexe-card__body">
        {{ item.description | markdownify }}
      </div>
      <a class="planexe-link--arrow" href="{{ item.download_link }}">Download plan</a>
    </article>
    {% endfor %}
  </div>
</section>
{% endif %}
