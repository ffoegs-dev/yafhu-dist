# Yet Another FITS Header Updater (yafhu)

yafhu edits the headers of astrophotography image files - FITS and XISF
- one file at a time or a whole session at once: change, add and delete
keywords, fix timestamps across hundreds of files with expressions, and
apply the changes safely, with backups and a way back. It never changes
the image data itself.

This repository holds yafhu's **downloads**: each version is a
[Release](../../releases), with what's new in it. (Its source is kept
privately.)

## Download

Open the [latest release](../../releases/latest) and download the file
for your computer:

| Your computer | File |
|---|---|
| **Windows** 10 or 11, 64-bit | `yafhu-<version>-windows-x86_64.zip` |
| **Linux**, 64-bit PC, from 2022 or later | `yafhu-<version>-linux-x86_64.tar.gz` |
| **macOS** 13 or later, Apple Silicon (M1 or later) | `yafhu-<version>-macos-arm64.zip` |

There's nothing to install: unpack it and run yafhu from the `yafhu`
folder it makes. Keep the folder's contents together. To check the
download, compare its checksum with the release's `SHA256SUMS`
(`sha256sum -c SHA256SUMS --ignore-missing` on Linux; `Get-FileHash` in
PowerShell on Windows).

- **Windows**: right-click the `.zip`, **Extract All**, then run
  `yafhu.exe`. Windows may say it "protected your PC" from an
  unrecognized app the first time: click **More info**, then **Run
  anyway**. The first start can take a little longer while your
  antivirus checks the new files.
- **Linux**: `tar -xzf yafhu-<version>-linux-x86_64.tar.gz`, then run
  `yafhu` in the unpacked folder. To add it to your applications menu,
  with its icon, run `./install-desktop-entry.sh` there: it asks which
  menu section (Science, Graphics, Education, Utility or Other), and
  `--desktop` adds a desktop icon too. Supported: Ubuntu 22.04 and later (Linux
  Mint 21 and later, Pop!_OS, Zorin OS, elementary OS), Debian 12 and
  later, Fedora 36 and later, RHEL/Rocky/AlmaLinux 10, Arch, Manjaro,
  openSUSE Tumbleweed.
- **macOS**: unzip it and move `yafhu.app` to Applications. The first
  time, macOS won't open it because it isn't from an identified
  developer: open **System Settings → Privacy & Security** and click
  **Open Anyway** beside the message about yafhu.

The first time it starts, yafhu asks you to accept its license
agreement, then offers a short guided tour. Its user guide is in the app,
under the **(i)** icon → **Documentation...**

## Updates

To see whether a newer version is out, choose **Check for Updates...**
under the **(i)** icon: it asks this repository and shows what's new. On
Windows and Linux, **Download and Install** installs it for you - it
checks the download against the release's `SHA256SUMS`, restarts yafhu
into the new version in the same folder, and keeps your previous version
beside it (as `yafhu.previous`) until the next update. Or open the
download page and download and unpack the new version as above - into a new place, not over your current `yafhu` folder (files
from two versions mixed together could misbehave); then delete the old
folder, and move the new one where the old one was if you like. You can also have yafhu check at each start (Preferences →
Updates) - it's off unless you turn it on, and otherwise yafhu never
goes online by itself.

## What's new

Each [release](../../releases) lists its changes; in the app, **(i)** →
**What's New...** lists them all.

## License

yafhu is free to use, for any purpose, and you may share complete,
unmodified copies. It's proprietary software, © 2026 Geoff Shapiro; the
`LICENSE` file in each download states the terms. yafhu includes other
software - among it Python, Qt and PySide6, numpy and astropy - under
their own licenses, listed in `license.txt`.

## Support

Questions and problem reports: the Discord link in yafhu's **About**
dialog (under the **(i)** icon).
