# Skills

Agent skills for software engineering workflows.

Each skill is small and does one job. They work with Claude Code, Codex, Cursor, and any other agent that supports [Agent Skills](https://agentskills.io). Change them to fit how you work.

## Installation

Install all skills:

```bash
npx skills@latest add johnnyfekete/skills
```

Install one skill:

```bash
npx skills@latest add johnnyfekete/skills --skill handoff
```

The installer copies the skill files into your project. You can edit them there. To get new versions, run `npx skills@latest update`.

## Skills

### [handoff](./skills/handoff/SKILL.md)

When the agent finishes a task, it ends its last message with a short review block: the dev server link, the worktree path, the ticket link, the PR link, and 2–3 steps to test the change.

```
✅ Ready for review

- 🌐 Dev server: http://localhost:5174/settings
- 📁 Worktree: /Users/you/code/app-feature-x
- 🎫 Ticket: ENG-123
- 🔀 PR: https://github.com/you/app/pull/42

Test it:
1. Open the settings page.
2. Change your display name and click Save.
```

**Setup (optional):** To get a clickable ticket link, add your ticket link format to your project's `CLAUDE.md` or `AGENTS.md`. For example:

```
Tickets: Linear. Link format: https://linear.app/<team>/issue/<ID>
```

```
Tickets: Jira. Link format: https://<company>.atlassian.net/browse/<ID>
```

Without this line, the block shows only the ticket ID.

## License

[MIT](./LICENSE)
