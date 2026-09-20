# Decision Log

Add an entry when a decision changes architecture, cost, security, product behavior, or developer workflow.

## D-001 — Build incrementally

- **Status:** Accepted
- **Decision:** Begin with documentation and scaffolding; add no framework, ingestion, database, or cloud resource yet.
- **Reason:** Keeps learning visible and avoids premature commitments.

## D-002 — Editorial value over volume

- **Status:** Accepted
- **Decision:** Optimize for what happened, why it matters, how it is used, and what to learn or try.
- **Reason:** This is the product differentiation and inclusion test.

## D-003 — Preserve evidence and publish canonical stories

- **Status:** Accepted in principle; implementation deferred
- **Decision:** Store source documents independently and cluster them into one canonical story with provenance.
- **Reason:** Prevents duplicate stories while retaining primary evidence and secondary context.

## D-004 — Treat credibility explicitly

- **Status:** Accepted in principle; implementation deferred
- **Decision:** Use levels A–D and mark community sources discovery-only where appropriate.
- **Reason:** Popularity must not be mistaken for factual confirmation.

## D-005 — Use extensible platform and topic data

- **Status:** Accepted in principle; implementation deferred
- **Decision:** Use many-to-many records rather than hardcoded UI branches.
- **Reason:** The ecosystem changes and stories span platforms and topics.

## D-006 — Enrich after deduplication

- **Status:** Accepted in principle; implementation deferred
- **Decision:** Validate, clean, filter, and deduplicate before one consolidated structured LLM call per useful unique item.
- **Reason:** Controls cost and avoids inconsistent repeated analysis.

## D-007 — Separate learning and production concerns

- **Status:** Accepted in principle; implementation deferred
- **Decision:** Reuse raw data for an ADLS/Databricks learning path without making restricted learning services production dependencies.
- **Reason:** Preserves educational value without compromising licensing, reliability, or cost.

## D-008 — Low-cost, secret-free baseline

- **Status:** Accepted
- **Decision:** Target less than approximately ₹1,000 INR/month, prefer consumption pricing, and keep secrets in environment variables.
- **Reason:** Cost and security are design constraints, not cleanup tasks.

## Open decisions

- Exact first adapters and ingestion mechanisms
- Canonical schemas and identifiers
- Deduplication and clustering thresholds
- LLM provider/model and evaluation criteria
- Backend, database, frontend, and Azure service choices

These remain open until the relevant phase supplies enough evidence.
