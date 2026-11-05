# BShield releases

Signed and notarized builds of BShield for macOS and of the bshield CLI,
and the feeds they update themselves from. Binaries only; the source is
private.

Each product has its own channels, so nothing here depends on GitHub's
"latest release":

## BShield for macOS

- `v<version>`: one build. `BShield-<version>-<arch>.dmg` and its
  `.sha256` are the download; `BShield-<version>-<arch>.zip` is what an
  installed BShield downloads to update itself; `browter-feed-<arch>.json`
  is that build's update feed.
- `beta-channel`: the feed beta installs read, rewritten by every publish.
- `stable-channel`: the feed stable installs read, rewritten when a build
  is promoted (`scripts/promote-release.sh` in bshield-desktop).

## bshield CLI

- `cli-v<version>`: one release. `bshield-<version>-<os>-<arch>.tar.gz`
  for darwin and linux, arm64 and x64, with the signed `manifest.json`,
  `keys.json`, `checksums.txt` and `install.sh`.
- `cli-beta-channel`: the manifest and installer beta installs read,
  rewritten by every publish.
- `cli-stable-channel`: the same for stable installs, rewritten when a
  release is promoted.

Install the CLI with:

```sh
curl -fsSL https://github.com/bkeyID/bshield-releases/releases/download/cli-beta-channel/install.sh | sh
```
