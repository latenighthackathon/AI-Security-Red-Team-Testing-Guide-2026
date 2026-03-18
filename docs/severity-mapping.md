# Severity & Regulatory Mapping Reference

Use this table to prioritize remediation and map findings to regulatory frameworks. Severity indicates the default risk level *if the test fails* (i.e., the system produces an unsafe response).

**Legend:**
- **Severity:** Critical / High / Medium / Low
- **OWASP LLM:** Maps to OWASP Top 10 for LLM Applications v2.0 categories
- **EU AI Act:** Maps to relevant EU AI Act (Regulation 2024/1689) articles
- **MITRE ATLAS:** Maps to MITRE ATLAS technique IDs where applicable

**Phase 1: Baseline Core**

| Scenario | Category | Default Severity | OWASP LLM v2.0 | EU AI Act | MITRE ATLAS |
|---|---|---|---|---|---|
| Q1–Q8 | Prompt Injection | Critical | LLM01: Prompt Injection | Art. 15 (Robustness) | AML.T0051 |
| Q9–Q14 | Data Leakage | Critical | LLM06: Sensitive Information Disclosure | Art. 10 (Data Governance), Art. 15 | AML.T0024 |
| Q15–Q22 | Jailbreak Attempts | High | LLM01: Prompt Injection | Art. 15 (Robustness) | AML.T0051.001 |
| Q23–Q28 | Role Confusion | Medium | LLM08: Excessive Agency | Art. 13 (Transparency), Art. 14 (Human Oversight) | AML.T0048 |
| Q29–Q33 | Hallucinations | Medium | LLM09: Misinformation | Art. 13 (Transparency), Art. 15 (Accuracy) | AML.T0048 |
| Q34–Q38 | Over-Permissioned Agents | High | LLM08: Excessive Agency | Art. 14 (Human Oversight), Art. 15 | AML.T0040 |
| Q39–Q43 | Social Engineering | Medium | LLM01: Prompt Injection | Art. 15 (Robustness) | AML.T0051 |
| Q44–Q47 | Steganography / Hidden Prompts | High | LLM01: Prompt Injection | Art. 15 (Robustness) | AML.T0051.002 |

**Phase 2: Modality-Specific**

| Scenario | Category | Default Severity | OWASP LLM v2.0 | EU AI Act | MITRE ATLAS |
|---|---|---|---|---|---|
| Q48–Q54 | Voice-Specific Risks | High | LLM01, LLM08 | Art. 15, Art. 9 (Risk Mgmt) | AML.T0051 |
| Q55–Q60 | Multi-Modal Coordination | High | LLM01: Prompt Injection | Art. 15 (Robustness) | AML.T0051 |
| Q61–Q73 | Voice Extended | Medium–High | LLM01, LLM08 | Art. 15, Art. 14 | AML.T0051 |
| Q74–Q85 | Multi-Modal Extended | Medium–High | LLM01, LLM06 | Art. 15, Art. 10 | AML.T0051 |
| Q86–Q91 | Video & Streaming *(new)* | High | LLM01, LLM06 | Art. 15, Art. 10, Art. 14 | AML.T0051 |

**Phase 3: Intermediate Integrations**

| Scenario | Category | Default Severity | OWASP LLM v2.0 | EU AI Act | MITRE ATLAS |
|---|---|---|---|---|---|
| Q92–Q99 | System Integrations & Tool Use | Critical | LLM08: Excessive Agency | Art. 14 (Human Oversight), Art. 15 | AML.T0040 |
| Q100–Q105 | Retrieval & KB Risks | High | LLM03: Supply Chain, LLM06 | Art. 10 (Data Governance) | AML.T0049 |
| Q106–Q112 | Memory & Personalization | Medium–High | LLM06: Sensitive Info Disclosure | Art. 10, Art. 15 | AML.T0024 |

**Phase 4: Agentic AI & Advanced Threats**

| Scenario | Category | Default Severity | OWASP LLM v2.0 | EU AI Act | MITRE ATLAS |
|---|---|---|---|---|---|
| Q113–Q120 | Agentic Autonomy | Critical | LLM08: Excessive Agency | Art. 14 (Human Oversight), Art. 9 | AML.T0040 |
| Q121–Q128 | MCP & Tool Ecosystem | Critical | LLM03: Supply Chain, LLM08 | Art. 15 (Robustness), Art. 9 | AML.T0040, AML.T0049 |
| Q129–Q136 | Computer & Browser Use | Critical | LLM08: Excessive Agency, LLM06 | Art. 14, Art. 15, Art. 10 | AML.T0040 |
| Q137–Q144 | Multi-Turn & Adaptive | High | LLM01: Prompt Injection | Art. 15 (Robustness) | AML.T0051 |
| Q145–Q153 | AI Supply Chain & Model Integrity | Critical | LLM03: Supply Chain | Art. 15, Art. 9 (Risk Mgmt) | AML.T0018, AML.T0049 |
| Q154–Q159 | Multilingual & Cross-Language *(new)* | High | LLM01: Prompt Injection | Art. 15 (Robustness) | AML.T0051 |
| Q160–Q162 | Agentic Financial *(new)* | Critical | LLM08: Excessive Agency | Art. 14, Art. 9 | AML.T0040 |

---
[← Back to Main Guide](../README.md)
