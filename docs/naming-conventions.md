# Naming conventions (suggested)

Pick a convention early and write it down. These are suggestions, not Fabric rules. Because item folders in Git are named `[Item Name].[Item Type]`, short consistent names keep paths readable.

## Workspaces
`<Domain>_<Layer or Purpose>_<Env>`, for example `Sales_Gold_Prod`. Avoid spaces if you script against names. The folder in `workspaces/` uses the exact workspace name.

## Items
Short type prefix, lowercase words with underscores:

| Item | Prefix | Example |
|---|---|---|
| Lakehouse | lh_ | lh_sales |
| Warehouse | wh_ | wh_finance |
| Notebook | nb_ | nb_load_orders |
| Pipeline | pl_ | pl_daily_refresh |
| Dataflow Gen2 | df_ | df_clean_customers |
| Semantic model | sm_ | sm_sales |
| Report | rpt_ | rpt_sales_overview |
| Eventstream | es_ | es_clickstream |
| Eventhouse / KQL database | eh_ / kqldb_ | eh_telemetry |
| Environment | env_ | env_spark_default |

## Tables and columns
Be consistent: for example `snake_case`, singular or plural (pick one), and a clear prefix or schema per layer.

## Branches
`feature/<short-description>`, `fix/<short-description>`.
