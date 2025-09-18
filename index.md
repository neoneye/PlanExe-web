---
layout: planexe_empty_page
title: Homepage of PlanExe
---

<div class="planexe-hero">
  <div class="planexe-hero__content">
    <span class="planexe-badge">Operational directive engine</span>
    <h1>PlanExe codifies high-risk directives into controlled execution</h1>
    <p>Feed PlanExe unstable mandates, hard budgets, and political redlines. It returns staged operations with traceable checkpoints, escalation windows, and executive-ready debriefs.</p>
    <div class="planexe-hero__actions">
      <a class="planexe-button planexe-button--primary" href="https://app.mach-ai.com/planexe_early_access" target="_blank" rel="noopener">Request clearance</a>
      <a class="planexe-button planexe-button--ghost" href="{{ '/use-cases/' | relative_url }}">Review sample dossiers</a>
    </div>
    <ul class="planexe-hero__highlights">
      <li>Hardened dossier exports with embedded audit trails and risk bands.</li>
      <li>Swap between isolated OpenRouter, Ollama, or LM Studio stacks without leakage.</li>
      <li>Custom kill-chain templates, redaction rules, and escalation defaults.</li>
    </ul>
  </div>
  {% assign featured_case = site.data.usecases | where: 'featured', true | first %}
  {% if featured_case %}
  <div class="planexe-hero__card">
    <span class="planexe-section__eyebrow">Active dossier</span>
    <h2>{{ featured_case.title }}</h2>
    <div class="planexe-card__body">
      {{ featured_case.description | markdownify }}
    </div>
    <a class="planexe-link--arrow" href="{{ featured_case.report_link | relative_url }}">Open dossier</a>
  </div>
  {% endif %}
</div>

<section class="planexe-section">
  <span class="planexe-section__eyebrow">Rationale</span>
  <h2 class="planexe-section__title">Impose order on volatile directives</h2>
  <p class="planexe-section__lede">PlanExe cross-references budgets, politics, and risk tolerance to turn ambiguous commands into accountable roadmaps you can defend under scrutiny.</p>
  <div class="planexe-feature-grid">
    <article class="planexe-feature-card">
      <h3>Surface destabilizers</h3>
      <p>Fuse backstory, intelligence notes, and constraints to expose silent dependencies, civic flashpoints, and supply shocks before the mission launches.</p>
    </article>
    <article class="planexe-feature-card">
      <h3>Synchronize sealed teams</h3>
      <p>Distribute templated plans across compartmentalized crews while keeping prompts, redlines, and approvals aligned with oversight policy.</p>
    </article>
    <article class="planexe-feature-card">
      <h3>Control your intelligence stack</h3>
      <p>Leverage the LlamaIndex core to switch between OpenRouter, Ollama, LM Studio, or isolated endpoints without leaking context.</p>
    </article>
  </div>
</section>

<section class="planexe-section">
  <span class="planexe-section__eyebrow">Deployment</span>
  <h2 class="planexe-section__title">Select your deployment perimeter</h2>
  <div class="planexe-feature-grid">
    <article class="planexe-feature-card">
      <h3>Operators</h3>
      <p>Leverage the hosted console with managed isolation. Generate sanitized dossiers from secured browsers—no local install.</p>
      <a class="planexe-link--arrow" href="https://app.mach-ai.com/planexe_early_access" target="_blank" rel="noopener">Enter hosted console</a>
    </article>
    <article class="planexe-feature-card">
      <h3>Engineers</h3>
      <p>Clone the repository, wire your preferred model endpoints, harden the prompts, and run PlanExe within your own enclave.</p>
      <a class="planexe-link--arrow" href="{{ '/github.html' | relative_url }}">Review the source</a>
    </article>
  </div>
</section>

<section class="planexe-section">
  <span class="planexe-section__eyebrow">Dossier feed</span>
  <h2 class="planexe-section__title">Inspect the latest sanctioned dossiers</h2>
  {% assign showcased_cases = site.data.usecases | slice: 0, 3 %}
  <div class="planexe-usecase-grid">
    {% for item in showcased_cases %}
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
  <a class="planexe-link--arrow" href="{{ '/use-cases/' | relative_url }}">Browse the full library</a>
</section>

<section class="planexe-section">
  <span class="planexe-section__eyebrow">Network</span>
  <h2 class="planexe-section__title">Join the quiet network behind PlanExe</h2>
  <div class="planexe-feature-grid">
    <article class="planexe-feature-card">
      <h3>Protocol engineers</h3>
      <p>Strengthen the orchestration core, extend data isolation layers, and stress-test the reporting surface.</p>
    </article>
    <article class="planexe-feature-card">
      <h3>Scenario architects</h3>
      <p>Design directive scaffolds and datasets for contentious industries, geopolitics, and asymmetric threats.</p>
    </article>
    <article class="planexe-feature-card">
      <h3>Operations liaisons</h3>
      <p>Audit the UI, push for brutal honesty in reporting, and circulate field intelligence from live deployments.</p>
    </article>
  </div>
  <p class="planexe-section__lede">Access is invite-gated. Share field feedback, red-team notes, and next directives inside the sealed channel.</p>
  <a class="planexe-link--arrow" href="{{ '/discord.html' | relative_url }}">Request Discord access</a>
</section>
