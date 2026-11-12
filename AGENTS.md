# Authoring contract

Keep each instruction in one authoritative place. Before adding guidance, inspect
the service instructions and schemas available in the current session, plus existing
skills and workspace policy. Retain only guidance those sources do not provide.
Link to authoritative references instead of copying their rules.

Never embed executable tool identifiers, tool inventories, argument schemas or
call recipes in skill instructions or their references. Discover capabilities
through the configured service interface; keep connection setup and access control
outside skills. Skill text owns decisions and conventions, independent of the
MCP client, connection method or gateway.

Keep service-specific operational judgment separate from workflow preferences.
When useful guidance is missing or unclear, improve the existing skill or reference
that owns it. Add a service skill only when the live interface leaves useful
guidance unstated and no existing skill is an appropriate home.
Keep workspace identities, private policies and credentials out of this public
repository. Consumer-specific changes belong with that consumer.

Keep investigation logs and point-in-time validation results in PR evidence.
Repository documentation should describe maintained guidance.

Before publishing, validate skill frontmatter and references, review for semantic
duplication and inspect realistic examples. A clean textual merge does not prove
that an updated instruction preserves its intent. Installed files are outputs;
edit their source repository, never an installation cache.
