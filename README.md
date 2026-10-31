# HRIZE plugin

HRIZE, your evidence-backed career agent: find jobs that fit your proven experience, see why, draft applications with your own AI, practise interviews and your pitch, and track your search. You review and approve everything in HRIZE.

The plugin connects your AI assistant to your own HRIZE account (you sign in to HRIZE when the
assistant first uses it) and adds skills for the most useful tasks. The skills run on your own
assistant, so they use your subscription, not HRIZE credits.

## What is inside

| Skill | What it does |
|---|---|
| `hrize-career-agent` | HRIZE career agent. Use whenever the user talks about their career, job search, CV, a job posting, applications, interviews or HRIZE. Explains what HRIZE does, which tools to use and the rules for using the user's evidence. |
| `hrize-application-pipeline` | Work through my applications. Use when the user wants to work on their job applications, asks what to do next, which job to apply to, or wants help filling an employer's application form. |
| `hrize-import-background` | Import my background into HRIZE. Use when the user is new to HRIZE, has an empty profile, or wants to add their career history from what you already know about them. |
| `hrize-explain-match` | Explain my match for a job. Use when the user asks whether they fit a job in HRIZE, why a job matches, or what their gaps are. |
| `hrize-draft-application` | Draft my application with my own AI. Use when the user wants to apply for a job in HRIZE: a tailored CV, cover letter, outreach messages or screening answers. |
| `hrize-mock-interview` | Run a mock interview for a job. Use when the user wants to practise an interview for one of their HRIZE jobs. |
| `hrize-pitch-coach` | Coach my elevator pitch. Use when the user wants help with their elevator pitch or how to introduce themselves to an employer. |
| `hrize-search-check-in` | How is my job search going?. Use when the user asks how their job search or applications are going, what happened this week, or what to do next. |
| `hrize-craft-my-job` | Craft my job. Use when the user wants to grow, learn or get more from their current job without changing employer, or asks what to learn next. |

- **MCP server:** `https://staging.hrize.me/api/mcp` (Streamable HTTP, OAuth sign-in to your HRIZE account).
- **Formats:**
  - `plugin.json`, `mcp.json` and `skills/`: the open [Agent Plugins](https://agent-plugins.org) format.
  - `.claude-plugin/` and `.mcp.json`: Claude Code's plugin format.

## Install

- **Claude Code:**

  ```
  /plugin marketplace add delame/hrize-plugin
  /plugin install hrize@hrize
  ```

- **Codex, Cursor, VS Code and GitHub Copilot:** add this repository as an Agent Plugins source in the app's plugin settings.
- **ChatGPT:** download the .zip from the latest release, then in ChatGPT open Plugins, choose +, and upload it under New Plugin. Or add a custom MCP server with the URL `https://staging.hrize.me/api/mcp`.
- **Claude (web, desktop and mobile):** add a custom connector with the URL `https://staging.hrize.me/api/mcp`. For the skills, upload a skill folder from `skills/` under Settings, then Capabilities.

## Your data and approvals

- **Your account:** HRIZE uses only your own data. The assistant sees what you allow when you sign in, and you can disconnect it any time under Integrations in HRIZE.
- **Approvals:** HRIZE never submits applications, sends messages or answers screening questions for you. Everything is a draft you approve in the app.
- **Privacy policy:** https://staging.hrize.me/privacy
- **Learn more:** https://staging.hrize.me

## Licence

Free to install and use with your HRIZE account. The plugin is not open source: its skills,
prompts and method may not be copied, changed or redistributed. See LICENSE.

This repository is generated from the HRIZE app. Please report issues in HRIZE (More, then Report a bug).
