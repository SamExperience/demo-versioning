# demo-versioning

Practice repository for learning release versioning with **Git Flow** and **GitHub Actions**.

## Branching

- `main`: production-ready code, every release is tagged here
- `develop`: integration branch
- `feat/*`: feature branches, opened from `develop` and merged back via PR

## Releases

1. Merge `develop` into `main` via PR (normal merge, full history kept).
2. Tag manually with semantic versioning: `git tag vX.Y.Z && git push origin vX.Y.Z`.
3. The [release workflow](.github/workflows/release.yml) validates the tag (format, on `main`, greater than the previous one) and publishes a GitHub Release with auto-generated notes.

Release notes are grouped by PR labels, see [release.yml](.github/release.yml).

## Changelog

See the [Releases](../../releases) page for the full list of changes per version.
