# Awesome Agent Memory [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of memory systems, frameworks, benchmarks, and research for AI agents.

Agents forget between sessions and between tools. "Agent memory" is the growing category of systems that decide what to keep, connect related facts, and improve recall over time. This list tracks the tools and research in that space.

Contributions welcome. Please keep entries factual and free of marketing language. One tool per pull request, alphabetical within each section. See [Contributing](#contributing).

## Contents

- [Managed memory APIs and services](#managed-memory-apis-and-services)
- [Open-source frameworks and engines](#open-source-frameworks-and-engines)
- [MCP memory servers](#mcp-memory-servers)
- [Benchmarks and evaluation](#benchmarks-and-evaluation)
- [Papers](#papers)
- [Contributing](#contributing)

## Managed memory APIs and services

- [GoodMem](https://goodmem.ai) - Memory layer for agentic AI with owners, roles, scoped API keys and retrieval logging, multi-modal hybrid search with reranking, available as a managed cloud or self-hosted, with SDKs in Python, TypeScript, Java, .NET and Go.
- [Mem0](https://github.com/mem0ai/mem0) - Open-source (Apache-2.0) memory layer that extracts facts from conversations, plus a managed cloud, with many framework integrations.
- [Mnemoverse](https://mnemoverse.com) - Persistent memory API for AI agents over MCP. Scores importance on write, strengthens associations between concepts (Hebbian), and re-ranks recall from outcome feedback. MIT client, managed engine.
- [Supermemory](https://github.com/supermemoryai/supermemory) - Memory and context API for AI apps and agents, with fact extraction, user profiles, connectors, and hybrid vector-plus-keyword retrieval.
- [Zep](https://www.getzep.com/) - Managed memory service built on a temporal knowledge graph (open-source Graphiti engine), offered as cloud, BYOK, and self-hosted deployments.

## Open-source frameworks and engines

- [chamnan](https://github.com/ArcticFox2029/chamnan) - MIT repository-local memory for coding agents that stores an architecture index, an impact map, session records, and decisions as markdown committed beside the code, retrieved by keyword and injected at session start. Python standard library only, no network at runtime.
- [Cognee](https://github.com/topoteretes/cognee) - Apache-2.0 memory framework that builds a self-hosted knowledge graph via an extract-cognify-load pipeline combining vector and graph retrieval.
- [Graphiti](https://github.com/getzep/graphiti) - Apache-2.0 engine building real-time, bi-temporal knowledge graphs from conversational and structured data, with hybrid semantic, keyword, and graph retrieval (powers Zep).
- [Hindsight](https://github.com/vectorize-io/hindsight) - MIT agent-memory system running four parallel retrieval strategies per query: semantic search, BM25 keyword matching, graph traversal, and temporal reasoning.
- [LangMem](https://github.com/langchain-ai/langmem) - MIT SDK giving LangGraph agents long-term semantic, episodic, and procedural memory, plus a background memory manager.
- [Letta](https://github.com/letta-ai/letta-code) - Apache-2.0 stateful-agent harness with self-editing memory blocks, Git-backed context (MemFS), and conversation search; the current Letta implementation.
- [LWC](https://github.com/JanYork/llm-wiki-cli) - Apache-2.0 local-first CLI giving coding agents source-grounded project memory, plans, citations, and optional document and code graphs.
- [Memary](https://github.com/kingjulio8238/Memary) - Long-term memory framework for autonomous agents that builds a Neo4j/FalkorDB knowledge graph and tracks entities by breadth and recency.
- [MemEngine](https://github.com/nuster1128/MemEngine) - Library unifying many published LLM-agent memory models under a common, modular, pluggable interface (RUC and Huawei Noah's Ark).
- [Memobase](https://github.com/memodb-io/memobase) - User-profile-based long-term memory backend for LLM applications; maintains structured, evolving user profiles and event timelines across sessions.
- [Memori](https://github.com/MemoriLabs/Memori) - Apache-2.0 agent-memory engine that stores memory in standard SQL databases (SQLite, PostgreSQL, MySQL), with an optional managed cloud.
- [MemoryOS](https://github.com/BAI-LAB/MemoryOS) - OS-inspired hierarchical memory framework with short-, mid-, and long-term storage plus updating, retrieval, and generation modules.
- [MemOS](https://github.com/MemTensor/MemOS) - Memory operating system for LLMs; a unified API to add, retrieve, and manage graph-structured, multi-modal long-term memory.
- [memU](https://github.com/NevaMind-AI/memU) - Apache-2.0 agent-memory framework where agents store notes as organized Markdown files, recalled via embedding-based ranked retrieval.
- [MIRIX](https://github.com/Mirix-AI/MIRIX) - Apache-2.0 multi-agent memory system with six memory types (core, episodic, semantic, procedural, resource, knowledge vault); multimodal.
- [ReasonGraph](https://github.com/bgokden/reasongraph) - MIT graph-memory library that extracts entities and cause-effect relations with small fine-tuned models, answers why-questions by walking causal chains with citations, supports time-travel queries and contradiction handling, with a hosted service (ReasonGraph Cloud).

## MCP memory servers

Memory servers that connect to any Model Context Protocol client (Claude, Cursor, VS Code, ChatGPT, and others).

- [Basic Memory](https://github.com/basicmachines-co/basic-memory) - Local-first, AGPL-3.0 MCP server that stores agent memory as Obsidian-compatible Markdown files, building a knowledge graph agents can read and write.
- [Firekeep](https://github.com/kapella-hub/FirekeepHQ) - BUSL-1.1 self-hosted MCP operating layer that shares durable knowledge, working state, cooperative coordination leases, and replay evidence across Claude Code, Codex, Kiro, and OpenCode.
- [Hyperconsciousness](https://github.com/louis030195/hyperconsciousness) - MIT-licensed developer-alpha knowledge store with encrypted, append-only records and MCP retrieval through scoped, expiring grants.
- [Memento](https://mementoagi.com) - Hosted MCP memory for coding agents with editable Markdown records, team-shared context, and a web dashboard.
- [Mnemoverse](https://github.com/mnemoverse/mcp-memory-server) - Hosted persistent memory over MCP; one key or OAuth across MCP clients.
- [OpenMemory](https://github.com/mem0ai/mem0/tree/main/openmemory) - Local-first, private MCP memory server (part of the Mem0 project).
- [ReasonGraph Cloud](https://memory.primaxiom.ai) - Hosted graph memory over Streamable HTTP MCP with API-key auth; tools for remembering facts, discovering connections, tracing causes and effects and what-if queries.
- [Screenpipe](https://github.com/screenpipe/screenpipe) - MCP server for searching screen text and audio transcripts captured by a running Screenpipe instance, with source available under the Screenpipe Commercial License.
- [Vestige](https://github.com/samvallad33/vestige) - Local-first, AGPL-3.0 memory system for coding agents over MCP. Retroactive backfill ranks earlier records as candidate causes of a fresh failure, a composed graph records which memories were used together and surfaces never-tried combinations, retrieval decays on an FSRS-6 schedule, and receipts fail closed after compaction. Single Rust binary.

## Benchmarks and evaluation

Common suites used to evaluate agent memory.

- [agent-memory-bench](https://github.com/GiulioDER/agent-memory-bench) - Apache-2.0 execution-graded benchmark for coding-agent memory, with a retrieval-only official run and separate optional lifecycle probes.
- [BEAM](https://arxiv.org/abs/2510.27246) - Long-term memory benchmark: multi-turn conversations up to 10M tokens, 2,000 questions across ten memory abilities (ICLR 2026).
- [LoCoMo](https://snap-research.github.io/locomo/) - Very long-term multi-session dialogue benchmark (~300 turns, up to 35 sessions), evaluated via QA, event summarization, and multimodal dialogue generation (ACL 2024).
- [LongMemEval](https://xiaowu0162.github.io/long-mem-eval/) - 500-question benchmark testing five long-term memory abilities of chat assistants over scalable chat histories (ICLR 2025).
- [Open Agent Memory Benchmark](https://github.com/rocke2020/open-agent-memory-benchmark) - Apache-2.0 benchmark comparing self-hosted agent-memory systems through native APIs across answer accuracy, answer-visible context, indexing, and latency, with public question-level results and frozen evaluation plans.

## Papers

- [A-MEM: Agentic Memory for LLM Agents](https://arxiv.org/abs/2502.12110) - Organizes agent notes via Zettelkasten-style linking and evolution for dynamic retrieval (NeurIPS 2025).
- [Generative Agents: Interactive Simulacra of Human Behavior](https://arxiv.org/abs/2304.03442) - Introduces a memory stream with reflection and retrieval to simulate believable behavior (UIST 2023).
- [HippoRAG: Neurobiologically Inspired Long-Term Memory for LLMs](https://arxiv.org/abs/2405.14831) - Combines knowledge graphs with Personalized PageRank, inspired by hippocampal indexing, for long-term retrieval (NeurIPS 2024).
- [MemGPT: Towards LLMs as Operating Systems](https://arxiv.org/abs/2310.08560) - Virtual context management (the origin of Letta).
- [MemoryBank: Enhancing LLMs with Long-Term Memory](https://arxiv.org/abs/2305.10250) - Long-term memory via an Ebbinghaus-inspired forgetting curve and event summarization (2023).
- [SLoD: Semantic Level of Detail for Knowledge Graphs](https://arxiv.org/abs/2603.08965) - Discovering abstraction boundaries via spectral heat diffusion over hyperbolic embeddings (Mnemoverse).
- [Zep: A Temporal Knowledge Graph Architecture for Agent Memory](https://arxiv.org/abs/2501.13956) - Describes the Graphiti temporal knowledge-graph engine for agent memory, with retrieval-benchmark evaluation (2025).

## Contributing

Open a pull request adding one tool, in the right section, in alphabetical order, with a short factual description (no marketing language). New sections are welcome if a genuine category is missing. See [CONTRIBUTING.md](CONTRIBUTING.md) for the full guidelines.

## License

[CC0-1.0](https://creativecommons.org/publicdomain/zero/1.0/). To the extent possible under law, contributors have waived all copyright and related rights to this list.
