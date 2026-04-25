# Aletheia-Core Policy Packs

Policy packs are tested, signed manifest files that tell Aletheia-Core how to enforce security rules for your specific AI system type. Each pack includes: plain-English rules, formal control mappings, test cases per rule, and implementation notes.

## How Policy Packs Work

- **Self-hosters:** Download the template, customize for your system, load into your local Aletheia-Core instance.
- **Hosted API customers:** We configure and deploy a signed manifest to your dedicated endpoint.
- **Manifest signing subscription:** We sign your manifest updates monthly with the Aletheia-Core root key ($99/month).

## Policy Packs

| Pack Name | Use Case | Rules Included | Template | Price |
|-----------|----------|-----------------|----------|-------|
| Customer Service AI | Customer support chatbots, ticket systems, refund flows | 7 rules: PI-001, TS-003, DE-002, LQ-001, TS-005, DE-004, TS-007 | `/manifests/customer-service.json` (Phase 2) | $499 |
| Sales Bot | Lead qualification, pricing discussions, demo booking | 5 rules: BL-001, BL-002, BL-003, LQ-002, TS-006 | `/manifests/sales-bot.json` (Phase 2) | $299 |
| Document Q&A | RAG systems, knowledge base search, document analysis | 5 rules: II-001, BL-004, PI-003, LQ-003, OH-002 | `/manifests/document-qa.json` (Phase 2) | $249 |
| Code Assistant | Code generation, review, explanation tools | 5 rules: OH-001, TS-008, DE-005, LQ-004, TS-009 | `/manifests/code-assistant.json` (Phase 2) | $349 |
| Multi-Agent Orchestration | Agent-to-agent systems, TMRP pipelines, chained LLM workflows | 8 rules: PI-001, PI-006, TS-003, TS-010, DE-006, LQ-001, LQ-005, RA-003 | `/manifests/multi-agent.json` (Phase 2) | $799 |
| Default (OWASP LLM Top 10) | Any AI system — baseline coverage | 10 rules covering all OWASP LLM Top 10 categories | `/manifests/default.json` (Phase 2) | Free with API key |

## Rule Outcome Key

Every rule in a policy pack enforces one of five outcomes:

- **BLOCK** — Request refused before reaching the model.
- **ESCALATE** — Request paused for human approval before execution.
- **LOG** — Request proceeds with enriched audit record.
- **ALLOW** — Request explicitly permitted.
- **EXCEPTION** — Alternative rule applies under specific conditions.

## Manifest Signing

Templates in `/manifests/` are unsigned reference files. Signed manifests carry the Aletheia-Core root Ed25519 signature, proving they cannot be tampered with and match your deployed policy exactly.

- **Unsigned:** Free, self-managed, no external credibility.
- **Signed:** $99/month subscription or included in Audit + Policy Pack service.

## Get a Policy Pack

**Option 1: Use a template**  
Download a policy pack template from `/manifests/` (available Phase 2). Customize for your system and load into your Aletheia-Core instance.

**Option 2: Custom pack from audit findings**  
Book a security audit at [https://aletheia-core.com](https://aletheia-core.com) — $499. We analyze your threat model and deliver a custom manifest signed and ready to deploy.

**Option 3: Full audit + custom pack**  
Comprehensive threat modeling, rule design, test case validation, and signed deployment — from $699. Contact [https://aletheia-core.com](https://aletheia-core.com).
