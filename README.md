# Gremlin Connect — Releases

Public distribution channel for **[Gremlin Connect](https://neuralfury.ai)**, the
friendly WireGuard GUI for Ubuntu — by **NeuralFury.AI**.

> Powered by **NF · NEURALFURY.AI**

The application source code is maintained privately. This repository hosts only
the **signed `.deb` release artifacts**, so the app can be installed and can
securely update itself without any credentials.

## Install

1. Download the latest `gremlin-connect_<version>_all.deb` (and its signature)
   from the [Releases](../../releases) page.
2. Install it (apt resolves the runtime dependencies):
   ```sh
   sudo apt install ./gremlin-connect_<version>_all.deb
   ```
3. Launch **Gremlin Connect** from your app grid.

## Integrity

Each release `.deb` is signed with NeuralFury's **Ed25519** release key. Gremlin
Connect's in-app updater downloads releases from this repository over HTTPS and
verifies the signature against a public key embedded in the app **before**
installing — so receiving updates never requires a token or any private access.

## Links

- NeuralFury.AI — https://neuralfury.ai

---

© 2026 NeuralFury.AI · Distributed under the MIT License.
