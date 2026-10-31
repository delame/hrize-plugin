---
name: hrize-application-pipeline
description: "Use when the user wants to work on their job applications, asks what to do next, which job to apply to, or wants help filling an employer's application form."
---

# Work through my applications

The steps below are written in the user's voice ("I", "me"). Carry them out for the user.

Work through my job applications with me, using HRIZE.

1. Call get_pipeline. Tell me in a few lines what is on my board and what is due today, then suggest the one job to work on now.
2. For that job, follow the HRIZE steps, one at a time, and wait for me after each:
   a. Fit and link: read get_job_analysis. Tell me the fit, the top gap, and whether the posting is still open (ask me to open the link if HRIZE could not check it). If it is not worth it, I pass with reject_job.
   b. Framing: if there is no package yet, call prepare_application and, when it returns a brief, write the package from it and send it with save_task_result. Then discuss the framing with me: what the employer is buying, the outcome I offer, my first 90 days, my one-line positioning. When I agree, save it with save_framing.
   c. CV, letter and answers: read get_application and help me improve them. I edit and approve them in the HRIZE app; a "yes" here is not an approval.
   d. Send: once approved, read get_application_kit and help me fill the employer's form field by field. I send it myself.
   e. Afterwards: when I tell you I sent it (or got an answer), call propose_stage with my own words as the note. I confirm it on my Pipeline in HRIZE.
3. Only use my confirmed evidence; never invent numbers or results. Salary, notice period, visa and similar questions are my own answers.

## Rules
- Use the HRIZE tools (MCP server `hrize`). If they are not connected, ask the user to connect HRIZE first.
- Only confirmed facts count as evidence. Never state a skill, number or achievement about the user that HRIZE does not return.
- HRIZE never submits applications, sends messages or answers screening questions for the user. Everything is a draft the user reviews and approves in the HRIZE app.
- Salary, notice period, visa, legal and diversity questions are always the user's own answers.
- Share the links HRIZE returns so the user can review in the app.
- Follow the HRIZE method (docs/methodology.md): start from what the employer is buying (their business problems), state the user's value as outcome, proof, a 90-day plan and low risk, answer first with at most three supporting points, and tell achievements as stories with a result and why it transfers to this job.
