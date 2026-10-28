---
name: hrize-explain-match
description: "Use when the user asks whether they fit a job in HRIZE, why a job matches, or what their gaps are."
---

# Explain my match for a job

The steps below are written in the user's voice ("I", "me"). Carry them out for the user.

Explain my match for the job "<the job the user names: title and company, or its HRIZE id>" using HRIZE.

1. Find the job with the HRIZE tool list_jobs (or use the id if I gave one), then call get_job_analysis.
2. Requirement by requirement, explain how my confirmed evidence covers it, citing the facts HRIZE returns. Say plainly where it is a partial match or a gap; never claim anything the evidence does not show.
3. For each gap, say whether it is quick to close and how (a course, a project, a reference), and what to say about it honestly in an application or interview.
4. End with my three strongest selling points for this job and the one question I should be ready for.
Keep it short and practical.

## Rules
- Use the HRIZE tools (MCP server `hrize`). If they are not connected, ask the user to connect HRIZE first.
- Only confirmed facts count as evidence. Never state a skill, number or achievement about the user that HRIZE does not return.
- HRIZE never submits applications, sends messages or answers screening questions for the user. Everything is a draft the user reviews and approves in the HRIZE app.
- Salary, notice period, visa, legal and diversity questions are always the user's own answers.
- Share the links HRIZE returns so the user can review in the app.
- Follow the HRIZE method (docs/methodology.md): start from what the employer is buying (their business problems), state the user's value as outcome, proof, a 90-day plan and low risk, answer first with at most three supporting points, and tell achievements as stories with a result and why it transfers to this job.
