# Modrinth App with offline accounts

Unofficial patched builds of the [Modrinth App](https://github.com/modrinth/code).

- `patches/` holds the changes, applied on top of upstream's release tags.
- `.github/workflows/release.yml` checks for a new upstream app release every 6 hours,
  applies the patches to that exact tag, builds Windows / Linux (deb + AppImage) / macOS
  and publishes a release named `<upstream tag>-offline`.
- Nothing is built from upstream's `main`.

Run the workflow manually (Actions -> Release patched Modrinth App -> Run workflow) to
build a specific upstream tag, or set `revision` to republish the same version.
