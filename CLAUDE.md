# upwork-agents

This repository contains Claude-powered agents that help generate Upwork proposals for Raphael, a Python developer focused on automation and web scraping.

## What this repo does

Each agent reads a freelancer profile and a job posting, selects the right proposal template, fills in the specifics, and outputs a ready-to-send proposal.

## How to generate a proposal

1. Open a Claude Code session in this directory
2. Paste the full text of the Upwork job posting into the chat
3. Say: **"gera proposta"**

Claude will:
- Read `context/profile.md` for Raphael's background and style
- Pick the right template from `agents/proposal-generator/templates/`
- Fill in job-specific details
- Output the finished proposal, ready to copy and paste

## Key files

| File | Purpose |
|---|---|
| `context/profile.md` | Freelancer profile: rate, stack, projects, proposal style |
| `agents/proposal-generator/agent.md` | The agent prompt — instructions for Claude |
| `agents/proposal-generator/templates/scraping.md` | Template for web scraping jobs |
| `agents/proposal-generator/templates/pdf-automation.md` | Template for PDF generation jobs |
| `agents/proposal-generator/templates/email-automation.md` | Template for email automation jobs |

## Notes

- The agent prompt lives in `agent.md` — edit it if you want to change tone, structure, or rules
- Templates use `[UPPERCASE PLACEHOLDERS]` — Claude fills these in from the job posting
- Update `context/profile.md` whenever you add a new GitHub project or change your rate
