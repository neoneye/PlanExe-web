---
layout: page
title: Use Cases
permalink: /use-cases/
---

PlanExe transforms abstract ideas into comprehensive, actionable plans.

{% for use_case in site.data.usecases %}
## {{ use_case.title }}

{{ use_case.description | markdownify }}

[View Report]({{ use_case.report_link }})

{% endfor %}


## Arxiv distillation

Distill Arxiv papers into an objective, hype-free summary that indicates whether improvements are truly significant or just noise. Compare claims with benchmarks, flag inflated gains, and foster a clear, evidence-based understanding of machine learning progress without marketing language. To make the distilled data available with minimal upkeep and maximum longevity, publish these summaries as an open-access dataset on a well-established repository.

[20250210_arxiv_distillation.zip](https://github.com/neoneye/PlanExe-web/raw/refs/heads/main/20250210_arxiv_distillation.zip)

## Puzzle restaurant

I want to make a restaurant for puzzle solving happy people. An important part is that humans are solving puzzles with each other. While having something to drink and eat.

[20250209_puzzle_restaurant.zip](https://github.com/neoneye/PlanExe-web/raw/refs/heads/main/20250209_puzzle_restaurant.zip)

## Lunar base

Manned moon mission, for establishing a permanent base.

[20250209_lunar_base.zip](https://github.com/neoneye/PlanExe-web/raw/refs/heads/main/20250209_lunar_base.zip)

## Global language

I'm envisioning a streamlined global language—free of archaic features like gendered terms and excessive suffixes, taking cues from LLM tokenization. Some regions might only choose to adopt certain parts of this modern language. Would humanity ultimately benefit more from preserving many distinct languages, or uniting around a single, optimized one?

[20250209_global_language.zip](https://github.com/neoneye/PlanExe-web/raw/refs/heads/main/20250209_global_language.zip)

## US-Mexico canal

US-Mexico canal. I want to build a canal along USA's southern border to mexico, so that containers no longer have to go all the way to Panama. Also this would help with southern border security.

[20250208_us_mexico_canal.zip](https://github.com/neoneye/PlanExe-web/raw/refs/heads/main/20250208_us_mexico_canal.zip)
