# Project: <name> (Microsoft Fabric)

## Purpose
<What this project delivers and what "done" looks like.>

## How this repo works
- One folder per Fabric workspace in workspaces/. Each has its own CLAUDE.md; read it before working there.
- Index of workspaces: workspaces/README.md
- Cross-workspace topics: shared/. Guides: docs/ (start with docs/mcp-and-skills.md).
- Fabric tools: the "fabric" MCP server (see .mcp.json). Procedures live in .claude/skills/.

## Rules
- Always name the exact target workspace before any Fabric action. Never assume one.
- Read-only first. Ask before creating, changing or deleting anything in Fabric. Use the fabric-safe-changes skill.
- Protected workspaces (do not change unless I say so): <list>
- Work one small step at a time and explain what each step does.
- Fabric items are not Azure resources: do not look for them in Azure or create Azure resources for them. Using `az login` to sign in for Fabric tools is fine.
- Never hand-edit `.platform` files or `logicalId` values in items/.
- Never commit secrets, keys, connection strings or customer data.
- <Add project-specific rules here.>

## Environment
- Account to sign in with: <account>
- Capacity / trial end date (if a trial): <date>

## Current focus
<What we are working on right now.>
