---
name: fabric-new-workspace
description: Use when adding a new Fabric workspace to this project. Creates its folder from the template, fills in its plan and rules, and updates the workspace index.
---

# Add a new workspace to the project

1. Ask for: workspace name (exact, as in Fabric), purpose, layer or environment (for example Bronze, Silver, Gold, Dev, Test, Prod), capacity, and whether it is protected.
2. Copy `workspaces/_template-workspace/` to `workspaces/<WorkspaceName>/`. Use the exact Fabric workspace name, avoiding characters that are invalid in folder names.
3. Fill in `workspaces/<WorkspaceName>/CLAUDE.md` and `README.md` from the answers. Keep CLAUDE.md short.
4. Add a row to the table in `workspaces/README.md`.
5. If the workspace is protected, add it to "Protected workspaces" in the root CLAUDE.md.
6. Remind the user to connect the workspace to Git with the Git folder set to `workspaces/<WorkspaceName>/items`, and to do that in the Fabric settings themselves.
7. Do not create or change anything in Fabric itself unless asked; follow the fabric-safe-changes skill if so.
