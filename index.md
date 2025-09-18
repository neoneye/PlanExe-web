---
layout: planexe_empty_page
title: Homepage of PlanExe
---

<div class="planexe-hero">
  <div class="planexe-hero__content">
    <span class="planexe-badge">AI planning assistant</span>
    <h1>PlanExe turns ambitious ideas into structured action plans</h1>
    <p>Give PlanExe a direction, a budget, and constraints. Receive a complete plan with milestones, risks, and resourcing you can execute.</p>
    <div class="planexe-hero__actions">
      <a class="planexe-button planexe-button--primary" href="https://app.mach-ai.com/planexe_early_access" target="_blank" rel="noopener">Try the early access</a>
      <a class="planexe-button planexe-button--ghost" href="{{ '/use-cases/' | relative_url }}">Browse example plans</a>
    </div>
    <ul class="planexe-hero__highlights">
      <li>Open source under the MIT license</li>
      <li>Swap between OpenRouter, Ollama, LM Studio, and more</li>
      <li>Fine-tune prompts, templates, and reports to your workflow</li>
    </ul>
  </div>
  {% assign featured_case = site.data.usecases | where: 'featured', true | first %}
  {% if featured_case %}
  <div class="planexe-hero__card">
    <span class="planexe-section__eyebrow">Featured scenario</span>
    <h2>{{ featured_case.title }}</h2>
    <div class="planexe-card__body">
      {{ featured_case.description | markdownify }}
    </div>
    <a class="planexe-link--arrow" href="{{ featured_case.report_link | relative_url }}">View plan</a>
  </div>
  {% endif %}
</div>

<section class="planexe-section">
  <span class="planexe-section__eyebrow">Why PlanExe</span>
  <h2 class="planexe-section__title">Bring clarity to messy problem statements</h2>
  <p class="planexe-section__lede">PlanExe analyses vague direction, budgets, time horizons, and constraints to produce structured plans with milestones, dependencies, and risk mitigation.</p>
  <div class="planexe-feature-grid">
    <article class="planexe-feature-card">
      <h3>Understand the landscape</h3>
      <p>Feed PlanExe the backstory and it highlights hidden risks, resources, and decision points before work begins.</p>
    </article>
    <article class="planexe-feature-card">
      <h3>Move faster together</h3>
      <p>Share repeatable plan templates with your team, then adjust prompts and outputs to match your internal processes.</p>
    </article>
    <article class="planexe-feature-card">
      <h3>Choose your AI provider</h3>
      <p>Powered by LlamaIndex so you can run PlanExe with OpenRouter, Ollama, LM Studio, or your preferred stack.</p>
    </article>
  </div>
</section>

<section class="planexe-section">
  <span class="planexe-section__eyebrow">Get started</span>
  <h2 class="planexe-section__title">Use PlanExe your way</h2>
  <div class="planexe-feature-grid">
    <article class="planexe-feature-card">
      <h3>Non-developers</h3>
      <p>Use the hosted experience and generate plans in the browser—no installation required.</p>
      <a class="planexe-link--arrow" href="https://app.mach-ai.com/planexe_early_access" target="_blank" rel="noopener">Launch early access</a>
    </article>
    <article class="planexe-feature-card">
      <h3>Developers</h3>
      <p>Clone the repository, customize the prompts or report templates, and run PlanExe locally.</p>
      <a class="planexe-link--arrow" href="{{ '/github.html' | relative_url }}">See the source code</a>
    </article>
  </div>
</section>

<section class="planexe-section">
  <span class="planexe-section__eyebrow">Example output</span>
  <h2 class="planexe-section__title">Explore the latest generated plans</h2>
  {% assign showcased_cases = site.data.usecases | slice: 0, 3 %}
  <div class="planexe-usecase-grid">
    {% for item in showcased_cases %}
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
  <a class="planexe-link--arrow" href="{{ '/use-cases/' | relative_url }}">Browse all use cases</a>
</section>

<section class="planexe-section">
  <span class="planexe-section__eyebrow">Community</span>
  <h2 class="planexe-section__title">Help shape where PlanExe goes next</h2>
  <div class="planexe-feature-grid">
    <article class="planexe-feature-card">
      <h3>Python &amp; full-stack contributors</h3>
      <p>Improve the core engine, integrate additional AI providers, or evolve the report structure.</p>
    </article>
    <article class="planexe-feature-card">
      <h3>Prompt engineers &amp; domain experts</h3>
      <p>Create better prompt scaffolds and datasets for niche industries or complex risk profiles.</p>
    </article>
    <article class="planexe-feature-card">
      <h3>Designers &amp; operators</h3>
      <p>Polish the UI, challenge the output format, and share feedback from real-world usage.</p>
    </article>
  </div>
  <p class="planexe-section__lede">Join the conversation on Discord and let us know what plan you want to generate next.</p>
  <a class="planexe-link--arrow" href="{{ '/discord.html' | relative_url }}">Join the Discord server</a>
</section>
