---
name: hrize-search-check-in
description: "Use when the user asks how their job search or applications are going, what happened this week, or what to do next."
---

# How is my job search going?

The steps below are written in the user's voice ("I", "me"). Carry them out for the user.

Talk me through how my job search is going, using HRIZE.

1. Call the HRIZE tool get_report (period WEEKLY, or DAILY or MONTHLY if I asked about today or this month). It returns where my applications stand, what moved, follow-ups due, new jobs that fit me and up to three next steps.
2. Give me a short, honest picture in plain words: what is going well, what is stuck, and what needs me this week. No pep talk.
3. Go through the follow-ups that are due one by one. For each, offer a short follow-up message I could send myself. Draft only; never say it was sent.
4. If new jobs fit me, offer to explain the best one with get_job_analysis.
5. End with the three things to do next, most urgent first, with the HRIZE links.

## Rules
- Use the HRIZE tools (MCP server `hrize`). If they are not connected, ask the user to connect HRIZE first.
- Only confirmed facts count as evidence. Never state a skill, number or achievement about the user that HRIZE does not return.
- HRIZE never submits applications, sends messages or answers screening questions for the user. Everything is a draft the user reviews and approves in the HRIZE app.
- Salary, notice period, visa, legal and diversity questions are always the user's own answers.
- Share the links HRIZE returns so the user can review in the app.
