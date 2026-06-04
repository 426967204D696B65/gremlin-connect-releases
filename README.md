# Gremlin Connect — Releases

Signed release downloads for **Gremlin Connect**, a desktop app for setting up and
using a **WireGuard VPN on Ubuntu** without touching the terminal — by **NeuralFury.AI**.

> Powered by **NF · NEURALFURY.AI**

## What is Gremlin Connect?

WireGuard is a fast, modern VPN, but configuring it normally means editing `.conf`
files and running command-line tools as root. Gremlin Connect is a native GTK4 app
that makes it point-and-click: create tunnels, generate or paste keys, choose what
traffic to route, connect/disconnect with live status, import/export `.conf` files,
show a QR code for your phone, use a kill switch and auto-connect, with a system-tray
icon and built-in help. Targets Ubuntu 24.04 / 26.04 LTS.

The application source is maintained privately. **This repository hosts only the
signed `.deb` release artifacts.**

---

## How to install

> **A `.deb` is a package you _install_ — not a program you run.** Double-clicking it
> or making it executable (`chmod +x`) will **not** launch it. You install it with a
> package manager, which unpacks the app, pulls in its dependencies, and adds it to
> your applications menu.

### Easiest — one terminal command (recommended)

1. Download `gremlin-connect_<version>_all.deb` from the
   [**Releases**](../../releases) page.
2. Install it (this automatically resolves GTK4, WireGuard, polkit and the other
   dependencies):

   ```sh
   sudo apt install ~/Downloads/gremlin-connect_<version>_all.deb
   ```

   The `~/Downloads/...` path (or a leading `./`) is required — it tells `apt` to
   install a **local file** rather than search the online repositories.
3. Launch **Gremlin Connect** from the apps menu (Activities → search "Gremlin"),
   or run `gremlin-connect`.

### No terminal? Use the GDebi graphical installer

On Ubuntu 24.04 the Files app no longer installs `.deb`s when you double-click them.
Install GDebi once:

```sh
sudo apt install gdebi
```

Then right-click the downloaded `.deb` → **Open With → GDebi Package Installer** →
**Install**. GDebi shows a graphical installer and resolves dependencies for you.

### Troubleshooting

- **"It won't run / nothing happens when I double-click it."** That's expected — a
  `.deb` is installed, not executed. Use one of the methods above.
- **`dpkg` dependency errors.** If you ran `sudo dpkg -i file.deb` and got unmet
  dependency errors, run `sudo apt --fix-broken install`. (Using
  `sudo apt install ./file.deb` avoids this — it resolves dependencies in one step.)
- **`Download is performed unsandboxed as root … _apt` notice.** Harmless; the
  package still installs. It appears when the file is in your home directory. To
  avoid it, install from `/tmp` (`cp` the file there first).

### Remove

```sh
sudo apt remove gremlin-connect
```

Requires Ubuntu 24.04+ (GTK 4.12+, libadwaita 1.5+). WireGuard is installed as a
dependency.

---

## Integrity

Every release `.deb` is signed with NeuralFury's **Ed25519** release key, and each
release includes the matching `.deb.sig`. Gremlin Connect's in-app updater downloads
from this repository over HTTPS and verifies the signature against a public key
embedded in the app **before** installing — so receiving updates never requires a
token or any private access.

## Links

- NeuralFury.AI — https://neuralfury.ai

---

© 2026 NeuralFury.AI · MIT License.
