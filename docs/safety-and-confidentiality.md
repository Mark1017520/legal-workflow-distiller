# Safety And Confidentiality

This project is designed for legal workflow analysis, not legal advice.

## Core Principles

- Use audit-only mode first.
- Do not create reusable assets from client-specific facts.
- Do not preserve privileged or confidential materials in prompts, examples or templates.
- Do not treat model output as final legal advice.
- Require human legal review for high-risk outputs.

## Data Sensitivity Levels

| Level | Description | Handling |
|---|---|---|
| S0 | Public, non-sensitive examples | Safe for examples |
| S1 | Internal but low-risk process information | Use with care |
| S2 | Confidential business or legal information | Sanitize before use |
| S3 | Personal data, privileged materials, trade secrets, investigation records, credentials | Do not include unless environment and policy explicitly allow |

## Materials To Remove Or Mask

- client names
- counterparty names
- employee names
- email addresses and phone numbers
- IDs, account numbers, store IDs, merchant IDs
- contract text
- dispute facts
- regulatory correspondence
- investigation records
- source code secrets
- API keys, tokens, passwords and cookies
- logs with personal data or secrets

## Legal Review Boundary

The distiller can identify repeatable workflows and asset candidates. It should not:

- decide final legal risk
- replace counsel review
- create legal conclusions for live matters
- invent legal authorities
- store confidential facts in reusable assets

## Asset Creation Boundary

Reusable assets may include:

- process steps
- review dimensions
- required input materials
- output format
- quality gates
- escalation triggers
- human review points

Reusable assets must not include:

- real client facts
- real contracts
- confidential negotiations
- dispute strategies
- regulatory case details
- personal information
- privileged analysis

## Incident Response

If sensitive data is accidentally included:

1. Stop the run.
2. Do not create assets from the output.
3. Remove or quarantine generated files.
4. Notify the appropriate internal owner.
5. Re-run only with sanitized materials.
