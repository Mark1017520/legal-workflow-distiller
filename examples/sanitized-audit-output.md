# Sanitized Audit Output

This is a sample output showing what a completed audit may look like. It is intentionally generic and does not include client, matter, contract or personal data.

## 1. Accessible Materials

| Material Type | Status | Notes |
|---|---|---|
| README / project docs | Found | Provides workspace purpose and safe example scope |
| Existing templates | Found | One contract review note template |
| Existing checklists | Found | One open-source review checklist |
| Existing Skills | Not found | No legal Skills detected |
| Recent legal work summaries | Found | Sanitized summaries only |
| Confidential source files | Not provided | No live contracts, disputes or personal data |

## 2. Existing Asset Coverage Matrix

| Legal Workflow Area | Existing Asset | Coverage | Gap |
|---|---|---:|---|
| Contract review | Template | Medium | No issue taxonomy or escalation rules |
| Open-source review | Checklist | Medium | No SaaS/private deployment distinction |
| AI feature review | None | Low | No reusable workflow |
| Model vendor review | None | Low | No DPA/security checklist |
| Privacy request review | None | Low | No deletion/access workflow |
| Marketing claims review | None | Low | No substantiation checklist |

## 3. Candidate Workflow Scoring

| Rank | Candidate Workflow | Reuse | Structure | Risk Control | Asset Fit | Maintenance | Total | Recommended Asset |
|---:|---|---:|---:|---:|---:|---:|---:|---|
| 1 | AI feature launch legal review | 5 | 5 | 5 | 5 | 4 | 24 | Skill |
| 2 | Model vendor DPA review | 5 | 4 | 5 | 4 | 4 | 22 | Checklist + template |
| 3 | App SDK permission review | 4 | 5 | 5 | 4 | 4 | 22 | Skill or checklist |
| 4 | Data deletion request review | 4 | 4 | 5 | 4 | 4 | 21 | Template + checklist |
| 5 | Marketing claims substantiation | 4 | 4 | 4 | 4 | 3 | 19 | Checklist |
| 6 | Open-source license review | 3 | 4 | 4 | 3 | 3 | 17 | Extend existing checklist |

## 4. Top 3 Assetization Recommendations

### 1. AI Feature Launch Legal Review Skill

**Why it is valuable:** AI features appear repeatedly and require structured checks across data, vendor, user-facing claims, human review, logging and launch gate.

**Recommended asset:** Skill.

**Minimum contents:**

- applicable AI feature types
- required PRD facts
- data and model supplier questions
- high-risk launch blockers
- output format with risk level and gate
- human legal/privacy/security review points

**Do not include:** real feature names, customer data, production model prompts or confidential incident details.

### 2. Model Vendor DPA Review Checklist

**Why it is valuable:** Vendor model reviews reuse similar contract and security questions.

**Recommended asset:** checklist plus negotiation note template.

**Minimum contents:**

- data role
- training/use restriction
- subprocessors
- data location
- security controls
- deletion/return
- incident notice
- audit and liability

**Human review:** required for production personal data, cross-border transfers or regulated industries.

### 3. App SDK Permission Review Checklist

**Why it is valuable:** SDK reviews have repeatable inputs and clear evidence requirements.

**Recommended asset:** Skill or checklist.

**Minimum contents:**

- SDK name and version
- permission list
- actual network behavior
- initialization timing
- consent and privacy disclosure
- vendor terms
- app store risk

**Human review:** required for location, clipboard, contact list, device identifiers or background collection.

## 5. Skip Or Defer Items

| Item | Recommendation | Reason |
|---|---|---|
| Bespoke contract negotiation strategy | Skip | Too matter-specific and confidential |
| One-off regulator response memo | Defer | Needs human-led matter context |
| Unstructured meeting notes | Skip | Not enough stable workflow signal |

## 6. Human Review Points

- Legal owner must approve each reusable asset before team use.
- Privacy owner must review workflows involving personal data.
- Security owner must review workflows involving SDKs, logs or vendors.
- No asset should contain client facts, contract excerpts or privileged strategy.
- High-risk workflows should include escalation triggers and stop conditions.

## 7. Suggested Creation Order

1. Create `skills/ai-feature-launch-review/SKILL.md`.
2. Create `checklists/model-vendor-dpa-review.md`.
3. Extend `checklists/open-source-review-checklist.md` only after reviewing current checklist coverage.

## 8. Final Summary

The workspace contains several repeatable legal workflows. The strongest candidate is AI feature launch review because it has repeatable facts, recurring risk dimensions and clear launch gates. Model vendor DPA review and App SDK permission review are also strong candidates. Matter-specific negotiation and regulator response materials should not be converted into reusable assets without additional human review.
