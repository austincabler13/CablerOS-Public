# Versioning Policy

CablerOS uses semantic-style versions:

`MAJOR.MINOR.PATCH[-PRERELEASE]`

- `MAJOR`: incompatible stable platform or ABI generation
- `MINOR`: a completed capability milestone or compatible feature set
- `PATCH`: compatible fixes and narrowly scoped improvements
- `PRERELEASE`: development maturity such as `dev.0`, `alpha.1`, or `rc.1`

Before `1.0.0`, interfaces may change. Such changes still require documentation
and migration notes; version zero is not permission for untracked breakage.

## Initial version

The repository begins at `0.0.1-dev.0`. The first bootable diagnostic image
will advance the project to `0.1.0-alpha.1` after its milestone tests pass.

Versions describe verified capability, not aspiration. A version is never
advanced solely because time passed or a feature was started.

