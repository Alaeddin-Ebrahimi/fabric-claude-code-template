---
name: fabric-safe-changes
description: Use before creating, changing, deleting, deploying or re-permissioning anything in Microsoft Fabric (workspaces, items, schedules, shortcuts, roles, capacity). Enforces explicit target, plan first, small steps and verification.
---

# Safe changes in Fabric

1. **Name the target.** State the exact workspace (and item) you will touch. If it is not clear, ask. Never assume the current or last-used workspace.
2. **Read first.** Inspect the current state with read-only calls before proposing anything.
3. **Plan.** Write a short plan: what changes, in which workspace, what could break, how to undo it. Wait for approval.
4. **Prefer lower environments.** Change Dev or Test before Prod. Never change a workspace listed as protected in CLAUDE.md.
5. **One thing at a time.** Make one change, check it, then continue.
6. **Verify.** Re-read the state after the change and report what actually changed.
7. **Record.** Update the workspace README (items table, notes). For a notable choice, add a short file in docs/decisions/.

Never delete items or workspaces, remove permissions, or pause capacity unless the user confirmed that exact action. Never write secrets into files.
