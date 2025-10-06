---
layout: planexe_empty_page
title: Homepage of PlanExe
---

<header class="post-header planexe-index-header">
<h1 class="post-title">Homepage of PlanExe</h1>
<div class="header-description">
    <p class="subtitle">PlanExe is a tool for making plans.</p>
    <p class="description">Try out your ideas.</p>
</div>
</header>

## What is it

- PlanExe is a planner, that can make plans from vague descriptions.
- Open source, MIT license. You can modify the python code or the report template.
- Uses LlamaIndex so the AI provider can be changed, such as OpenRouter, Ollama, LM Studio.

## Why use it

- Save money. Don't fund doomed projects.
- Save time. It's time consuming to manually create a plan.
- Avoid surprises. Uncover pitfalls early.

## How to use it

- If you are not a developer. [Try it here](https://app.mach-ai.com/planexe_early_access).
- If you are a developer, you can install PlanExe on your own computer.

## Example plan

{% for item in site.data.examples %}
{% if item.featured %}
<div class="examples-card">
<h2>{{ item.title }}</h2>
{% if item.description %}
<div class="examples-card-description">
{{ item.description | markdownify }}
</div>
{% endif %}
<div class="examples-card-prompt">{{ item.prompt | markdownify }}</div>
<a class="examples-card-arrow-link" href="{{ item.report_link }}">View Plan</a>
</div>
{% endif %}
{% endfor %}

## Get involved

Introduce yourself on the PlanExe Discord and ask how you can help.

- Python developer, tweak most of the code.
- Prompt engineer, make changes to the system prompts for different responses.
- Project manager, for feedback about what is missing in the report. 
- Designer, make the report look nicer.
