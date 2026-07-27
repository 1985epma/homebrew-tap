# 1985epma/homebrew-tap

Homebrew tap for [1985epma](https://github.com/1985epma) projects.

## Usage

```bash
brew tap 1985epma/tap
brew trust 1985epma/tap
brew install epma-windows-usb-creator
```

`brew trust` is required by Homebrew for any third-party tap. It is a one-time
confirmation that you accept formulae from this tap.

## Formulae

### `epma-windows-usb-creator`

Create a bootable Windows 11 USB drive from macOS or Linux.

A graphical application that downloads the official Windows 11 ISO and writes a
UEFI-bootable USB drive (GPT + FAT32), automatically splitting `install.wim`
when it exceeds the FAT32 4 GB single-file limit.

- Source: <https://github.com/1985epma/epma-windows-usb-creator>
- License: GPL-3.0-or-later

> **This tool erases the selected disk completely.** It only lists external
> removable drives, hides any disk holding a critical system mountpoint,
> requires you to type the disk identifier by hand, and re-verifies the target
> immediately before writing. Double-check the selected disk before confirming.

## Updating a formula after a new release

From the project repository:

```bash
./Formula/update-formula.sh v1.2.3
```

Then copy the updated formula here and validate:

```bash
brew style 1985epma/tap
brew audit --strict --online 1985epma/tap/epma-windows-usb-creator
```
