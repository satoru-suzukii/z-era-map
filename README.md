# 🧟 Z-Era: Infinite Survival Map Engine

**Made by Satoru Suzuki**

A high-performance, single-file procedural world engine designed for the ultimate zombie apocalypse and urban scavenger survival experience. This engine simulates an infinite decaying world where every tile represents a **1x1 km area**, governed by complex urbanization and bio-hazard noise layers.

This tool provides a foundation for building infinite scavenger-exploration games without the overhead of heavy game engines.

---

## ☣️ The Apocalypse Logic

Z-Era uses **Triple-Layer Noise Abstraction** to determine the environment based on coordinates:

1.  **Urbanization ($e$):** Determines the physical landscape, from toxic oceanic abysses to high-rise city grids and jagged mountain peaks.
2.  **Overgrowth ($s$):** A vegetation-equivalent layer that dictates how much nature has reclaimed the concrete—from barren wasteland to deep overgrown forests.
3.  **Infection Density ($c$):** Represents the biological threat. Low $c$ values indicate **Sanitized Strongholds** or **Green Zones**, while high $c$ values create lethal "Dead Zones" overflowing with hordes.

---

## ✨ Key Features 

* **🌐 Infinite Precedual Exploration:** Uses **Fractal Brownian Motion (FBM)** with 4 octaves to ensure natural, continuous terrain across infinite coordinates.
* **🏚️ Infection Sync Settlements:** Intelligent spawning that distinguishes between **Functional (Safe)** and **Ruined (Hazardous)** locations based on local infection data.
* **🏗️ Dynamic Industrial Zones:** Spawns functional **Ammo Plants** or abandoned **Toxic Factories** depending on the surrounding biological chaos.
* **📜 The Scavenger's Log:** A built-in coordinate-based ledger that allows survivors to "tag" locations with notes on loot caches, horde movements, or water sources.
* **💾 Persistent Save System:** Integrated `localStorage` support. Your coordinates ($X, Y$), current world seed, and all scavenger logs are automatically saved and reloaded.
* **📋 Centralized Log Reviewer:** A new centralized log interface allows you to view all notes made across the infinite map in one chronological list, making navigation back to safe zones easy.
* **🔑 Custom Seed Injection:** Players can now manually input and **"Load"** specific world seeds, allowing for shared world exploration and speed-running.
* **⚙️ Unified System Menu:** A clean modal-based UI replaces the old action bar, housing world-reset, trekking, and log-management tools.
* **💯 Zero-Dependency Architecture:** One single HTML file containing all Logic (JS), Styling (CSS), and Structure (HTML).

---

## 🎮 Controls

* **Navigation:** Use `WASD` or `Arrow Keys` to move your position through the wasteland.
* **🔦 Scout (Flashlight):** Click your current tile to read detailed radiation/infection data and leave a note in the **Scavenger's Log**.
* **⚙️ System Menu:** Access the settings icon to save your progress, jump to new coordinates, or view your logs.
* **☢️ Wasteland Trek:** A "Void Drift" protocol that allows you to jump thousands of kilometers to a new random coordinate.
* **☠️ New Life:** Permanently wipe current progress and generate a completely new world seed.

---

## 🗺️ Post-Apocalyptic Biome Reference

| Icon | Name | Description | Logic Condition |
| :--- | :--- | :--- | :--- |
| 🏙️ | **Fortified City** | Human bastion; functional walls. | High Urban ($e$) + Low Infection ($c$) |
| 🌆 | **Ruined Metropolis** | Collapsed skyscrapers; high loot. | High Urban ($e$) + High Infection ($c$) |
| 🏠 | **Farming Village** | Small community with food. | Mid Urban + High Overgrowth ($s$) |
| 🏚️ | **Burnt Village** | Looted and abandoned ruins. | Frequent Spawn ($c > 0.5$) |
| 🏭 | **Industrial Zone** | Functional plant or toxic ruin. | Mid Urban + Low Overgrowth ($s$) |
| 🌳 | **Deep Forest** | Dense trees for cover/wood. | High Overgrowth ($s$) + Low Urban ($e$) |
| 💀 | **The Dead Zone** | Maximum infection; constant hordes. | Maximum Infection ($c > 0.92$) |
| 🌊 | **Toxic Ocean** | Black, undrinkable sludge. | Minimum Elevation ($e < 0.22$) |

---

## 🚀 Deployment

1.  Save the code as `z-era-map.html`.
2.  Open it in any modern web browser.
3.  No server, build-tools, or installation required. 

---

> "In the end, it isn't the dead that change the world; it's the ones who keep living despite all odds."
