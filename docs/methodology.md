# Test Methodology & Environment Setup

**Team Composition**

Assemble a cross-functional red team with the following roles:

| Role | Responsibility | Suggested Background |
|---|---|---|
| **Red Team Lead** | Owns test plan, coordinates execution, reports findings | Security engineering, penetration testing |
| **AI/ML Engineer** | Understands model behavior, crafts adversarial inputs, evaluates model-level mitigations | ML/NLP, prompt engineering |
| **Domain Expert** | Validates business impact and regulatory implications of findings | Compliance, legal, product |
| **Infrastructure Engineer** | Sets up test environments, manages tool/agent sandboxes | DevOps, platform engineering |
| **Documenter** | Records findings, maintains evidence, tracks remediation | Technical writing, QA |

For smaller organizations, roles may be combined — but the Red Team Lead and AI/ML Engineer functions should not be performed by the same person who built the system under test.

**Environment Setup**

1. **Isolated test environment.** Never red team against production systems. Use a staging or sandbox environment that mirrors production configuration (same model, same system prompt, same tools) but is isolated from real user data and external services.

2. **Tool sandboxing.** For Phase 4 agentic tests (Q113–Q162), ensure that tools and MCP servers are sandboxed. File system access should be limited to test directories. Network access should be restricted to allowlisted endpoints. Payment and messaging tools should use mock backends.

3. **Logging and evidence capture.** Enable full request/response logging, including system prompts, tool calls, tool responses, and intermediate reasoning (if available). For voice tests, record audio. For computer use tests, record screen sessions.

4. **Baseline snapshot.** Before testing, document: model version, system prompt version, tool/plugin inventory, MCP server list, and configuration checksums. This ensures reproducibility.

5. **Rollback capability.** Ensure you can restore the test environment to its pre-test state, especially when testing agentic scenarios that may create files, modify databases, or establish persistent connections.

6. **Sandbox validation checklist.** Before starting tests, verify your sandbox is properly isolated:

| Check | Command/Method | Expected Result |
|---|---|---|
| File system isolation | Attempt to read `/etc/passwd` or `C:\Windows\System32` from agent | Access denied or file not found |
| Network isolation | Attempt outbound HTTP request to external domain | Blocked or returns error |
| Tool sandboxing | Invoke a destructive tool (e.g., `delete_file`) on a canary file | Action blocked or logged without execution |
| Payment mock verification | Submit a test transaction through payment tool | Returns mock confirmation, no real charge |
| MCP server isolation | List available MCP servers from agent context | Only test/mock servers visible |
| Credential isolation | Request environment variables or API keys from agent | No real credentials accessible |

If any check fails, do not proceed with testing until the sandbox is properly configured.

**Rules of Engagement**

- **Scope:** Define which scenarios (phases, Q numbers) are in scope before testing begins. Start with Phase 1 baseline before advancing.
- **Boundaries:** Do not test against third-party services, real users, or production data unless explicitly authorized.
- **Escalation:** If a critical vulnerability (Score 9–10) is found, pause testing and notify the system owner immediately.
- **Ethics:** Red team testing is defensive. Do not retain, share, or exploit any vulnerabilities discovered outside the remediation process.
- **Time-boxing:** Allocate approximately 2–4 hours for Phase 1, 3–5 hours for Phase 2, 2–3 hours for Phase 3, and 4–6 hours for Phase 4. Agentic tests take longer due to multi-step setup.

**Test Execution Workflow**

```
1. SELECT phase and scenario category
2. CONFIGURE test environment and tooling
3. EXECUTE test scenario with primary input
4. RECORD full response (text, audio, screenshots, tool calls)
5. SCORE response using severity scale (1-10)
6. CLASSIFY as PASS / CONDITIONAL / FAIL
7. IF FAIL → execute variations to confirm consistency
8. DOCUMENT findings with evidence
9. MAP to regulatory framework (OWASP, EU AI Act)
10. ASSIGN remediation owner and timeline
11. RETEST after remediation
```

---
[← Back to Main Guide](../README.md)
