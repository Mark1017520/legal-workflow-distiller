# Usage Guide

## 1. Prepare The Workspace

Run the distiller from the workspace you want to audit. The workspace may include:

- legal memos
- contract review notes
- policy reviews
- compliance checklists
- product review records
- privacy impact assessments
- existing Skills, templates or checklists

Do not run the prompt on unsanitized confidential materials unless your environment is approved for those materials.

## 2. Run The Audit Prompt

Copy:

```text
prompts/legal-workflow-distiller-v1.0.3.md
```

Paste it into Codex or another local coding agent.

The prompt begins in `AUDIT_ONLY` mode. It should not write files.

## 3. Review The Output

The expected output should include:

- accessible materials
- unavailable materials
- existing asset inventory
- candidate workflow list
- candidate scoring table
- recommended asset form
- skip list
- human review points
- suggested creation order

## 4. Choose Candidates

Do not create every candidate. Prefer candidates with:

- repeatable facts and input materials
- stable review logic
- low risk of embedding client-specific facts
- clear human review gates
- high reuse frequency

## 5. Build Assets

After the audit is complete, use:

```text
prompts/legal-workflow-asset-builder-v1.0.3.md
```

Paste the second-stage prompt directly into the same Codex conversation after the audit output. It will read the prior audit result, select the Top 1 candidate by default, and propose files before creating anything.

Copy the whole prompt file body, starting from the first line `# 法律工作流资产创建器 v1.0.3` and ending at the final line of the file. If copying from GitHub, use the raw file view to avoid copying page navigation.

Only build or write assets after the user has confirmed the proposed plan.

## 6. Review Before Team Use

Before sharing assets with a legal team:

- remove all case-specific details
- verify legal boundaries
- confirm human review points
- test on sanitized examples
- add owner and maintenance rules

## Typical Workflow

```text
sanitize materials
→ run audit-only distiller
→ review candidate scoring
→ confirm Top 1-3 assets
→ run asset builder
→ legal owner review
→ team pilot
→ maintain/update
```
