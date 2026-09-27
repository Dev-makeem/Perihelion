# Maintainer notes — Dev-makeem

## #760 — deny.toml licence/bans/sources policy

Already resolved on `main`. `deny.toml` at the repo root now includes
`[licenses]` (a permissive-licence allowlist covering MIT, Apache-2.0,
BSD-2/3-Clause, ISC, Unicode-3.0, Unlicense, Zlib, plus the LLVM
exception), `[bans]` (`multiple-versions = "warn"`, `wildcards = "deny"`),
and `[sources]` (`unknown-registry = "deny"`, `unknown-git = "deny"`), in
addition to the `[advisories]` section the issue reported as the only one
present. No further change was needed for this issue.
