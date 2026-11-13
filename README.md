# fabric-claude-code-template

A project template for building on **Microsoft Fabric** with **Claude Code in VS Code**. It is designed for busy, multi-workspace work: every Fabric workspace gets its own folder with its own rules, so Claude loads only what it needs and you can find everything fast.

## What is in the box

| Piece | What it does |
|---|---|
| `CLAUDE.md` | Short rules Claude reads every session, and a map of the repo |
| `.mcp.json` | Connects the **Fabric Core MCP server** (hosted, nothing to install) |
| `.claude/skills/` | Three small project skills: safe changes, new workspace, conventions |
| `workspaces/` | One folder per Fabric workspace (copy `_template-workspace/`) |
| `shared/` | Things that span workspaces: governance, CI/CD, OneLake |
| `docs/` | Getting started, MCP and skills guide, architecture, item catalog, naming, runbook |
| `content/` | Optional notes and recordings if you teach or document your work |

Microsoft's official **Skills for Fabric** are not copied here; `docs/mcp-and-skills.md` shows how to install them so they stay up to date.

## Structure

```
fabric-claude-code-template/
  CLAUDE.md
  .mcp.json
  .claude/skills/
    fabric-safe-changes/SKILL.md
    fabric-new-workspace/SKILL.md
    fabric-project-conventions/SKILL.md
  workspaces/
    README.md                      Index of all workspaces
    _template-workspace/           Copy this for each workspace
      CLAUDE.md                    Rules for this workspace only
      README.md                    Plan and inventory
      items/                       Fabric Git folder (Name.ItemType)
      src/                         Hand-written code
        notebooks/  sql/  kql/  dax/
  shared/
    governance-and-security/
    cicd/ (parameters/, scripts/)
    onelake/
  docs/
  content/
```

## Quick start

1. Click **Use this template** (or copy the folder) and name your project.
2. Open the project folder in VS Code and read `docs/getting-started.md`.
3. Start Claude Code in the folder and approve the project MCP server when asked.
4. Copy `workspaces/_template-workspace/` to `workspaces/<YourWorkspace>/` and fill in its `CLAUDE.md` and `README.md` (or just ask Claude to run the `fabric-new-workspace` skill).
5. Connect that Fabric workspace to Git with the **Git folder** set to `workspaces/<YourWorkspace>/items`.

## Why one folder per workspace

Claude Code loads the root `CLAUDE.md` at the start and reads a `CLAUDE.md` in a subfolder when it works in that folder. With many workspaces, this keeps each session focused: the rules for Bronze don't crowd the context while you work on Gold.

## Good to know

- Fabric's Git sync writes item folders named `[Item Name].[Item Type]` into `items/`. Let Fabric manage them, and avoid hand-editing `.platform` files or `logicalId` values.
- Never commit secrets, connection strings or customer data.
- Fabric moves fast: item types, preview features and MCP servers change. Check Microsoft's documentation before relying on anything marked preview.
- Keep `CLAUDE.md` short. Put repeatable procedures in skills and long explanations in `docs/`.

## License

MIT. See [LICENSE](LICENSE).
