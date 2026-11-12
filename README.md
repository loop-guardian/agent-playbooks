# Agent playbooks

Public skills for service-specific judgment and reusable work conventions.
The [authoring contract](AGENTS.md) owns contribution rules.

## Linear pilot

- `linear-workflow` supplies the work-structure baseline and its reference.

Install it from a reviewed Git revision using the Skills CLI:

```sh
npx skills@1.7.6 add mmroczka/agent-playbooks@<reviewed-revision> \
  --skill linear-workflow -a codex claude-code
```

Replace the revision placeholder before running. Add a workspace adaptation from
its owning repository when required. Referencing another skill does not install
it. Each complete skill directory is portable; Hermes requires installation in
the intended profile's skill catalog and separate verification there.

## Ownership and updates

This repository owns shared defaults. Workspace adaptations own only their
differences and source pointers. A consumer's `upstream.lock` records the base
revision for review; it is provenance metadata, not an automatic dependency resolver.
Update dependencies explicitly through a consumer PR. Do not assume installer
updates merge local modifications.

Use workspace policy for expected differences. Use a small Git patch only for a
core instruction that cannot be expressed by that policy, retaining its base
revision and rationale. Review upstream changes, resolve conflicts in a working
checkout and verify the resolved instructions before updating an installation.
Promote generally useful patches into the base and retire redundant downstream
patches. No patch engine or new installer is included in this pilot.
