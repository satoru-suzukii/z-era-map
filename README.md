# 🧟 Z-Day: Infinite Survival Map Engine

**Made by Satoru Suzuki**

A high-performance, single-file procedural world engine designed for the ultimate zombie apocalypse and urban scavenger survival experience. This engine simulates an infinite decaying world where every tile represents a 1x1 km area, governed by complex urbanization and bio-hazard noise layers.

This tool provides a foundation for building infinite scavenger-exploration games without the overhead of heavy game engines.

---

## ☣️ The Apocalypse Logic

Z-Day uses Triple-Layer Noise Abstraction to determine the environment based on coordinates:

1. Urbanization (e): Determines the physical landscape, from toxic oceanic abysses to high-rise city grids and mountain peaks.
2. Overgrowth (s): A vegetation-equivalent layer that dictates how much nature has reclaimed the concrete—from barren wasteland to deep overgrown forests.
3. Infection Density (c): Represents the biological threat. Low c values indicate Sanitized Strongholds or Green Zones, while high c values create lethal "Dead Zones" overflowing with hordes.

---

## ✨ Key Features 

* 🗺️ Infinite Urban Exploration: Uses Fractal Brownian Motion (FBM) with 4 octaves to ensure natural, continuous terrain across infinite coordinates.
* 🏚️ Scavenger's Discovery System: Intelligent spawning that distinguishes between Functional (Safe) and Ruined (Hazardous) locations based on local infection data.
* 🏗️ Dynamic Industrial Zones: Spawns functional ammo plants or abandoned toxic factories depending on the surrounding chaos.
* 📜 The Scavenger's Log: A built-in coordinate-based ledger that allows survivors to "tag" locations with notes on loot caches, horde movements, or water sources.
* 💾 Persistent Save System: Integrated localStorage support. Your location (X, Y), world seed, and all scavenger logs are automatically saved and reloaded.
* 📋 Centralized Log Reviewer: View every discovery you have ever made in the infinite world in one chronological list, making navigation back to safe zones easy.
* 💯 Zero-Dependency Architecture: A "Digital Talisman"—one single HTML file containing all Logic (JS), Styling (CSS), and Structure (HTML).

---

## 🎮 Controls

* Navigation: Use WASD or Arrow Keys to move your position through the wasteland.
* 🔦 Scout (Flashlight): Click your current tile to read detailed radiation/infection data and leave a note in the Scavenger's Log.
* ⚙️ System Menu: Access the settings to save progress, view logs, or jump to new coordinates.
* ☢️ Wasteland Trek: A "Void Drift" protocol that allows you to jump thousands of kilometers to a new random coordinate.
* ☠️ New Life: Permanently wipe current progress and generate a completely new world seed.

---

## 🗺️ Post-Apocalyptic Biome Reference

| Icon | Name                | Description                                |
| :--- | :---                | :---                                       |
| 🏙️   | Fortified City      | Human bastion; functional walls and power. |
| 🌆   | Ruined Metropolis   | Collapsed skyscrapers; high loot/danger.   |
| 🏠   | Farming Village     | Small survivor community with food.        |
| 🏚️   | Burnt Village       | Looted and abandoned residential ruins.     |
| ⛺   | Survivor Camp       | Common clusters of temporary tents/traders.|
| 🏭   | Industrial Zone     | Can be a functional plant or toxic ruin.   |
| 🌳   | Deep Forest         | Dense trees used for cover/wood.           |
| ⛰️   | Mountain Range      | Difficult terrain; low infection.          |
| 🗻   | High Peak           | Pure summits; air is thin and safe.        |
| 💀   | THE DEAD ZONE       | Maximum infection; constant horde presence. |
| ☠️   | Biohazard Zone      | Extreme radiation and mutated threats.      |
| 🌊   | Toxic Ocean         | Black, undrinkable sludge.                 |

---

## 🚀 Deployment

1. Save the code as `zday-map.html`.
2. Open it in any modern web browser.
3. No server, build-tools, or installation required. 

---

"In the end, it isn't the dead that change the world; it's the ones keep living despite all odds."
