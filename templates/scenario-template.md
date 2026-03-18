# Scenario Template

Use this template when contributing new test scenarios. Copy this file and fill in the sections.

---

### Q[NUMBER]. [Scenario Name]

**Threat:** [Category] – [Subcategory]

<!--
Categories: Prompt Injection, Data Leakage, Jailbreak, Role Confusion, Hallucination,
Over-Permissioned, Social Engineering, Steganography, Voice Risk, Multi-Modal,
Video/Streaming, Tools/Integration, RAG, Memory, Agentic, MCP/Tool Ecosystem,
Computer/Browser Use, Multi-Turn, Supply Chain, Multilingual, Financial
-->

**Scenario:** [Describe the attack in 1-2 sentences. Be specific — include an example prompt or action the attacker would take.]

**Variations:**
- [Alternative phrasing or approach 1]
- [Alternative phrasing or approach 2]
- [Optional: additional variation]

**Expected Safe Response:**

> "[Write the ideal response the AI system should give. Be concrete — this is what testers will compare against.]"

**Mitigation:** [Specific defensive measures. Be actionable — "implement X" not "be more secure."]

**Prerequisites:** [What setup is needed? Special tools, environments, permissions, or configurations required to run this test.]

**Estimated Time:** [How long should this test take to execute? e.g., "5 minutes," "15-30 minutes for all variations"]

**Evidence Type:** [What evidence should be captured? e.g., "Full text response log," "Screenshot of tool call," "Audio recording," "Screen recording"]

**False Positive Risk:** [Could a legitimate use case trigger this test? e.g., "Low — this attack pattern is clearly adversarial" or "Medium — legitimate users may phrase requests similarly"]

---

## Metadata (for new categories only)

If proposing a new category, include:

- **Phase:** [1/2/3/4]
- **Default Severity:** [Critical/High/Medium/Low]
- **OWASP LLM v2.0:** [LLM01-LLM10 mapping]
- **EU AI Act:** [Article reference]
- **MITRE ATLAS:** [Technique ID if applicable]
