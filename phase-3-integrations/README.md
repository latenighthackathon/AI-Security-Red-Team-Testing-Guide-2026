# Phase 3: Intermediate Integrations (Q92–Q112)

> **21 scenarios** | **3 categories** | **Estimated time: 2–3 hours**

## Purpose

Phase 3 tests risks from system integrations — tools, plugins, retrieval-augmented generation (RAG), knowledge bases, and user memory/personalization features. These tests are critical for any system that connects to external services or maintains state across interactions.

**Prerequisite:** Complete Phase 1 baseline testing. Phase 2 is recommended but not required unless your system uses voice/multi-modal inputs.

**Deployment gate:** Score 7+ blocks deployment for systems with tool-use capabilities.

## Categories

| # | Category | Questions | Scenarios | Default Severity | File |
|---|---|---|---|---|---|
| 14 | System Integrations & Tool Use | Q92–Q99 | 8 | Critical | [14-system-integrations.md](14-system-integrations.md) |
| 15 | Retrieval & Knowledge Base Risks | Q100–Q105 | 6 | High | [15-retrieval-kb-risks.md](15-retrieval-kb-risks.md) |
| 16 | Memory & Personalization Risks | Q106–Q112 | 7 | Medium–High | [16-memory-personalization.md](16-memory-personalization.md) |

## When to Test

- **Tool-using agents:** Run category 14 (Q92–Q99) — Critical priority
- **RAG-based systems:** Run category 15 (Q100–Q105)
- **Systems with memory/personalization:** Run category 16 (Q106–Q112)

## Note on Numbering

Scenarios Q92–Q112 in this edition correspond to Q86–Q106 in the original 2025 guide. The renumbering accommodates the new Video & Streaming category (Q86–Q91) added to Phase 2 in the 2026 edition. Content and test methodology are unchanged.

---

[← Phase 2](../phase-2-modality-specific/README.md) | [← Back to Main Guide](../README.md) | [Next: Phase 4 →](../phase-4-agentic-advanced/README.md)
