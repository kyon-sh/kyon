# Kyon2

Builds of Kyon2 for macOS, Windows and Linux. Kyon2 installs beside an
existing Kyon rather than over it.

Every build is published as a **preview** first. A preview that has been
tried becomes a **release** without being rebuilt, so a release is exactly
the preview it was. Each platform below has a channel for releases and one
for previews.

Downloads are under [Releases](https://github.com/kyon-sh/kyon2/releases).

## macOS

macOS 11 or later, Apple silicon or Intel. Signed and notarised.

```sh
brew install --cask kyon-sh/kyon/kyon2            # releases
brew install --cask kyon-sh/kyon/kyon2@preview    # every preview
```

Update with `brew upgrade --cask kyon2` (or `kyon2@preview`). The two
casks install the same application, so only one can be installed at a time.

Without Homebrew, download `Kyon2-<version>.dmg` and drag Kyon2 to
Applications.

## Windows

Windows 10 or later, x64 or Arm64.

Download `Kyon2-<version>-windows-x64.zip` (or `-windows-arm64.zip`),
unzip it wherever you keep programs, and run `Kyon2\kyon.exe`. Nothing is
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
curl -fsSL https://kyon-sh.github.io/kyon2/apt/kyon2.asc \
  | sudo tee /etc/apt/keyrings/kyon2.asc > /dev/null
echo "deb [signed-by=/etc/apt/keyrings/kyon2.asc] https://kyon-sh.github.io/kyon2/apt stable main" \
  | sudo tee /etc/apt/sources.list.d/kyon2.list
sudo apt update && sudo apt install kyon2
```

Use `preview` instead of `stable` for every preview. `sudo apt upgrade`
then keeps Kyon2 current. The repository is signed with the key
`9490 05ED 0839 DF50 05B9  CA06 492B A402 D376 B788`.

Or install one package by hand, without updates:

```sh
sudo apt install ./kyon2_<version>_amd64.deb
```

### Any other distribution

Download `Kyon2-<version>-linux-x86_64.tar.gz` and unpack it:

```sh
tar -xzf Kyon2-<version>-linux-x86_64.tar.gz
./Kyon2/bin/kyon
```

Kyon2 needs a running X11 or Wayland session, with libxkbcommon and
fontconfig installed.

---

Copyright © Ryowave. All rights reserved. This repository hosts binaries
only.
