---
name: fabric-project-conventions
description: Use when naming things or deciding where files go in this Fabric project (workspaces, items, SQL, KQL, DAX, notebooks, docs, decisions).
---

# Project conventions

Where things go:
- Synced Fabric items: `workspaces/<ws>/items/` (folders named `[Item Name].[Item Type]`). Let Fabric manage them; do not hand-edit `.platform` or `logicalId`.
- Hand-written code: `workspaces/<ws>/src/{notebooks,sql,kql,dax}/`.
- Workspace plan and inventory: `workspaces/<ws>/README.md`.
- Cross-workspace topics: `shared/`. Guides and decisions: `docs/`.

Naming: follow `docs/naming-conventions.md`. If the project has chosen different names, follow the project, not the suggestion.

Files: one purpose per file, a comment at the top saying what it does and what it changes. Number scripts when order matters (01_, 02_).

Never commit secrets, connection strings or customer data.
