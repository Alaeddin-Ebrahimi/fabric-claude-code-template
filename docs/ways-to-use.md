# Ways to use this template

Pick the scenario that matches you. All of them end the same way: a project folder that VS Code and Claude Code can read.

## 1. New GitHub repo (most common)

Click **Use this template** on GitHub, name your repo, then clone it. You get clean history and no link back to this template.

## 2. Local only, no Git

Click **Code > Download ZIP** (or copy the folder), unzip it where you keep projects, and open it in VS Code. Everything works without Git. Claude Code uses `CLAUDE.md`, `.mcp.json` and `.claude/skills/` straight from the folder. You lose history and backup, so keep the folder somewhere that is backed up.

## 3. Add it to an existing repo (your org's repo)

Do not merge this template wholesale. Copy only what you need into a subfolder or the repo root:

- `CLAUDE.md` and `.mcp.json` (merge by hand if you already have them)
- `.claude/skills/` (optional)
- `workspaces/`, `shared/` and `docs/` if you want the layout

Remove the template's `LICENSE` and `README.md` so they don't replace your own.

## 4. Clone it and keep pulling updates

Clone it normally and keep the original as `upstream`. Merge updates when you want them. Expect to resolve conflicts in `CLAUDE.md`, because you will edit it.

## Fabric Git integration: how it fits

Fabric's own Git integration connects a workspace to one branch and **one folder** of a repo. It only reads and writes inside that folder.

- This template points each workspace at its own folder: `workspaces/<WorkspaceName>/items`. Everything else in the repo (docs, CLAUDE.md, shared scripts, notebooks you hand-write) sits outside it, so Fabric never touches it.
- **Your org already has Git integration on?** Keep it as it is. Don't move or rename the folder a workspace is connected to. Use this template only around it: put `CLAUDE.md`, skills and docs next to or above the existing folder. Set a workspace's Git folder to `items/` only for new connections.
- **One workspace, one branch, one folder.** Don't connect two workspaces to the same folder.
- **No Git at all?** The template still works. Skip the `items/` folder, or use it only for notes. Claude reaches Fabric through the MCP server, not through Git.
- Fabric item folders are named `[Item Name].[Item Type]` and contain a `.platform` file. Let Fabric write them. Don't edit `.platform` or `logicalId` by hand.
- Git integration has limits: not every item type is supported, and some are preview. Check Microsoft Learn before relying on it for a given item.

## What Claude should never do in any scenario

Change or delete Fabric items without you naming the exact workspace and approving the change. The `fabric-safe-changes` skill and the rules in `CLAUDE.md` enforce this.
