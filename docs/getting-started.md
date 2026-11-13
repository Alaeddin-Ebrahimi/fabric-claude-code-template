# Getting started

1. **Tools:** VS Code, Claude Code, Git, and Azure CLI (Microsoft lists it as needed for most Fabric operations).
2. **VS Code extensions:** Microsoft Fabric (workspaces and items), Python, Jupyter, and optionally MSSQL. Sign in to Fabric with F1, then `Fabric: Sign in`.
3. **Sign in to Azure CLI** with the account that has access to your Fabric workspace: `az login`. If the account has no Azure subscription, add `--allow-no-subscriptions`.
4. **Open this folder in VS Code and start Claude Code.** The project's `.mcp.json` adds the Fabric Core MCP server. Claude Code asks you to approve project servers the first time. Run `/mcp` to check it is connected and to sign in if asked.
5. **Optional:** install Microsoft's Skills for Fabric and extra MCP servers. See `mcp-and-skills.md`.
6. **Paste the setup prompt** from `first-prompt.md`. Claude asks you a few questions and creates your workspace folders.
7. **Test with a read-only prompt:** "Using the fabric MCP server, list my Fabric workspaces. Don't change anything."
