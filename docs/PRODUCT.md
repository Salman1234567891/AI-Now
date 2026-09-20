# Product

## Purpose

AI Intelligence Hub helps users understand important AI developments, what people are building, how AI is used in practice, and which ideas are worth learning or trying. It is not intended to be a high-volume news aggregator.

Its differentiator is: **What happened + Why it matters + How people are using it + What can I learn or try from it.**

The project also provides a practical setting for learning data engineering, cloud architecture, backend development, AI engineering, and system design, with decisions documented well enough to explain in interviews.

## MVP experience

The initial product surface is a General AI feed for developers, data professionals, technical leaders, product practitioners, and serious AI learners. Its intended sections are:

- Important Today
- People Are Building
- How People Are Using AI
- Interesting Repositories
- Platform Updates
- Tools Worth Trying
- Research That Matters
- Worth Learning Today

Every published story should earn its place through importance, credibility, practical value, or learning value. Research is included selectively when it has reasonable practical significance.

## Content model

Each item has one primary content type: `NEWS`, `PRODUCT_RELEASE`, `MODEL_RELEASE`, `REPOSITORY`, `PRACTICE`, `TUTORIAL`, `CASE_STUDY`, `RESEARCH`, `TOOL`, `BENCHMARK`, or `OPINION`.

An item can relate to multiple extensible platforms and topics. Initial topics include agents, coding agents, LLMs, reasoning, multimodal AI, RAG, embeddings, fine-tuning, prompting, context engineering, AI/data/software engineering, cloud AI, infrastructure, open-source and local AI, enterprise AI, developer tools, automation, research, safety, evaluation, serving, vector databases, databases, and data platforms.

## Source strategy

Sources are grouped by their role:

- **Official Sources** — platform announcements, documentation, research labs, and official repositories; preferred for factual confirmation.
- **Developer / Open Source Sources** — repositories, engineering communities, demos, and technical projects; especially useful for practical evidence.
- **AI Newsletters / Publications** — trusted secondary discovery and context.
- **Research Sources** — selected papers and research-lab publications with practical significance.
- **Community / Discovery Sources** — trend and discussion signals that require verification before factual publication.

Credibility levels are A (primary/official), B (trusted secondary), C (technical/community evidence), and D (community discovery). Community interest is a discovery signal, not proof. See the complete [source registry](SOURCES.md).

## Future capabilities

Later versions may add platform and role-specific feeds, personalization, learning features, semantic search or Ask, saved stories, subscriptions, email briefings, and premium features. Future role relevance may score stories for data, software, AI, ML, analytics, DevOps/platform, and cloud engineers; data scientists; product managers; technical leaders; and general AI learners. Role scoring is outside the initial MVP.

## Constraints

- Initial production spend must remain below approximately ₹1,000 INR/month.
- LLM calls must be consolidated, filtered, and deduplicated.
- The design should allow later local-model or hybrid enrichment, but this is not implemented now.
- Databricks learning environments may reuse raw data for education but must not become a production dependency where licensing or production restrictions apply.
- Secrets must remain in environment variables and never in source control.

Early success means a small feed in which each story is credible, non-duplicative, clearly explained, and actionable. Volume and personalization come later.
