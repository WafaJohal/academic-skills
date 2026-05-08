# Academic Skills for Claude

A growing collection of Claude skills for academic work — covering research ethics, grant writing, and paper writing. Built for everyday academic use: usable as-is or adaptable to your institution.

> **This is a personal/lab resource shared openly.** Skills are added as they are developed and tested. Contributions welcome.

---

## What is a Claude skill?

A **skill** is a plain-text instruction file (a `SKILL.md`) that you give Claude before starting a task. It tells Claude exactly how to approach a specific job — what questions to ask, what rules to apply, what the output should look like.

Think of it as a reusable prompt template, but richer: skills can include reference files, structured checklists, and domain-specific knowledge that Claude loads before helping you.

📖 [Learn more about Claude skills](https://www.anthropic.com/news/building-with-claude)

---

## How to use a skill

1. **Download** the `SKILL.md` file (and any `references/` folder alongside it) from this repo.
2. **Open Claude** at [claude.ai](https://claude.ai) (a Pro or Team account is recommended for longer tasks).
3. **Upload the skill file(s)** as attachments at the start of a new conversation.
4. **Start your task** — Claude will automatically follow the skill's structure.

For skills with a `references/` folder, upload all files in that folder alongside the `SKILL.md`. The skill instructions tell Claude to read them.

**Tip:** You can also paste the contents of `SKILL.md` directly into your message if you prefer not to upload files.

---

## Skills in this repo

### 🔬 Ethics Skills (`ethics-skills/`)

Three skills to support the full lifecycle of a human research ethics application, calibrated for Australian HREC processes and the Infonetica ERM submission system. Adaptable to other institutional contexts.

| Skill | What it does |
|-------|-------------|
| `ethics-writer` | Interviews you about your project across four phases and produces a complete draft: Infonetica application, Plain Language Statement, and Consent Form |
| `ethics-reviewer` | Reviews a draft application against National Statement requirements and common reviewer hotspots; rates issues by severity and gives a prioritised fix list |
| `ethics-response` | Drafts a point-by-point formal response to committee feedback, ready to upload to Infonetica as "Response to review documents" |

Each ethics skill includes a `references/` folder with supporting files (form structure, templates, writing patterns, common issues). Upload all of them together.

**Note on institutional adaptation:** The skills use `[Your Institution]` as a placeholder wherever institution-specific details are needed (complaint paragraph, approved storage systems, policy references). Search for `[Your Institution]` in the files and replace with your own details before use. The `references/institutional-rules.md` file is the main place to customise.

---

### 📄 Paper Writing Skills (`paper-writing-skills/`)

| Skill | What it does |
|-------|-------------|
| `paper-compliance-checker` | Audits a grant proposal or paper submission against a Call for Proposals (CfP) — checks word limits, formatting, mandatory sections, and required attachments. Outputs a compliance table with PASS/FAIL status and corrective actions |

---

## Adapting skills to your institution

Most skills work out of the box for any academic context. For the ethics skills specifically, you'll want to:

1. Replace `[Your Institution]` placeholders with your institution's name
2. Update `references/institutional-rules.md` with your institution's ethics policy name, approved data storage systems, and mandatory research integrity training
3. Replace the complaint paragraph placeholder in `references/templates.md` with your institution's exact approved wording
4. Check the data retention periods match your institution's Records & Disposal Authority

Everything else — the National Statement requirements, risk framing rules, consent logic, Infonetica form structure — applies broadly across Australian university HREC contexts.

---

## Contributing

Contributions are welcome — especially skills that fill gaps in the academic workflow.

**To contribute a skill:**

1. Fork this repo
2. Create a folder for your skill under the appropriate category (or propose a new category)
3. Include a `SKILL.md` and, if needed, a `references/` subfolder
4. Make sure the skill is anonymised — no institution-specific names, policy numbers, contact details, or personal information
5. Open a pull request with a short description of what the skill does and what triggered you to build it

**Skill ideas welcome too** — open an issue if there's a workflow you'd like to see covered.

---

## Repo structure

```
academic-skills/
├── ethics-skills/
│   ├── ethics-writer/
│   │   ├── SKILL.md
│   │   └── references/
│   ├── ethics-reviewer/
│   │   ├── SKILL.md
│   │   └── references/
│   └── ethics-response/
│       ├── SKILL.md
│       └── references/
│
└── paper-writing-skills/
    └── paper-compliance-checker/
        └── SKILL.md
```

---

## License

CC BY-NC-SA 4.0