# Agent playbooks

Public reusable guidance. The [authoring contract](AGENTS.md) owns contribution rules.

## Rulesync pilot

Authored pilot skills live in `.rulesync/skills/`. Use Rulesync 43.8.2:

```sh
npx --yes rulesync@43.8.2 install --frozen
npx --yes rulesync@43.8.2 generate
```

The default preview writes Claude Code and Codex skills under `.rulesync-output/`,
leaving active installations untouched. Installation fetches dependencies;
generation emits runtime files. Commit `rulesync.jsonc` and a `rulesync.lock` when external sources are selected,
not curated caches or generated output. Sources and skill selections are explicit.

For an update, change the pinned source revision, run `install --update`, review
the source diff and lockfile, then regenerate in a fresh preview directory.
Local additions use distinct skill names. A same-name local skill replaces the
entire upstream skill; upstream changes require manual review, not an automatic merge.

Hermes skills require global scope in this version. Verify generation with an
isolated home before the integration owner selects a real profile. Installed files
do not prove runtime loading or implicit selection.

Generate into fresh, exclusively owned output directories. Default generation can
leave removed companion files, while `--delete` can remove unrelated skills.
Verify the complete output file manifest, preserve the previous config/lock/source
revision and output snapshot, and restore that snapshot for rollback. Mixed-owner
installation cleanup belongs to the scoped rollout, not this preview.

## Consumer selection

Select this repository’s `.rulesync/skills` source path and `linear-workflow`
explicitly from a reviewed commit. For GitHub transport the source form is
`loop-guardian/agent-playbooks@<reviewed-commit>:.rulesync/skills`.
Workspace adaptations remain additive skills in their owning repositories.
Teammates can consume this baseline without access to a personal repository.
