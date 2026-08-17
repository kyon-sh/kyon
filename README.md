# Kyon

Kyon is a terminal: a GPU-rendered, block-structured shell client with a built-in
editor, code search, SSH-native remote work, and AI assistance that runs against
your own keys and your own servers.

It is a fork of [Warp](https://github.com/warpdotdev/warp) that answers to nobody
but you. No account, no telemetry, no server round-trip to start a shell. The
remote half is a single fork-owned daemon (`orb`) that you reach over your own
SSH connections.

## Downloads

Every release on this repository carries:

| Artifact | Platform |
|---|---|
| `Kyon-*.dmg` | macOS (Apple Silicon), signed and notarized |
| `kyon_*.deb`, `kyon-*.rpm`, `Kyon-*.AppImage` | Linux x86_64 |
| `Kyon-*-setup.exe` | Windows x64 / arm64 |
| `kyon-web-*.tar.gz` | the browser client, served by `serve-wasm` |
| `kyon-src-*.tar.gz` | complete source for that build |

## Source

Kyon is licensed under the **GNU Affero General Public License v3.0**. The
`kyon-src-*.tar.gz` beside each release is the corresponding source for exactly
that build — everything needed to rebuild it, including the assets. It is
attached to every release, so the source travels with the binary rather than
depending on continued access to a repository.

## Issues

This is where to report them. Bugs, feature requests and questions all belong in
[Issues](../../issues); the templates ask for the version from `Settings → About`
and, for bugs, the steps to reproduce.

Security problems go through a [private advisory](../../security/advisories/new)
instead — please do not open a public issue for one.

## Development

Day-to-day development happens in a separate repository. Releases here are cut
from it, and each carries the full source of what it built.
