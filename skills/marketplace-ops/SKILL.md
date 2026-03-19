---
name: marketplace-ops
description: Use this skill when a task involves operational workflows across Russian marketplaces such as order incidents, returns, SLA breaches, content rollback, seller support queues, or cross-platform exception handling. Do not use it for basic catalog edits or pricing analysis covered by the main marketplaces skill.
---

# Marketplace-Ops Skill

Use this skill for incident-heavy marketplace operations that need escalation logic and auditability.

## Use This Skill For

- Order exceptions and shipment incidents
- Returns, claims, and SLA breach handling
- Seller-support queue triage
- Cross-platform rollback and escalation workflows
- Operational dashboards for marketplace incidents

## Workflow

1. Identify the affected platform and incident type.
2. Separate read-only diagnosis from live seller actions.
3. Define SLA, rollback, and escalation boundaries before any mutation.
4. Preserve order, listing, and case identifiers in the result.
5. Return an operator-ready action plan with ownership and next step.

## Output Contract

```json
{
  "platform": "ozon|wildberries|yandex-market|multi",
  "incident_type": "orders|returns|claims|sla|rollback|support",
  "severity": "low|medium|high|critical",
  "requires_operator_queue": true,
  "audit_log_required": true
}
```

## Guardrails

- Do not auto-resolve financial or seller-penalty disputes.
- Make rollback boundaries explicit before touching listings or order state.
- Keep support ownership and next action visible in the final output.
- Preserve incident evidence for claims and appeals.

## Bundled Resources

- See `references/integration-notes.md` for escalation and rollback guidance.
- See `examples/output.json` for a minimal result shape.
- See `schemas/output.schema.json` for the output contract schema.
