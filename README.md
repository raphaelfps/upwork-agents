# upwork-agents

Claude-powered agents for generating Upwork proposals — reads a job posting, picks the right template, fills in the specifics, and outputs a ready-to-send proposal.

Built for a Python developer focused on automation, web scraping, and document generation.

---

## How it works

1. Paste a job posting into the Claude Code chat
2. Say: `gera proposta`
3. Get a finished proposal, ready to copy and paste

The agent reads your freelancer profile, identifies the job category, selects the matching template, and fills in job-specific details automatically.

---

## Project structure

```
upwork-agents/
├── CLAUDE.md                          # Instructions for Claude Code
├── context/
│   └── profile.md                     # Freelancer profile (rate, stack, projects, style)
└── agents/
    └── proposal-generator/
        ├── agent.md                   # Agent prompt (Claude's instructions)
        └── templates/
            ├── scraping.md            # Web scraping jobs
            ├── pdf-automation.md      # PDF generation jobs
            └── email-automation.md    # Email automation jobs
```

---

## Usage

**Prerequisites:** [Claude Code](https://claude.ai/code) installed and configured.

```bash
cd upwork-agents
# Open Claude Code, paste a job posting, and type: gera proposta
```

---

## Adding new templates

1. Create a new `.md` file in `agents/proposal-generator/templates/`
2. Write the template using `[UPPERCASE PLACEHOLDERS]` for job-specific fields
3. Open `agents/proposal-generator/agent.md` and add the new template to the selection table in Step 2

---

## Customizing

- **Change your profile:** edit `context/profile.md`
- **Change tone or rules:** edit `agents/proposal-generator/agent.md`
- **Change a template:** edit the relevant file in `templates/`

---

## Author

[Raphael](https://github.com/raphaelfps) — Python developer, automation & web scraping
