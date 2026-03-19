# Telecom Integration Notes

## Focus Areas

- Message delivery in Russia is operationally sensitive even when the API surface looks simple.
- Split provider selection, consent logging, and delivery retries into separate decisions.

## Practical Guidance

- Normalize phone numbers before they reach the provider layer.
- Keep a deterministic resend policy for OTP and recovery flows.
- Store provider message IDs so support teams can investigate failures.
- Maintain at least one fallback path for critical transactional traffic.

## Agent Boundaries

- Agents can classify traffic, choose a routing strategy, and prepare send payloads.
- Agents should not silently trigger production sends or rewrite consent rules.
