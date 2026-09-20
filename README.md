# AI Intelligence Hub

AI Intelligence Hub will help people understand important AI developments, how they are being used, and what is worth learning or trying. Its core editorial promise is:

> What happened + Why it matters + How people are using it + What can I learn or try from it.

The project is also an incremental learning environment for data engineering, cloud architecture, backend development, AI engineering, and system design. It is currently in the documentation-and-scaffolding phase; no application, ingestion pipeline, database, or cloud infrastructure has been implemented.

## MVP scope

The first product surface is a General AI feed, eventually organized into Important Today, People Are Building, How People Are Using AI, Interesting Repositories, Platform Updates, Tools Worth Trying, Research That Matters, and Worth Learning Today.

The first ingestion phase will use roughly 8–12 high-quality sources. Ingestion itself is not part of the current phase.

## Repository map

- `docs/` — product, architecture, roadmap, decision, and source-registry documentation.
- `backend/` — placeholder for the future API and application services.
- `frontend/` — placeholder for the future web application.
- `data/samples/` — placeholder for safe, non-sensitive sample fixtures used in development and learning.
- `infra/` — placeholder for future infrastructure-as-code and cloud configuration.
- `scripts/` — placeholder for future developer and operational utilities.

## Start here

1. Read [the product definition](docs/PRODUCT.md).
2. Review [the staged architecture](docs/ARCHITECTURE.md).
3. Follow [the incremental roadmap](docs/ROADMAP.md).
4. Consult [the source registry](docs/SOURCES.md) before adding a source.
5. Record consequential trade-offs in [the decision log](docs/DECISIONS.md).

## Security and cost guardrails

- Never commit secrets. Copy `.env.example` to `.env` only when configuration is introduced.
- Keep the initial production system below approximately ₹1,000 INR/month.
- Prefer consumption-based or free-tier services; avoid always-on compute.
- Validate, filter, and deduplicate content before any LLM processing.
- Do not add infrastructure or dependencies without a demonstrated need.

## Current status

Only the initial structure and documentation exist. The next implementation step is deliberately deferred until the product model and first-wave sources are agreed.
