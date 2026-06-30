# Source of truth — Med Nykuto Core

This repository is the core standard/reference repository for Med Nykuto platform organization, pedagogy, AI workflows, documentation, and project rules.

## Branches

- `main` is the main branch.
- Use a short working branch for each change.
- Open a PR before merging.

## Editable sources

The editable source of truth is the project documentation, standards, algorithms, and any source folders declared in this repository.

Generated, copied, temporary, or exported files should never be treated as primary sources unless explicitly documented.

## Documentation

- `AGENTS.md` = operating rules for AI agents.
- `.github/copilot-instructions.md` = repository-level AI instructions.
- `docs/site-architecture.md` = repository organization and workflow.

## Validation

The hygiene script is:

```bash
node scripts/validate-repository-hygiene.js
```

The GitHub workflow is:

```txt
.github/workflows/repository-hygiene.yml
```

## Forbidden stale material

Do not keep temporary archives, backup copies, debug workflows, or old generated dumps in the repository unless explicitly documented and validated.
