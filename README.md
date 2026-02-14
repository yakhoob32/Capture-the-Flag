# Capture-the-Flag (CTF)

# Elite Flag Conquest: Super Stratego Elite 🚩🛡️

An advanced, tactical 2D turn-based strategy game built with **Python**. This project evolves from a CLI-based logic core to a full-fledged networked graphical game. Inspired by the classic Stratego but enhanced with modern "Fog of War" and "Stealth" mechanics.

---

## 🚀 Project Vision: Two-Phase Development

To ensure a robust and bug-free game, the development is divided into two major milestones:

### 🔹 Phase 1: Logic Core (CLI MVP)
* **Focus**: Game Mechanics, Rules, and Win Conditions.
* **Interface**: Terminal-based ASCII grid.
* **Networking**: Local turn-based (single machine).
* **Goal**: Stabilize the battle engine, movement constraints, and "Hidden Information" logic.

### 🔹 Phase 2: The Elite Experience (GUI & Network)
* **Interface**: Full 2D Graphics using **Pygame**.
* **Networking**: **Client-Server** architecture using Python Sockets.
* **Visuals**: Sprites, animations for combat, and Fog of War overlays.
* **Scaling**: Transition from a test grid (6x6) to the full Elite Board (12x12).

---

## 🕹️ Unique Elite Features

### 🌫️ The "Storm Cloud" Mechanic (8x8)
Every 6 to 8 turns, a massive **8x8 Fog Cloud** appears randomly on the board. 
* **Stealth**: All units inside the cloud (including yours) become invisible to the opponent.
* **Tactics**: Use this window to relocate your Flag or reposition your heavy hitters without being tracked.

### 🌑 Blind Combat & Stealth
* **True Fog of War**: Enemy ranks are never revealed. 
* **Post-Battle Silence**: If a battle occurs, the only information given is "Your piece was defeated" or "You won." No ranks are disclosed, forcing players to deduce strength based on movement patterns.
* **Obstacles (Rock/Islands)**: Units behind obstacles are hidden from view unless an enemy unit has a direct line of sight.

### ⏳ Tactical Pressure
* **Turn Timer**: Players have a limited window to make a move, preventing "Analysis Paralysis."
* **Power Tokens**: Limited-use abilities like *Radar* (reveal small area) or *Reinforce* (revive a unit).

---

## 📊 Unit Hierarchy (The Army)

| Rank | Identity | Ability |
|:---:|:---:|:---|
| **10** | Marshal | Supreme strength; can be killed only by Spy or Bomb. |
| **3** | Miner | The only unit that can defuse Bombs without dying. |
| **2** | Scout | Can move any distance in a straight line. |
| **S** | Spy | Weakest unit, but the only one who can defeat the Marshal. |
| **B** | Bomb | Immovable; destroys any attacker (except Miner). |
| **F** | Flag | The ultimate goal. Capture this to win. |

---

## 🛠️ Tech Stack & Architecture

* **Language**: Python 3.x
* **Graphics**: Pygame (Phase 2)
* **Network**: Socket / Threading (Phase 2)
* **Design Pattern**: Object-Oriented Programming (OOP)
    * `Piece`: Handles rank, team, and visibility.
    * `Board`: Manages the grid, collisions, and Fog of War.
    * `GameEngine`: Orchestrates turns, combat, and win conditions.

---

## 🗺️ Roadmap
- [ ] Phase 1: Basic Board & Movement Logic.
- [ ] Phase 1: Blind Combat & Win Conditions.
- [ ] Phase 1: CLI "Cloud" implementation.
- [ ] Phase 2: Pygame GUI Integration.
- [ ] Phase 2: Socket-based Server/Client communication.
- [ ] Phase 2: Matchmaking & Lobby system.

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
