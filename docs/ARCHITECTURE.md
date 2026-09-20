# Architecture

## Current state

The repository contains documentation and placeholders only. There are no frameworks, ingestion jobs, databases, cloud resources, or external API integrations.

## Target flow

```text
External sources
  -> Python ingestion
  -> raw cloud storage
  -> validation and cleaning
  -> deduplication / story clustering
  -> one structured LLM enrichment call per useful unique item
  -> structured database
  -> backend API
  -> web application
```

This is a direction, not a day-one deployment plan. Each component should be introduced only when the preceding stage creates a real need.

## Future source registry

The registry should be data-driven rather than encoded in UI conditionals.

| Field | Purpose |
|---|---|
| `source_id` | Stable machine identifier |
| `source_name` | Human-readable name |
| `source_category` | Official, developer/open source, publication, research, or community/discovery |
| `platform_ids` | References to zero or more extensible platform records |
| `credibility_level` | A, B, C, or D |
| `intended_content_types` | Content types commonly produced by the source |
| `expected_ingestion_method` | RSS, API, HTML, repository metadata, email/manual, or another adapter |
| `enabled_for_mvp` | Whether it belongs to the first ingestion wave |
| `discovery_only` | Prevents unverified community claims being treated as facts |
| `canonical_url` | Official location of the source |
| `active` | Operational enable/disable switch |
| `notes` | Scope, restrictions, and editorial guidance |

Platforms and topics should be separate records joined many-to-many to documents and stories. This permits additions without schema or UI rewrites.

## Source documents and canonical stories

Every fetched page, post, paper, or repository is a **Source Document**. Several documents can describe the same event. Deduplication and clustering should create one **Canonical Story**, retaining links to all evidence.

```text
Official announcement --\
Newsletter context -------> Canonical Story
Developer analysis -------/
Example repository -------/
```

A canonical story should eventually include title, summary, what changed, why it matters, practical uses, topics, platforms, source documents, primary source, importance score, practice value, repository links, and publication date. The primary source should normally be the strongest direct evidence.

## Classification, credibility, and enrichment

- A story has one primary content type but may have multiple platforms and topics.
- Source credibility belongs to evidence; it does not guarantee every claim is true.
- Level D material is discovery-only until corroborated.
- Official sources are preferred for facts; technical and secondary sources add context and examples.
- Research selection prioritizes practical significance rather than volume.

Enrichment occurs only after validation, cleaning, and deduplication. One versioned structured call should request all needed fields where practical. Store schema and model metadata. Control cost with early filtering, hashes, cached results, retry limits, and no repeated calls for unchanged items. A later hybrid design may use local models for simpler tasks.

## Learning and cloud direction

The same raw data may later feed a separate educational path:

```text
ADLS -> Databricks -> PySpark -> Bronze -> Silver -> Gold
```

This supports learning Spark DataFrames, Delta Lake, `MERGE`, joins, windows, partitioning, schema evolution, incremental processing, quality, and optimization. It remains logically separate from the lowest-cost production serving path.

Azure Functions, ADLS, Azure SQL, Azure Data Factory, Databricks, monitoring, secrets management, and CI/CD are candidates, not current dependencies. Prefer consumption-based compute and justify every addition against the approximate ₹1,000/month budget.

## Security baseline

- Configuration comes from environment variables.
- `.env` and generated data are ignored; `.env.example` contains names only.
- Secrets, tokens, passwords, and connection strings never enter code or samples.
- Future logs must avoid credentials, personal data, and sensitive payloads.
