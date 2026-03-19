---
name: document-signature
description: Use this skill when a task involves Russian document-signing workflows, certificate-backed approvals, signing ceremony design, or legally significant review gates. Do not use it for plain PDF generation or informal approvals without a signature or attestation layer.
---

# Document-Signature Skill

Use this skill for signature-aware document workflows that need explicit review boundaries.

## Use This Skill For

- Signing-flow design for contracts, applications, or HR documents
- Separation of draft, review, sign, and archive stages
- Mapping who signs what and in which order
- Evidence capture around approvals and certificate use

## Workflow

1. Classify the document as `contract`, `hr`, `filing`, or `internal`.
2. Identify the signing model: single signer, sequential, parallel, or countersign.
3. Separate draft generation from the legally significant signing step.
4. Capture the required evidence trail before and after signature.
5. Return a signing plan with approval checkpoints, not just a document summary.

## Output Contract

```json
{
  "document_type": "contract|hr|filing|internal",
  "signature_mode": "single|sequential|parallel|countersign",
  "requires_certificate_check": true,
  "requires_human_review": true,
  "archive_required": true
}
```

## Guardrails

- Do not imply legal validity from a draft-only workflow.
- Keep the final human review step explicit before signing.
- Preserve signature evidence, timestamps, and archive location requirements.
- Never auto-sign production documents without an approval gate.

## Bundled Resources

- See `references/integration-notes.md` for review and evidence guidance.
- See `examples/output.json` for a minimal result shape.
- See `schemas/output.schema.json` for the output contract schema.
