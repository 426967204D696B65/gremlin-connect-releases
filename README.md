# Gremlin Connect — Releases

Signed release downloads for **Gremlin Connect**, a desktop app for setting up and
using a **WireGuard VPN on Ubuntu** without touching the terminal — by **NeuralFury.AI**.

> Powered by **NF · NEURALFURY.AI**

## What is Gremlin Connect?

WireGuard is a fast, modern VPN, but configuring it normally means editing
`.conf` files and running command-line tools as root. Gremlin Connect is a native
GTK4 app that makes it point-and-click: create tunnels, generate or paste keys,
choose what traffic to route, connect/disconnect with live status, import `.conf`
files, export tunnels to your phone as a QR code, use a kill switch and
auto-connect, and a system-tray icon — with built-in plain-language help. It
targets Ubuntu 24.04 / 26.04 LTS.

The application source is maintained privately. **This repository hosts only the
signed `.deb` release artifacts**, so the app can be installed and can securely
update itself with no credentials required.

## Install the latest release

1. Download `gremlin-connect_<version>_all.deb` from the
   [Releases](../../releases) page.
2. Install it (apt resolves the dependencies — GTK4, libadwaita, WireGuard, etc.):
   ```sh
   sudo apt install ./gremlin-connect_<version>_all.deb
   ```
3. Launch **Gremlin Connect** from your app grid.

## Integrity

Every release `.deb` is signed with NeuralFury's **Ed25519** release key, and each
release includes the matching `.deb.sig`. Gremlin Connect's in-app updater
downloads from this repository over HTTPS and verifies the signature against a
public key embedded in the app **before** installing — so receiving updates never
requires a token or any private access.

## Links

- NeuralFury.AI — https://neuralfury.ai

---

© 2026 NeuralFury.AI · MIT License.
