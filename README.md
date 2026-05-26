# LED Museum Kiosk — Installer Releases

This repository is a **release host** for the Windows installer of the LED Museum kiosk
display — the Electron shell that drives a chained-panel LED video wall with a live
news-headline ticker for a museum art installation.

Source code is **not** in this repo. It lives on gitcode:
**https://gitcode.com/bobjohansson/led-project**

## Download

Grab the latest installer from the [Releases](../../releases) page:

- `led-project-ticker-<version>-setup.exe` — Windows x64 NSIS installer
- `led-project-ticker-<version>-setup.exe.blockmap` — auto-updater delta data
  (not needed for a fresh install)

The installer creates Start Menu and Desktop shortcuts and supports per-user installs.

## What it does

The kiosk shell:

- Connects to the LED Project VPS over HTTP + SSE
- Renders a scrolling, all-caps ticker designed for chained LED panels
- Runs in true fullscreen kiosk mode for the museum display PC
- Includes a sidebar for live settings, category/topic filters, and an offline archive
  viewer with JSON/CSV export
- Caches recent headlines so the ticker survives short VPS outages

Hardware-wise it expects a Windows machine driving an LED sending card via HDMI/DP,
which then daisy-chains panels over Cat6. The PC sees this as a single monitor; no
driver work is needed on the kiosk side.

## Releases

- **v0.0.1** (2026-05-26) — first installer. Ticker, archive, categories, topic
  filter, LLM-classified topics, all-caps mode, SSE drop recovery.

## Maintainer

Oskar Johansson · Jade Circuit · oskar@jadecircuit.com
