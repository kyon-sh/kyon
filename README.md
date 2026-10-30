# Kyon

Builds of Kyon for macOS, Windows and Linux.

Every build is published as a **preview** first. A preview that has been
tried becomes a **release** without being rebuilt, so a release is exactly
the preview it was. Each platform below has a channel for releases and one
for previews.

Downloads are under [Releases](https://github.com/kyon-sh/kyon/releases).

## macOS

macOS 11 or later, Apple silicon or Intel. Signed and notarised.

```sh
brew install --cask kyon-sh/kyon/kyon             # releases
brew install --cask kyon-sh/kyon/kyon@preview     # every preview
```

Update with `brew upgrade --cask kyon` (or `kyon@preview`). The two
casks install the same application, so only one can be installed at a time.

Without Homebrew, download `Kyon-<version>-macos-<arch>.dmg` and drag Kyon to
Applications.

## Windows

Windows 10 or later, x64 or Arm64.

Download `Kyon-<version>-windows-x64.zip` (or `-windows-arm64.zip`),
unzip it wherever you keep programs, and run `Kyon\kyon.exe`. Nothing is
installed elsewhere; to remove it, delete the folder.

These builds are not signed yet, so the first time you run one, Windows
SmartScreen may say it doesn't recognise the program. Choose
**More info › Run anyway**.

To update, unzip a newer download over the old folder.

## Linux

x86_64, with glibc 2.39 or later: Ubuntu 24.04, Debian 13, Fedora 40 or
newer.

### Debian and Ubuntu, with updates through apt

```sh
sudo install -d /etc/apt/keyrings
curl -fsSL https://kyon.sh/kyon/apt/kyon.asc \
  | sudo tee /etc/apt/keyrings/kyon.asc > /dev/null
echo "deb [signed-by=/etc/apt/keyrings/kyon.asc] https://kyon.sh/kyon/apt stable main" \
  | sudo tee /etc/apt/sources.list.d/kyon.list
sudo apt update && sudo apt install kyon
```

Use `preview` instead of `stable` for every preview. `sudo apt upgrade`
then keeps Kyon current. The repository is signed with the key
`9490 05ED 0839 DF50 05B9  CA06 492B A402 D376 B788`.

Or install one package by hand, without updates:

```sh
sudo apt install ./kyon_<version>_amd64.deb
```

### Any other distribution

Download `Kyon-<version>-linux-x86_64.tar.gz` and unpack it:

```sh
tar -xzf Kyon-<version>-linux-x86_64.tar.gz
./Kyon/bin/kyon
```

Kyon needs a running X11 or Wayland session, with libxkbcommon and
fontconfig installed.

---

Copyright © Ryowave. All rights reserved. This repository hosts binaries
only.
