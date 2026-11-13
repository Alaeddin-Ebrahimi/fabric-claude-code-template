# Item catalog

Fabric groups items into workloads: Data Engineering, Data Factory, Data Science, Data Warehouse, Databases, Industry Solutions, Real-Time Intelligence, Fabric IQ and Power BI. All store data in OneLake.

The "Git type" column is the suffix Fabric uses in item folder names (`[Item Name].[Item Type]`). It is a guide: item types, preview status and Git support change, so check Microsoft's supported-items list before relying on it.

| Workload | Item | Git type (suffix) | Notes |
|---|---|---|---|
| Data Engineering | Lakehouse (with SQL analytics endpoint) | Lakehouse | Delta tables by default |
| Data Engineering | Notebook | Notebook | Python, Spark SQL, Scala, R |
| Data Engineering | Spark job definition | SparkJobDefinition | Scheduled batch Spark code |
| Data Engineering | Environment | Environment | Libraries and Spark settings |
| Data Engineering | User data functions | UserDataFunction | Python functions |
| Data Engineering | API for GraphQL | check docs | |
| Data Factory | Data pipeline | DataPipeline | Orchestration and copy |
| Data Factory | Dataflow Gen2 | check docs | Power Query based |
| Data Factory | Copy job | check docs | |
| Data Warehouse | Warehouse | Warehouse | T-SQL |
| Data Science | ML model, experiment | check docs | |
| Databases | SQL database in Fabric | check docs | Transactional |
| Mirroring | Mirrored database | check docs | Replicates external data into OneLake |
| Real-Time Intelligence | Eventstream | Eventstream | Ingest and route events |
| Real-Time Intelligence | Eventhouse | Eventhouse | |
| Real-Time Intelligence | KQL database | KQLDatabase | Includes a schema file |
| Real-Time Intelligence | KQL queryset | KQLQueryset | Saved KQL queries |
| Real-Time Intelligence | Real-Time dashboard | KQLDashboard | |
| Real-Time Intelligence | Activator | Reflex | Alerts and actions |
| Power BI | Semantic model | SemanticModel | Definition split into TMDL files |
| Power BI | Report | Report | |
| Power BI | Paginated report, dashboard, scorecard | check docs | |
| Developer experience | Variable library | VariableLibrary | Per-environment values |
| Developer experience | Deployment pipeline | n/a | Configured in the Fabric service |

Platform pieces that aren't items: OneLake (storage), shortcuts, domains, capacities, workspaces, Copilot, governance and the OneLake catalog.
