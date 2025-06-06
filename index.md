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
- Uses LlamaIndex so the LLM provider can be changed, such as OpenRouter, Ollama, LM Studio.

## Why use it

- Save time. It's time consuming to manually create a plan.
- Discover risks before they happen. Mistakes can be expensive.
- Get rough estimates of what resources are needed.

## How to use it

- Currently PlanExe is hard to use.
- You need to be a developer or find a developer that can help you.
- Ask on the PlanExe Discord for help.

## Example plan

{% for item in site.data.usecases %}
{% if item.featured %}
<div class="use-case-card">
<h2>{{ item.title }}</h2>
<p>{{ item.description | markdownify }}</p>
<a class="use-case-card-arrow-link" href="{{ item.report_link }}">View Plan</a>
</div>
{% endif %}
{% endfor %}

More plans: [Here]({{ '/use-cases/'  | relative_url}}).

## Get involved

Introduce yourself on the PlanExe Discord and ask how you can help.

- Python developer, tweak most of the code.
- Prompt engineer, make changes to the system prompts for different responses.
- Project manager, for feedback about what is missing in the report. 
- Designer, make the report look nicer.
