# Governance & RACI Template

Use this template to establish clear ownership for AI red team testing. Customize roles and names for your organization.

**RACI Matrix**

| Activity | Red Team Lead | AI/ML Engineer | Security Team | Product Owner | Engineering Lead | Compliance/Legal |
|---|---|---|---|---|---|---|
| Define test scope & schedule | **R** | C | C | **A** | C | I |
| Set up test environment | C | **R** | C | I | **A** | I |
| Execute test scenarios | **R** | **R** | C | I | I | I |
| Score and classify results | **R** | **R** | C | I | I | C |
| Prioritize remediation | C | C | C | **A** | **R** | C |
| Implement fixes | I | **R** | C | I | **A** | I |
| Verify fixes (retest) | **R** | C | C | I | I | I |
| Report to leadership | **R** | I | C | **A** | I | C |
| Regulatory mapping & compliance | I | I | C | I | I | **R** |
| Maintain this guide | **R** | C | C | I | I | I |

**R** = Responsible (does the work), **A** = Accountable (owns the outcome), **C** = Consulted, **I** = Informed

**Additional Roles to Consider**

Depending on your organization's size and regulatory requirements, add these roles:

| Role | When Needed | Key Responsibilities |
|---|---|---|
| **Data Protection Officer (DPO)** | Required under EU AI Act / GDPR | Consulted on data handling in tests, evidence retention, PII in test scenarios |
| **ML/Model Ops Engineer** | Systems with model versioning, fine-tuning, or adapter management | Responsible for model integrity testing (Q145–Q153), adapter verification |
| **Incident Response Lead** | All production systems | Accountable for immediate response when Critical (9–10) findings are discovered in production |

**Conflict Resolution**

If the Red Team Lead and Product Owner disagree on a PASS/FAIL classification:

1. Both document their rationale in the test log
2. Escalate to the Engineering Lead for technical assessment
3. If unresolved, escalate to CTO/VP Engineering for final decision
4. Document the decision and reasoning regardless of outcome

**Governance Cadence**

| Activity | Frequency | Owner |
|---|---|---|
| Phase 1 automated regression | Every deployment (CI/CD gate) | Engineering Lead |
| Phases 1–3 full test cycle | Weekly or bi-weekly | Red Team Lead |
| Full test (all phases, Q1–Q167) | Monthly | Red Team Lead |
| Red team findings review | After each test cycle | Product Owner + Security Team |
| Remediation status check | Weekly | Engineering Lead |
| Executive risk briefing | Monthly or quarterly | Product Owner |
| Guide update & maintenance | Quarterly or after major incidents | Red Team Lead |
| Regulatory compliance review | Quarterly | Compliance/Legal |

**Escalation Path**

```
Score 1-4 (PASS)
  → Document in test log
  → No further action required

Score 5-6 (CONDITIONAL)
  → Document with evidence
  → Assign remediation owner
  → Set timeline (typically 2-4 weeks)
  → Does NOT block deployment for Phases 1-3
  → BLOCKS deployment for Phase 4 (agentic)

Score 7-8 (FAIL - High Risk)
  → Document with full evidence
  → Escalate to Engineering Lead + Product Owner within 24 hours
  → Blocks deployment
  → Remediation timeline: 1-2 weeks
  → Retest required before deploy

Score 9-10 (FAIL - Critical Risk)
  → Document with full evidence
  → Escalate to Security Team + Engineering Lead + Product Owner IMMEDIATELY
  → Blocks deployment
  → If in production: initiate incident response
  → Remediation timeline: 48-72 hours
  → Full retest of category required before deploy
```

---
[← Back to Main Guide](../README.md)
