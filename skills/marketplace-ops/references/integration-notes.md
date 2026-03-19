# Marketplace Ops Integration Notes

## Focus Areas

- Marketplace operations are dominated by exceptions, not just happy-path catalog management.
- Incident severity, platform SLA, and rollback cost should shape the workflow.

## Practical Guidance

- Keep platform-specific case IDs and evidence links attached to every incident summary.
- Separate diagnosis, draft response, and final operator action.
- Use explicit severity tiers so support queues can prioritize correctly.
- Capture whether a rollback touches content, price, stock, or shipment state.

## Agent Boundaries

- Agents can classify incidents, draft responses, and prepare escalation packets.
- Agents should not auto-accept claims or close seller disputes without a human checkpoint.
