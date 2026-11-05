---
name: handoff
description: Use when you finish a task and hand the work back to me. Decide if a handoff block is useful, and add it to the end of your final message when it is.
---

# Handoff

When the task is done, end your final message with a handoff block. Include every line that applies. If a line applies but
you can't find the value, write "missing" and say why.

## When to use it

Use your judgment. Add the handoff block when I have something to
check, for example:
- you changed code that I can run or see in the browser
- you opened or updated a PR

Skip it when there is nothing to check, for example:
- you only answered a question or explained code
- you only changed docs or comments, and there is no PR

You can also show only some of the lines. For example, skip the
dev server line if the change has no UI (a backend script or a config file).

## Steps

1. **Dev server.** Start the dev server for this worktree if it isn't running.
   Other worktrees may already use the default port, so pick a free one.
   Use the URL that the dev server prints. Don't assume it's localhost.
   Open the URL once to make sure it loads.
2. **Worktree path.** Get the absolute path of this worktree.
3. **Ticket.** Find the ticket ID in the branch name, the commits, or the spec.
   Find the ticket tool's base URL in the project's CLAUDE.md or AGENTS.md.
   If you cannot find the base URL, show only the ID.
   Skip this line if there is no ticket.
4. **PR.** Get the link to the open PR.
5. **What to test.** Write 2–3 short steps I can click through
   to see the change working.

## Output format

---
✅ **Ready for review**

- 🌐 Dev server: <dev server URL>/<page-with-the-change>
- 📁 Worktree: <absolute path>
- 🎫 Ticket: [<TICKET-ID>](<link>)
- 🔀 PR: <link>

**Test it:**
1. ...
2. ...
---
