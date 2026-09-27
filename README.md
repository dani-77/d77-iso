<p align="center">
  <img src="assets/logo.png?v=2" width="128" alt="d77-iso logo">
</p>

<h1 align="center">d77-iso</h1>

<p align="center">
  Custom Arch Linux package repository -- the [custom] repo behind d77arch.
</p>

---

## Overview

A curated personal repository providing pre-built packages and configurations for Arch Linux and its derivatives.

The primary highlight of this repository is a tailored **Qtile** desktop environment bundled as a skeleton configuration (`skel`), providing an out-of-the-box, opinionated workflow alongside essential companion utilities.

<p align="center">
  <img src="d77arch.png" alt="d77_qtile desktop">
</p>

<hr>

## Included Packages

* **`d77-qtile-skel`** — Default user profile, keybindings, bar widgets, and companion scripts defining my custom Qtile setup.
* **`qtile-extras`** — Extra Qtile widgets/layouts used by the skel.
* **`arc-gtk-theme`** / **`arc-solid-gtk-theme`** — GTK theming to match.
* *Additional utility packages and patched tools as needed.*

### d77 desktop components

Pre-built from the PKGBUILDs in [dani-77/aur](https://github.com/dani-77/aur)
(also published on the AUR):

* **`d77run`** — Minimal GTK4 run-dialog launcher.
* **`fabric-d77`** — GTK desktop shell for Wayland compositors, built on Fabric.
* **`quickshell-d77`** / **`qsd77`** — Quickshell desktop shell and its control helper.
* **`utumno`** — Minimal Quickshell desktop shell.
* **`wasp-d77`** — dwl-based Wayland compositor (pulls in **`scenefx0.5`**, shipped here too).
* **`pwm-d77`** — Penrose-based X11 tiling window manager.

AUR-only dependencies of the above are shipped here too, so everything
resolves from `[custom]` plus the official repos: **`python-fabric-git`**,
**`python-thefuzz`** (for `fabric-d77`) and **`st`** (for `pwm-d77`).

<hr>

## Quick Setup

### 1. Add the Repository
Append the following configuration block to your `/etc/pacman.conf`:

```ini
[custom]
SigLevel = Optional TrustAll
Server = https://raw.githubusercontent.com/dani-77/d77-iso/main
```

### 2. Sync and Install

```
pacman -Sy
pacman -S d77-qtile-skel
```
