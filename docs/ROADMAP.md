# Roadmap

The roadmap is deliberately incremental. A phase begins only after the previous phase has produced something understandable and testable.

## Phase 0 — Foundation (current)

- Define the product promise, scope, source taxonomy, credibility model, and target architecture.
- Create the repository structure and security defaults.
- Record important decisions and constraints.

**Exit:** documentation can guide the first implementation slice.

## Phase 1 — Small local ingestion slice

- Choose approximately 8–12 first-wave sources from [SOURCES.md](SOURCES.md).
- Implement one or two adapters first, with local fixtures and explicit schemas.
- Preserve raw documents and metadata; add validation, idempotency, and basic observability.
- Expand only after the common ingestion contract is stable.

**Not yet:** broad source coverage or Azure deployment.

## Phase 2 — Cleaning and canonical stories

- Normalize content and dates.
- Add deterministic duplicate detection before semantic techniques.
- Cluster source documents into canonical stories while retaining provenance.
- Establish editorial review and data-quality checks.

## Phase 3 — Structured enrichment

- Add a versioned structured-output schema.
- Enrich only useful unique items, requesting required fields in one call.
- Add caching, budgets, retry limits, evaluation samples, and human review.
- Measure value and cost before scaling.

## Phase 4 — Minimal product

- Select a low-cost store and frameworks from demonstrated requirements.
- Expose a small read API and build the General AI feed.
- Add appropriate production logging, monitoring, secrets management, and CI/CD.

## Phase 5 — Cloud and data-engineering learning

- Introduce Azure services one at a time where they solve a measured need.
- Land reusable raw data in ADLS and build separate Bronze, Silver, and Gold exercises.
- Practice incremental processing, schema evolution, quality, and optimization without making a restricted learning environment a production dependency.

## Phase 6 — Product expansion

- Add second-wave platforms and discovery sources.
- Evaluate platform pages, role relevance, personalization, saved stories, subscriptions, briefings, learning features, and semantic search/Ask.
- Explore local or hybrid enrichment when quality and operating data justify it.

Every phase must protect credibility, provenance, user value, security, and the approximate ₹1,000/month initial production budget.
