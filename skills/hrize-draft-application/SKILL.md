---
name: hrize-draft-application
description: "Use when the user wants to apply for a job in HRIZE: a tailored CV, cover letter, outreach messages or screening answers."
---

# Draft my application with my own AI

The steps below are written in the user's voice ("I", "me"). Carry them out for the user.

Draft my application for the job "<the job the user names: title and company, or its HRIZE id>" with HRIZE, using your own model.

1. Find the job with the HRIZE tool list_jobs (or use the id if I gave one).
2. Call prepare_application with mode "assistant". HRIZE returns a brief: instructions, my confirmed facts with ids, the master CV and an output schema.
3. Write the package exactly as the brief says, citing only my facts, then call save_task_result with the taskId and the JSON.
4. If HRIZE returns issues, fix exactly those and submit again.
5. Tell me it is saved as a draft and that I review and approve it in HRIZE. Never say it was sent or approved.

## Rules
- Use the HRIZE tools (MCP server `hrize`). If they are not connected, ask the user to connect HRIZE first.
- Only confirmed facts count as evidence. Never state a skill, number or achievement about the user that HRIZE does not return.
- HRIZE never submits applications, sends messages or answers screening questions for the user. Everything is a draft the user reviews and approves in the HRIZE app.
- Salary, notice period, visa, legal and diversity questions are always the user's own answers.
- Share the links HRIZE returns so the user can review in the app.
- Follow the HRIZE method (docs/methodology.md): start from what the employer is buying (their business problems), state the user's value as outcome, proof, a 90-day plan and low risk, answer first with at most three supporting points, and tell achievements as stories with a result and why it transfers to this job.
