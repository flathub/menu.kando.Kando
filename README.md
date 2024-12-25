# 📦 Flatpak Packaging for Kando

[🌸 Kando](https://kando.menu/) offers an unconventional, fast, highly efficient, and fun way of interacting with your computer!
You can use it to launch applications, simulate keyboard shortcuts, open files, and much more.
It runs on Windows, macOS, and Linux.

This repository contains the necessary files to build a Flatpak package for Kando.

## Installation from Flathub

To install the Flatpak package from Flathub, just run the following command:

```bash
flatpak install flathub menu.kando.Kando
```

## Building the Flatpak Package

If you want to build and install the Flatpak package yourself, you can do so by running the following command:

```bash
flatpak-builder --force-clean --sandbox --user --install-deps-from=flathub --repo=repo --install builddir menu.kando.Kando.yml
```
