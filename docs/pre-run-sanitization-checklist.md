# Pre-Run Sanitization Checklist

Use this checklist before running the legal workflow distiller on any workspace.

## Workspace Scope

- [ ] I know which folder or repository will be audited.
- [ ] The workspace does not contain unrelated private materials.
- [ ] The workspace does not contain live matter files unless approved.
- [ ] I understand whether the agent can access parent directories.

## Client And Matter Information

- [ ] Client names are removed or replaced with neutral labels.
- [ ] Counterparty names are removed or replaced.
- [ ] Matter names and project code names are removed or generalized.
- [ ] Case numbers, regulator references and dispute IDs are removed.
- [ ] Privileged legal strategy is removed.

## Personal Information

- [ ] Employee names are removed.
- [ ] Customer names are removed.
- [ ] Email addresses are removed.
- [ ] Phone numbers are removed.
- [ ] Addresses are removed.
- [ ] Identity numbers, passport numbers and government IDs are removed.
- [ ] Account IDs, store IDs, merchant IDs and user IDs are masked.

## Contracts And Legal Documents

- [ ] Full contract text is removed unless explicitly approved.
- [ ] Sensitive pricing, liability caps and negotiation positions are removed.
- [ ] Draft redlines are removed or generalized.
- [ ] Privileged comments are removed.
- [ ] Confidential exhibits and schedules are removed.

## Product And Business Confidentiality

- [ ] Unannounced product plans are removed or generalized.
- [ ] Internal roadmaps are removed.
- [ ] Security architecture details are removed or summarized.
- [ ] Commercial strategy is removed.
- [ ] Internal risk ratings are generalized if needed.

## Technical Secrets

- [ ] API keys are removed.
- [ ] Tokens are removed.
- [ ] Passwords are removed.
- [ ] Cookies and session IDs are removed.
- [ ] Private keys and certificates are removed.
- [ ] Logs are checked for secrets and personal data.

## Output Safety

- [ ] I will not publish the raw audit output without review.
- [ ] I will not convert case-specific facts into reusable assets.
- [ ] I will review any proposed Skill, template or checklist before team use.
- [ ] I will mark high-risk workflows for human legal review.

## Final Confirmation

- [ ] The current environment is approved for the remaining materials.
- [ ] The prompt will start in `AUDIT_ONLY` mode.
- [ ] The agent is not authorized to create files unless I later say `开始创建资产`.
