# GeForceNow-App-for-non-SteamOS-distros
This repository contains a small modification in the code of the GeForceNow installation script for SteamOS that now (in theory) allows the installation of the APP on any Linux distribution.

## Notes
- This is an **unofficial modification** of a script provided by NVIDIA.
- The original script was designed solely for SteamOS use and required adaptation to work under other environments.

This project includes code licensed under the MIT License by NVIDIA CORPORATION & AFFILIATES.
See the LICENSE file for details.

> ✅ Intended for users of general-purpose Linux distros who want to install the GeForce NOW app **without relying on SteamOS or Steam Deck-specific tooling.**

---

## 🚀 Features

- Bypasses `steamos-add-to-steam`, replacing it with generic launch mechanisms.
- Adds system compatibility checks for non-SteamOS environments.
- Attempts automatic installation of Google Chrome (Flatpak) if not found.
- Designed for Flatpak-based setups (respects `com.google.Chrome` runtime).
- Clean logging of events and errors for debugging and diagnostics.

---

## ⚠️ Important Notes

- This script does **not** guarantee full compatibility or performance parity with SteamOS.
- Chrome must be available as a Flatpak (`com.google.Chrome`). Native or Snap versions are **not supported**.
- On some distros, installing Flatpaks might require **user input** (e.g. choosing between system/user install). This script currently does **not** automate that interaction for those distros.
- The app is still **dependent on NVIDIA’s streaming infrastructure and Chrome’s DRM**. A working GPU driver and up-to-date browser runtime are essential.

---

## ✅ Requirements

- Linux distro with:
  - `flatpak` and Flathub configured
  - `python3` and standard libraries (`os`, `shutil`, `platform`, `logging`)
  - Access to a terminal or TTY for script execution
- A **valid NVIDIA account** with access to GeForce NOW
- Steam (Required if you plan to integrate with it manually)

---

## 📦 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Ziednaga/GeForceNow-App-for-non-SteamOS-distros.git
   cd GeForceNow-App-for-non-SteamOS-distros/GeForceNOWNonSteamOS_Setup/
   chmod +x GeForceNOW_Setup
   ./GeForceNOW_Setup
