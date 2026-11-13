# MCP servers and skills

**MCP servers** give Claude *access* (tools that act on Fabric). **Skills** give Claude a *playbook* (how to do a kind of work well). You want both, but not everything at once: every MCP server adds tool definitions to Claude's context, so enable only what the project needs.

## Included in this template

- `.mcp.json` registers the **Fabric Core MCP server** (`https://api.fabric.microsoft.com/v1/mcp/core`), hosted by Microsoft, using Microsoft Entra ID sign-in. Project-scoped servers need your approval the first time.
- `.claude/skills/` has three small skills for this project: `fabric-safe-changes`, `fabric-new-workspace`, `fabric-project-conventions`.

## Microsoft Skills for Fabric (recommended)

Microsoft publishes official skills for Fabric as a plugin marketplace (repo: microsoft/skills-for-fabric). In Claude Code:

```
/plugin marketplace add microsoft/skills-for-fabric
/plugin install fabric-skills@fabric-collection
/plugin install powerbi-authoring@fabric-collection
```

Then restart Claude Code and run `/skills` to check. Per Microsoft: `fabric-skills` is the full Fabric bundle and does not include the Power BI plug-in; `powerbi-authoring` is separate. Smaller bundles exist (`fabric-authoring`, `fabric-consumption`, `fabric-operations`), and you can filter by workload, for example `--filter "spark-*"`. Most Fabric operations need Azure CLI sign-in (`az login`). Always name the workspace in your prompt and ask Claude to confirm it before making changes. See Microsoft's "Skills for Fabric" install page for the current details.

## Optional MCP servers (add per project, not by default)

Add with `claude mcp add --scope project ...` (writes `.mcp.json`) or `--scope user` (all your projects).

| Server | Use it for | How |
|---|---|---|
| Power BI (remote, preview) | Query data and generate insights from existing semantic models | `claude mcp add --scope project --transport http powerbi https://api.fabric.microsoft.com/v1/mcp/powerbi` |
| Fabric MCP (local) | Fabric docs, item definitions, OneLake tools on your machine | `claude mcp add --scope project fabric-local -- npx -y @microsoft/fabric-mcp@latest server start --mode all` |
| Fabric RTI MCP (preview) | KQL queries and Eventstreams in Real-Time Intelligence | `claude mcp add --scope project fabric-rti -- uvx microsoft-fabric-rti-mcp` |
| Power BI modeling (local, preview) | Build and change semantic models | see the microsoft/powerbi-modeling-mcp repo |
| Fabric Data Agent MCP | Ask a published Fabric data agent questions | copy the URL from the agent's MCP settings tab |

Server details, flags and preview status change; check Microsoft's documentation before relying on them.

## Scopes at a glance

| What | Just you, every project | This project (shared in git) |
|---|---|---|
| MCP servers | `--scope user` | `.mcp.json` |
| Skills | `~/.claude/skills/` | `.claude/skills/` |
| Rules | `~/.claude/CLAUDE.md` | `CLAUDE.md` |

Put things you use in every project at user level; put things this project depends on in the repo so anyone who clones it gets the same setup.

## Habits that keep Claude sharp

- Keep `CLAUDE.md` short. Move procedures into skills and long explanations into `docs/`.
- Run `claude mcp list` and `/mcp` to see what is on. Remove servers you don't use.
- Ask for a plan first, then approve, then run (Plan mode helps).
- Specify the workspace in every prompt that touches Fabric.
