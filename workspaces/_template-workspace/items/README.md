# items

The **Git folder** for this workspace. In the workspace's Git settings, set the Git folder to `workspaces/<WorkspaceName>/items`. Fabric then writes one folder per item here, named `[Item Name].[Item Type]` (for example `sales.Lakehouse`), each with a `.platform` file and the files that item type needs.

- Let Fabric create and update this folder (Commit to Git / Update from Git).
- Don't hand-edit `.platform` files or `logicalId` values.
- If you rename an item folder by hand, update dependency paths (for example a report pointing at its semantic model).
