# OSA Code releases

Builds of **OSA Code**, the macOS desktop app that runs the coding agents you already pay for (Claude Agent, Codex, Gemini, ACP agents) and local models in one place, with a continuity ledger that moves a thread between them. Apple silicon, macOS 14 or newer.

## Install

1. Download the `.dmg` from the [latest release](https://github.com/devartin/osa-code-releases/releases/latest) and drag **OSA Code** to Applications.
2. The build is unsigned (no Developer ID yet). On first launch macOS says it cannot verify the developer: on macOS 15 and newer click **Done**, open **System Settings → Privacy & Security**, scroll to the line about OSA Code and click **Open Anyway**; on macOS 14 right-click the app → **Open** → **Open**.

## Updates

From 0.3.0 the app updates itself from this repository: it checks `latest-mac.yml` on launch and every six hours, downloads the zip in the background, verifies its checksum, and installs it on the next restart or quit. Settings → About shows where things stand and has the switch.

Each release carries exactly the files electron-builder lists in `latest-mac.yml`: the `.dmg` for a first install and the `-mac.zip` the updater uses.
