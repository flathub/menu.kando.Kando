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

## Building the Flatpak Package Locally

If you want to build and install the same Flatpak package as is currently on Flathub locally (aka the latest stable release of Kando), you can do so by running the following commands:

```bash
git clone https://github.com/flathub/menu.kando.Kando.git
cd menu.kando.Kando
flatpak-builder --force-clean --sandbox --user --install-deps-from=flathub --repo=repo --install builddir menu.kando.Kando.yml
```

## Creating a Development Package

If you are a developer and want to test the latest changes in Kando in a Flatpak environment, you can use the `tools/make-flatpak-bundle.sh` script in Kando's repository to create a development bundle.

```bash
cd kando
npm run package
./tools/make-app-image.sh
./tools/make-flatpak-bundle.sh
flatpak install out/make/flatpak/*.flatpak
```
