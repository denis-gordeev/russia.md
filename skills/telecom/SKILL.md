---
name: telecom
description: Use this skill when a task involves Russian telecom workflows such as SMS delivery, voice OTP, number validation, call-routing, consent logging, or messaging/provider failover. Do not use it for generic notifications when telecom-specific delivery constraints are out of scope.
---

# Telecom Skill

Use this skill for telecom-dependent user communications in Russian products.

## Use This Skill For

- SMS and voice OTP workflows
- Provider failover and routing design
- Phone-number validation and normalization
- Delivery observability and retry policies
- Consent-aware messaging operations

## Workflow

1. Classify the channel as `sms`, `voice`, `flash-call`, or `multi`.
2. Separate pre-send validation from actual delivery attempts.
3. Define provider priorities and fallback behavior before going live.
4. Keep consent, template origin, and retry policy explicit.
5. Return a delivery plan or incident triage summary instead of generic messaging advice.

## Output Contract

```json
{
  "channel": "sms|voice|flash-call|multi",
  "task_type": "otp|transactional|support|routing",
  "provider_strategy": "",
  "requires_consent_check": true,
  "fallback_defined": true
}
```

## Guardrails

- Do not send messages without a documented consent basis.
- Keep OTP expiry and resend windows explicit.
- Never hide provider failover assumptions in production messaging flows.
- Preserve delivery IDs and provider responses for incident analysis.

## Bundled Resources

- See `references/integration-notes.md` for failover and consent guidance.
- See `examples/output.json` for a minimal result shape.
- See `schemas/output.schema.json` for the output contract schema.
