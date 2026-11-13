# Architecture

Describe the solution at a high level.

## Goal and users
<Who uses the result and what decisions it supports.>

## Layers
A common pattern is Bronze (raw), Silver (cleaned), Gold (modelled for use). Record your choice: which workspaces or lakehouses hold each layer, and what rules move data between them.

## Data flow
<Sources, ingestion, storage, transformation, serving, consumers. A simple diagram or list is enough.>

## Real-time path (if any)
<Event sources, Eventstream, Eventhouse, dashboards, Activator.>

## Serving
<Semantic models, reports, APIs, shortcuts to other teams.>

## Non-functional notes
Refresh and latency targets, capacity use, security model, cost limits, disaster recovery.
