---
layout: post
title: "The Output Dir"
date: 2025-02-20
---

When PlanExe is running, many files are created in the output dir. What are those files?

<br>

Here I'm explaining the purpose of these files.

<iframe width="560" height="315" src="https://www.youtube.com/embed/7AM2F1C4CGI?si=omxCdGIuJ-lMmW8e" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<br>

## Enumerated files

The filenames are prefixed with 3 digits, like this:

```
001-plan.txt
002-1-make_assumptions_raw.json
002-2-make_assumptions.json
003-distill_assumptions.json
004-1-pre_project_assessment_raw.json
004-2-pre_project_assessment.json
005-project_plan.json
006-1-find_team_members_raw.json
006-2-find_team_members.json
007-1-enrich_team_members_contract_type_raw.json
007-2-enrich_team_members_contract_type.json
008-1-enrich_team_members_background_story_raw.json
008-2-enrich_team_members_background_story.json
009-1-enrich_team_members_environment_info_raw.json
009-2-enrich_team_members_environment_info.json
010-review_team_raw.json
011-team.md
012-1-swot_analysis_raw.json
012-2-swot_analysis.md
013-1-experts_raw.json
013-2-experts.json
014-1-1-expert_criticism_raw.json
014-1-2-expert_criticism_raw.json
014-2-expert_criticism.md
015-1-wbs_level1_raw.json
015-2-wbs_level1.json
016-1-wbs_level2_raw.json
016-2-wbs_level2.json
017-wbs_project_level1_and_level2.json
018-1-pitch_raw.json
018-2-pitch_to_markdown_raw.json
018-3-pitch.md
019-task_dependencies_raw.json
020-1-1-task_durations_raw.json
020-1-2-task_durations_raw.json
020-1-3-task_durations_raw.json
020-2-task_durations.json
021-1-1-wbs_level3_raw.json
021-1-2-wbs_level3_raw.json
021-1-3-wbs_level3_raw.json
021-1-4-wbs_level3_raw.json
021-2-wbs_level3.json
021-3-wbs_project_level1_and_level2_and_level3.json
021-4-wbs_project_level1_and_level2_and_level3.csv
022-report.html
999-pipeline_complete.txt
log.txt
```

### What are `raw` files?

The filename usually ends with `_raw.json`.

```
002-1-make_assumptions_raw.json
004-1-pre_project_assessment_raw.json
006-1-find_team_members_raw.json
007-1-enrich_team_members_contract_type_raw.json
008-1-enrich_team_members_background_story_raw.json
009-1-enrich_team_members_environment_info_raw.json
010-review_team_raw.json
```

The `raw` files contains the raw response from the LLM. 
Some extra fields such as `metadata`, `user_prompt`, `system_prompt` are sometimes present.

Having access to all this info is helpful when debugging.

### What are `clean` files?

The filename does NOT end with `_raw.json`.

```
001-plan.txt
002-2-make_assumptions.json
003-distill_assumptions.json
004-2-pre_project_assessment.json
005-project_plan.json
006-2-find_team_members.json
007-2-enrich_team_members_contract_type.json
008-2-enrich_team_members_background_story.json
009-2-enrich_team_members_environment_info.json
011-team.md
012-2-swot_analysis.md
013-2-experts.json
```

The `raw` data has been post-processed and cleaned up, the result is stored in a `clean` file.
The LLMs are very sensitive to the naming of fields. So in the `raw` file a field may have one name,
and in the `clean` file the field may have a cleaned up field name.

### What is the `log.txt` file?

This is the output from python's logger with `DEBUG` level.
It may be helpful when troubleshooting.
It may contain sensitive data such as your API keys, IP address. So don't share it with anyone.
