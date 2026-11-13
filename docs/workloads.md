# Workload checklists

Short prompts for what to write down per workload. Put the answers in the workspace README or `shared/`.

- **Data Engineering:** for each lakehouse: purpose, layers or schemas, shortcuts, load pattern, owners. Notebooks: inputs, outputs, schedule. Environments: key libraries.
- **Data Factory:** for each pipeline or dataflow: purpose, trigger or schedule, sources and destinations, parameters, failure handling, who is alerted. Keep connection names here, never secrets.
- **Data Warehouse:** schemas, key tables, load order, views for consumers, permissions model.
- **Real-Time Intelligence:** event sources, schemas, retention and caching, Eventhouse and database layout, alert rules (Activator), dashboards. Typical flow: source, Eventstream, Eventhouse, queryset or dashboard, Activator.
- **Power BI:** semantic model grain, relationships, measures list, storage mode (Import, DirectQuery or Direct Lake), refresh, report audiences.
- **Data Science:** per experiment: question, data, features, metrics, result, next idea. Don't commit datasets or model files.
- **Databases and mirroring:** source system, what is mirrored, latency expectations, owners and permissions.
- **OneLake and governance:** shortcuts and owners, workspace roles, domains, sensitivity labels, network settings.
