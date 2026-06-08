# Legal Workflow Distiller

An audit-only prompt pack for legal teams who want to identify repeatable legal work and turn it into reusable AI workflow assets.

This project is not a general legal assistant. It helps legal, privacy, compliance, policy, contract and product-legal teams review recent work, identify repeatable workflows, and decide whether each workflow should become a Skill, custom subagent, automation, template, checklist, an extension of an existing asset, or be skipped.

The core prompt runs in **AUDIT_ONLY** mode by default. It should inspect available workspace materials, summarize reusable patterns, score candidate workflows, and recommend assetization paths. It must not create, modify, delete, move, rename or commit files unless the user explicitly starts the asset creation phase.

Chinese introduction: see [README.zh-CN.md](README.zh-CN.md).

## Who It Is For

- In-house legal and compliance teams
- Legal operations teams building reusable AI workflows
- Product counsel, privacy counsel, regulatory counsel and contract teams
- Founders or independent builders creating legal AI workflow assets
- Codex, Claude Code or local workspace users who want a read-only audit before creating Skills or templates

## What It Produces

The distiller prompt can produce:

- Accessible-materials summary
- Existing asset coverage matrix
- Candidate legal workflow list
- Candidate scoring table
- Top assetization recommendations
- Skip list
- Human review points
- Suggested creation order

See [examples/sanitized-audit-output.md](examples/sanitized-audit-output.md).

## Quick Start

1. Review the pre-run checklist:

```text
docs/pre-run-sanitization-checklist.md
```

2. Copy the core prompt:

```text
prompts/legal-workflow-distiller-v1.0.2.md
```

3. Paste it into Codex or another local coding agent from the workspace you want to audit.

4. Do not include confidential or personal data unless your environment is approved for that data.

5. Review the output and decide which candidates, if any, should move to the asset creation phase.

6. Paste the second-stage prompt into the same Codex conversation when you are ready to continue. You do not need to edit the prompt body; it will read the first-stage audit output, choose the Top 1 candidate by default, and propose a file plan before creating anything.

## Prompt Files

- `prompts/legal-workflow-distiller-v1.0.2.md`: audit-only workflow distillation prompt
- `prompts/legal-workflow-asset-builder-v1.0.2.md`: second-stage prompt for creating confirmed assets

The two prompt files are two workflow phases, not English/Chinese alternatives.

## Documentation

- `docs/usage.md`: how to run the prompt
- `docs/safety-and-confidentiality.md`: legal-data safety boundaries
- `docs/pre-run-sanitization-checklist.md`: practical pre-run checklist
- `docs/project-overview-for-sharing.md`: Chinese sharing and project overview copy

## Examples

- `examples/sanitized-audit-brief.md`: safe input brief
- `examples/sanitized-audit-output.md`: complete sample output

## Safety Boundary

This project does not provide legal advice. It does not replace review by qualified legal counsel. It is a workflow-audit and workflow-design aid.

The audit prompt must not preserve client names, case facts, contract text, internal investigations, personal information, credentials, API keys, privileged material or trade secrets in reusable workflow assets.

## License

MIT License. See [LICENSE](LICENSE).
