# Repository architecture

This repository follows the shared Nykuto standard.

## Layers

1. Editable standards and documentation.
2. Reusable AI/project instructions.
3. Validation scripts.
4. GitHub workflows.

## Expected folders

```txt
.github/   GitHub workflows and AI instructions
docs/      project documentation
scripts/   validation and maintenance scripts
```

Additional folders may exist when the core repository receives reusable algorithms, schemas, templates, or pedagogical standards.

## AI workflow

Before editing:

1. Read `SOURCE_OF_TRUTH.md`.
2. Read `AGENTS.md`.
3. Read `.github/copilot-instructions.md`.
4. Identify whether the target file is source, generated output, documentation, workflow, or asset.

Before merging:

1. Confirm the change is narrow.
2. Confirm checks are green.
3. Confirm the user approved the merge.

## Hygiene

Run:

```bash
node scripts/validate-repository-hygiene.js
```

The validator blocks known dangerous stale files and reports suspicious temporary or backup-style paths for review.
