---
name: hrize-import-background
description: "Use when the user is new to HRIZE, has an empty profile, or wants to add their career history from what you already know about them."
---

# Import my background into HRIZE

The steps below are written in the user's voice ("I", "me"). Carry them out for the user.

I am building my professional evidence base in a career tool called HRIZE. Using everything you
know about me from our previous conversations and any memory you hold, produce a **truthful,
evidence-only** export of my professional background.

Rules:
1. Include only what I actually told you or what is clearly supported by what I told you. Never invent employers, titles, dates, numbers, technologies, certifications or achievements.
2. For every item mark `"how_known": "user said"` if I stated it, or `"how_known": "inferred"` if you are concluding it from context. If unsure, use "inferred" and add the doubt to `open_questions`.
3. Keep my own wording where you can. Do not embellish or upgrade titles.
4. Exclude health, family, religious, political, union, sexual orientation, financial-hardship and legal-dispute information entirely.
5. Build one JSON object in the schema below. Show me a short summary of what you will send (employers, number of projects and achievements, anything you marked as inferred), and when I agree, call the HRIZE tool `import_background` with it. Then tell me what HRIZE reports and offer to go through the open questions.

Schema:

```json
{
  "hrize_export_version": "1.0",
  "generated_by": "<your product name>",
  "generated_at": "<YYYY-MM-DD>",
  "summary": "<2-4 sentences on my professional identity as you understand it>",
  "employment": [
    {
      "employer": "", "title": "", "start": "YYYY-MM", "end": "YYYY-MM or null", "location": "",
      "responsibilities": [""],
      "projects": [
        { "name": "", "description": "", "role": "", "outcome": "", "technologies": [""],
          "team_size": null, "budget": null, "revenue_impact": null,
          "clients_or_industries": [""], "period": "", "how_known": "user said | inferred" }
      ],
      "achievements": [ { "statement": "", "metric": "", "how_known": "user said | inferred" } ],
      "how_known": "user said | inferred"
    }
  ],
  "skills": [ { "name": "", "level": "basic | working | strong | expert", "evidence": "", "how_known": "" } ],
  "technologies": [""],
  "methodologies": [""],
  "industries": [""],
  "certifications": [ { "name": "", "issuer": "", "year": null, "how_known": "" } ],
  "education": [ { "institution": "", "degree": "", "field": "", "year": null, "how_known": "" } ],
  "languages": [ { "language": "", "level": "", "how_known": "" } ],
  "career_preferences": {
    "desired_direction": "", "roles_to_prioritize": [""], "roles_to_avoid": [""],
    "industries": [""], "company_sizes": [""], "work_model": "", "locations": [""],
    "commercial_vs_technical": "commercial | balanced | technical", "notes": ""
  },
  "open_questions": [""]
}
```

If you hold no information about me, return the JSON with empty lists and say so in `summary`.


## Rules
- Use the HRIZE tools (MCP server `hrize`). If they are not connected, ask the user to connect HRIZE first.
- Only confirmed facts count as evidence. Never state a skill, number or achievement about the user that HRIZE does not return.
- HRIZE never submits applications, sends messages or answers screening questions for the user. Everything is a draft the user reviews and approves in the HRIZE app.
- Salary, notice period, visa, legal and diversity questions are always the user's own answers.
- Share the links HRIZE returns so the user can review in the app.
