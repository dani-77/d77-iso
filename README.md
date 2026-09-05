# Custom Arch Linux Repository

A curated personal repository providing pre-built packages and configurations for Arch Linux and its derivatives.

The primary highlight of this repository is a tailored **Qtile** desktop environment bundled as a skeleton configuration (`skel`), providing an out-of-the-box, opinionated workflow alongside essential companion utilities.

---

## Included Packages

* **`custom-qtile-skel`** — Default user profile, keybindings, bar widgets, and companion scripts defining my custom Qtile setup.
* *Additional utility packages and patched tools as needed.*

---

## Quick Setup

### 1. Add the Repository
Append the following configuration block to your `/etc/pacman.conf`:

```ini
[custom]
SigLevel = Optional TrustAll
Server = https://raw.githubusercontent.com/dani-77/d77-iso/main
