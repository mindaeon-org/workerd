# Upstream

This repository is the Mindaeon-owned fork of [cloudflare/workerd](https://github.com/cloudflare/workerd) (Apache-2.0).
The runtime of platform apps (docs/05, app runtime; task R5.2). Tracked at a release tag: the project has no release branches, so the line is its major version.

| | |
|---|---|
| Tracked line | `1` |
| Last merged tag | `v1.20261002.1` |
| Last merged commit | `51a48a5bb7863fbeab791358bee8dff22c3ce83f` (2026-10-02) |
| Recorded | 2026-10-03 |

## Branches

| Branch | Content |
|---|---|
| `upstream/1` | An exact mirror of the upstream tag above. Never committed to by hand |
| `mindaeon/1` | `upstream/1` plus the patches listed in [PATCHES.md](PATCHES.md). The branch that is built from |

Builds are tagged `<upstream version>-m.<n>`. Our changes live in new files, or in an upstream file between
`mindaeon_change start` and `mindaeon_change end` comments that give the reason.

## Taking a new upstream version

1. Fetch the upstream tag and fast-forward `upstream/1` to it.
2. Merge `upstream/1` into `mindaeon/1`; resolve patch by patch and drop a patch upstream now covers.
3. Run the licence check, the provenance gate, the security scan and the tests.
4. Update the table above and [PATCHES.md](PATCHES.md).
