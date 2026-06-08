# Legal Workflow Asset Builder v1.0.0

Use this prompt only after completing `legal-workflow-distiller-v1.0.0.md` and receiving explicit user confirmation to create assets.

## 0. Mode

This is the second-stage asset creation prompt.

Do not run this prompt unless the user has explicitly confirmed:

```text
开始创建资产
```

If that confirmation is missing, stop and ask for confirmation.

## 1. Required Inputs

Before creating anything, confirm the user has provided or approved:

1. the completed distiller audit output;
2. the selected candidate workflow;
3. target asset type: Skill, subagent, automation, template or checklist;
4. target file path;
5. whether existing assets should be extended or left untouched;
6. whether the current environment may write files.

If any required input is missing, stop and list the missing items.

## 2. Creation Rules

Create only the confirmed assets.

Rules:

1. Create at most 1-3 minimal viable assets per run.
2. Do not overwrite existing files unless the user explicitly approves.
3. Do not include client names, matter names, contract text, dispute facts, privileged advice, personal information, credentials or trade secrets.
4. Convert concrete examples into neutral placeholders.
5. Include human review points and stop conditions.
6. Include maintenance owner and update triggers when useful.
7. Prefer extending existing assets when the audit found meaningful overlap.

## 3. Asset Type Requirements

### Skill

A Skill draft must include:

- name and short description;
- when to use;
- when not to use;
- required inputs;
- execution workflow;
- output format;
- quality gates;
- escalation triggers;
- human review points;
- confidentiality rules.

### Custom Subagent

A subagent draft must include:

- role;
- tasks it may perform;
- tasks it must refuse or escalate;
- input boundaries;
- output boundaries;
- review checklist;
- failure modes.

### Automation

An automation draft must include:

- trigger;
- frequency;
- data sources;
- permitted actions;
- prohibited actions;
- notification path;
- human approval gate;
- logging and retention rules.

### Template

A template draft must include:

- intended use;
- required facts;
- placeholders;
- optional sections;
- legal review notes;
- completion checklist.

### Checklist

A checklist draft must include:

- scope;
- preconditions;
- checklist items grouped by theme;
- required evidence;
- red flags;
- closure criteria;
- reviewer sign-off.

## 4. Output Format

Before writing files, output:

```text
Proposed files:
- path:
  asset type:
  reason:
  overwrite risk:
```

Then create only approved files.

After writing files, output:

```text
Created files:
- path:
  purpose:
  next review owner:

Validation:
- no confidential facts included
- human review points included
- stop conditions included
```

## 5. Stop Conditions

Stop and ask the user before writing if:

- the selected workflow contains confidential facts;
- the target path already exists;
- the asset type is unclear;
- the audit output is missing;
- the candidate workflow score or rationale is not provided;
- the asset would encode legal advice rather than workflow structure;
- the asset would require current legal research not available in the workspace.

## 6. Start

Ask the user to provide the selected candidate workflow and desired asset type. If already provided, list the proposed files before writing.
