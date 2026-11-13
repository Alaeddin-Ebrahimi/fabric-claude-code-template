# Runbook

What to do when something goes wrong. Fill in as you learn.

## Quick checks
- Is the capacity running, and is it throttled?
- Did the last pipeline or notebook run fail? Where are its logs?
- Is the workspace in sync with Git (Git status column)?
- Did a source system or credential change?
- Is the MCP server connected (`/mcp`) and is `az login` still valid?

## Common problems
| Symptom | Likely cause | Fix |
|---|---|---|
| Claude says it needs authentication | Sign-in expired | Run `/mcp` and sign in again; `az login` if skills need it |
| Actions land in the wrong workspace | Workspace not named in the prompt | Name the workspace in every prompt; use fabric-safe-changes |
| <symptom> | <cause> | <fix> |

## Contacts
- Workspace admins: <names>
- Capacity admins: <names>
