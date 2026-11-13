# First prompt

After you have the project folder (see `ways-to-use.md`), open it in VS Code, start Claude Code in that folder, run `/mcp` to check the `fabric` server is connected, then paste the prompt below.

It makes Claude read the template's rules, ask you a few questions, and set the project up. It does not change anything in Fabric.

## Paste this

```
Read CLAUDE.md, docs/getting-started.md and docs/ways-to-use.md in this project.

Then set this project up for me. Work in this order:

1. Check the fabric MCP server is connected. Using it, list the Fabric workspaces I can see. Read only: do not create, change or delete anything in Fabric.
2. Ask me these questions in one message, then wait for my answers:
   - Project name and what it is for
   - Which of those workspaces this project uses, and which are protected (never change them)
   - Whether my workspaces already use Fabric Git integration (and which repo and folder), or not at all
   - Whether this is a Fabric trial or an organisation tenant
3. After I answer, fill in the placeholders in the root CLAUDE.md (project name, protected workspaces, environment, current focus). Keep it short.
4. For each workspace I named, run the fabric-new-workspace skill to create its folder under workspaces/ and fill in its CLAUDE.md and README.md. If a workspace is already Git-connected, do not move its folder; just record where it is.
5. Update workspaces/README.md with the list.
6. Show me a short summary of what you changed in this folder. Do not commit anything.

Rules: Fabric items are not Azure resources, so do not search Azure or create Azure resources for them. Using az login to sign in for Fabric tools is fine. Always name the exact workspace before any change and ask me first.
```

## Then

- Review what Claude wrote. Edit anything that is wrong.
- Commit when you are happy (if you use Git).
- Next, ask for one small read-only job, for example: "List the items in workspace <Name> grouped by type."
