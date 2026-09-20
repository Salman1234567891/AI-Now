# Source Registry

This is a planning registry; it does not enable ingestion. `MVP` means a first-wave candidate, not that a connector exists. Exact URLs, permissions, and ingestion methods must be verified during implementation.

Credibility: `A` primary/official, `B` trusted secondary, `C` technical/community evidence, `D` community discovery.

## Official sources

| SourceName | Platform | Level | IntendedContentTypes | ExpectedIngestionMethod | MVP | Notes |
|---|---|---:|---|---|:---:|---|
| OpenAI News, Research, product and developer updates | OpenAI | A | NEWS, PRODUCT_RELEASE, MODEL_RELEASE, RESEARCH | RSS/API/HTML or changelog | Yes | ChatGPT, Codex, Agents, APIs, multimodal and enterprise updates |
| Anthropic News, research, Claude and developer updates | Anthropic | A | NEWS, PRODUCT_RELEASE, MODEL_RELEASE, RESEARCH | RSS/HTML or changelog | Yes | Claude Code, MCP, APIs, agents and safety research |
| Microsoft AI, Copilot, Azure AI and developer updates | Microsoft | A | NEWS, PRODUCT_RELEASE, TOOL, PRACTICE | RSS/API/HTML | Yes | M365, Azure AI Foundry, VS/VS Code when materially AI-related |
| GitHub Blog, Copilot and developer platform updates | GitHub | A | NEWS, PRODUCT_RELEASE, PRACTICE | RSS/API/HTML | Yes | Includes coding-agent and AI/ML articles |
| Google AI, Gemini, DeepMind and Cloud AI updates | Google | A | NEWS, PRODUCT_RELEASE, MODEL_RELEASE, RESEARCH | RSS/HTML or changelog | Yes | Gemini API, agents, multimodal and developer announcements |
| xAI announcements and Grok updates | xAI | A | NEWS, PRODUCT_RELEASE, MODEL_RELEASE, RESEARCH | HTML/API or changelog | Later | Official model, API and research announcements |
| Meta AI and Llama announcements/research | Meta | A | NEWS, MODEL_RELEASE, RESEARCH | RSS/HTML/repository metadata | Later | Open models, inference, research and multimodal work |
| DeepSeek official announcements and releases | DeepSeek | A | NEWS, MODEL_RELEASE, RESEARCH | HTML/API/repository metadata | Later | Model, API and research releases |
| Alibaba/Qwen announcements and releases | Qwen | A | NEWS, MODEL_RELEASE, REPOSITORY, RESEARCH | HTML/API/repository metadata | Later | Developer and open-source developments |
| Moonshot AI/Kimi announcements | Kimi | A | NEWS, PRODUCT_RELEASE, MODEL_RELEASE | HTML/API or changelog | Later | Reasoning, agents and long-context developments |
| MiniMax announcements | MiniMax | A | NEWS, PRODUCT_RELEASE, MODEL_RELEASE | HTML/API or changelog | Later | Major model, multimodal and API releases |
| Mistral AI announcements | Mistral | A | NEWS, MODEL_RELEASE, PRODUCT_RELEASE | RSS/HTML or changelog | Later | Open and enterprise models, APIs, European ecosystem |
| Cohere announcements | Cohere | A | NEWS, MODEL_RELEASE, PRODUCT_RELEASE, PRACTICE | RSS/HTML or changelog | Later | Enterprise LLMs, RAG and embeddings |
| Perplexity announcements | Perplexity | A | NEWS, PRODUCT_RELEASE, TOOL | HTML or changelog | Later | Major search, agent, research and productivity updates only |
| Databricks blog and product announcements | Databricks | A | NEWS, PRODUCT_RELEASE, PRACTICE | RSS/HTML or changelog | Yes | Mosaic AI, Spark, Delta, lakehouse, agents and major DE changes |
| Snowflake AI and data-platform announcements | Snowflake | A | NEWS, PRODUCT_RELEASE, PRACTICE | RSS/HTML or changelog | Later | Cortex, AI and relevant data-engineering developments |
| NVIDIA AI and research announcements | NVIDIA | A | NEWS, PRODUCT_RELEASE, MODEL_RELEASE, RESEARCH | RSS/HTML | Later | Only AI building/deployment impact; exclude general hardware news |
| Major lab research publications | Multiple | A | RESEARCH | RSS/API/HTML | Later | OpenAI, Anthropic, DeepMind, Meta, Microsoft and NVIDIA; practical significance required |

## Developer / open-source sources

| SourceName | Platform | Level | IntendedContentTypes | ExpectedIngestionMethod | MVP | Notes |
|---|---|---:|---|---|:---:|---|
| GitHub Trending | GitHub / Open Source | C | REPOSITORY, TOOL, PRACTICE | HTML or permitted API-derived metadata | Yes | Explain purpose, significance, technique, audience and learning value; do not mirror rankings |
| Official GitHub repositories | Multiple | A | REPOSITORY, MODEL_RELEASE, TOOL | GitHub API/repository metadata | Later | Verify official ownership |
| Hugging Face blog | Hugging Face | A | NEWS, MODEL_RELEASE, PRACTICE, RESEARCH | RSS/HTML | Yes | Open-source ecosystem and major releases |
| Hugging Face models, Spaces and datasets | Hugging Face / Open Source | C | MODEL_RELEASE, TOOL, REPOSITORY | API/platform metadata | Yes | Curate notable models, demos, experiments and datasets |
| Independent engineering blogs and tutorials | Open Source / General | C | PRACTICE, TUTORIAL, CASE_STUDY, OPINION | RSS/HTML | Later | Evaluate evidence and reproducibility per source |

## AI newsletters / publications

| SourceName | Platform | Level | IntendedContentTypes | ExpectedIngestionMethod | MVP | Notes |
|---|---|---:|---|---|:---:|---|
| TLDR AI | Open Source / General | B | NEWS, MODEL_RELEASE, TOOL, RESEARCH | RSS/email/HTML, subject to terms | Yes | Technical developments and research discovery |
| The Rundown AI | Open Source / General | B | NEWS, TOOL, TUTORIAL, CASE_STUDY | RSS/email/HTML, subject to terms | Yes | General developments, practical use cases and workflows |
| The Batch — DeepLearning.AI | Open Source / General | B | NEWS, RESEARCH, TUTORIAL | RSS/email/HTML, subject to terms | Yes | Research explanations and educational context |
| Latent Space | Open Source / General | B | PRACTICE, OPINION, TUTORIAL | RSS/email/podcast metadata/HTML | Yes | AI engineering, agents, infrastructure and developer practice |

## Research sources

| SourceName | Platform | Level | IntendedContentTypes | ExpectedIngestionMethod | MVP | Notes |
|---|---|---:|---|---|:---:|---|
| arXiv | Open Source / General | C | RESEARCH, BENCHMARK | API/RSS | Later | Select practical LLM, agent, RAG, multimodal, reasoning, infrastructure, inference or architecture work; preprints are not peer-review proof |
| Official research labs | Multiple | A | RESEARCH, BENCHMARK | RSS/HTML/API | Later | Prefer primary papers and artifacts; overlaps official entries above |

## Community / discovery sources

| SourceName | Platform | Level | IntendedContentTypes | ExpectedIngestionMethod | MVP | Notes |
|---|---|---:|---|---|:---:|---|
| Hacker News submissions | Open Source / General | D | NEWS, REPOSITORY, PRACTICE, OPINION | Official API/RSS | Later | Discovery and debate; verify factual claims independently |
| Hacker News comments | Open Source / General | D | OPINION, PRACTICE | Official API | Later | Community opinion, never automatic factual evidence |
| Reddit communities | Open Source / General | D | PRACTICE, TOOL, OPINION | Official API, subject to terms | Later | Discovery-only for local LLM, ML, DE, programming, platform and agent discussions |
| Social media posts | Multiple | D | NEWS, OPINION, PRACTICE | Platform API/manual review, subject to terms | Later | Discovery-only unless authenticated as primary and corroborated |

## V1 versus later

The recommended first wave is OpenAI, Anthropic, Microsoft, GitHub Blog, Google/DeepMind, Hugging Face, Databricks, TLDR AI, The Rundown AI, The Batch, Latent Space, and GitHub Trending.

The next platform layer includes DeepSeek, Qwen, Meta, xAI, Kimi, MiniMax, Mistral, Cohere, Perplexity, Snowflake, and NVIDIA. arXiv, broader repositories/blogs, Hacker News, Reddit, and social sources follow when verification and editorial workflows are ready.
