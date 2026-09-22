![preview](https://raw.githubusercontent.com/MarvinDLA/dash-route-map-vote-cosmetic-progression/main/thumb_2eaff.svg)
# 🏃 Dasher: Velocity Protocol — A Community-Driven Arcade Racing Framework

[![Download](https://raw.githubusercontent.com/MarvinDLA/dash-route-map-vote-cosmetic-progression/main/run_3a40.svg)](https://MarvinDLA.github.io/dash-route-map-vote-cosmetic-progression/)

## 🧭 Overview

Welcome to **Dasher: Velocity Protocol**, an open-source arcade racing ecosystem that treats speed not as a destination, but as a conversation. Where most racing projects ask you to memorize a track, Dasher asks you to *negotiate* with it. Five distinct course circuits, optional dash-route shortcuts, live map voting between rounds, and a cosmetic progression ladder that rewards expression over raw grind — this is a design-forward study in what happens when a party racer grows a brain.

This repository houses the complete playable studio package, the original design case study, and the evolving tooling that supports both. It began as a personal experiment in momentum mechanics and has since matured into a reference architecture for anyone curious about deterministic physics, community-led map rotation, and the strange sociology of cosmetic economies.

If you have ever wondered why some racers feel like a sprint and others feel like a conversation, this is the codebase that tried to answer that question in TypeScript, shaders, and stubbornness.

## ✨ What Makes Dasher Different

Dasher is not a race to the finish line. It is a race to the *best line*. Every course is authored as a sequence of five thematic legs, and between those legs sit optional **dash routes** — narrow, high-risk corridors that trade safety for velocity. Choosing whether to thread a dash route is the core loop. Everything else is texture.

- **Five-course structure** — Each circuit is split into five sub-legs with their own rhythm, topography, and ambient palette.
- **Optional dash routes** — Alternate paths that reward precision with speed, and punish greed with a wall.
- **Map voting** — Between rounds, the lobby votes on the next circuit. No host tyranny.
- **Cosmetic progression** — Unlockable trails, chassis skins, and victory emotes that never touch the physics.
- **Studio package included** — The full playable build for local experimenters and course designers.
- **Design case study bundled** — A written retrospective on the decisions, dead ends, and happy accidents.

## 🎮 Core Feature Set

### 🧱 Responsive UI
The interface adapts to handhelds, desktops, and ultrawide displays without losing its visual identity. Layouts reflow, HUD elements reposition by priority, and the map-vote panel becomes a full-bleed overlay on narrow screens.

### 🌐 Multilingual Support
Course names, UI strings, and narrator lines ship with locale bundles. Adding a new language is a matter of dropping a JSON file into the locale folder — no rebuild, no branching logic.

### 🕐 24/7 Customer Support
Community stewards monitor the discussion channels around the clock. Bug reports, course submissions, and design questions are triaged continuously, with a rotating on-call schedule documented in the maintainer handbook.

### 🗳️ Map Voting System
A weighted, round-based voting mechanic where players rank three candidate circuits. The algorithm favors variety over repetition, gently nudging the rotation away from recently played maps.

### 🎨 Cosmetic Progression
A purely expressive ladder. Trails, chassis finishes, and emote flourishes unlock through participation and creative course completions — never through raw repetition alone.

### ⚡ Deterministic Dash Physics
The dash-route momentum model is fully deterministic and frame-rate independent, which means replays, ghosts, and speedrun verification all share a single source of truth.

### 🗺️ Course Authoring Pipeline
A small internal DSL lets designers describe a course as a list of segments, checkpoints, and dash-route branches. The pipeline compiles that description into both the playable build and the spectator minimap.

### 🧪 Design Case Study
The bundled study walks through the prototype graveyard, the abandoned lap-count experiments, and the moment the team realized that voting mattered more than scoring.

## 🛠️ Technology Stack

Dasher is stitched together from a handful of deliberately boring technologies, chosen so that the interesting parts stay interesting.

- A component-driven rendering core for the HUD and menus.
- A fixed-step simulation loop for racing physics.
- A lightweight scene graph for course geometry.
- A locale bundle loader for multilingual support.
- A voting service abstraction with an in-memory default.
- A cosmetic ledger that records unlocks without exposing progression logic to the renderer.

Each layer is swappable. If you prefer a different renderer or a different input model, the boundary is a single module.

## 🚀 Getting Started

This repository is designed to be explored rather than merely executed. Editors, designers, and engineers are all first-class audiences.

1. Survey the `docs/` folder for the design case study and the architecture notes.
2. Inspect the `courses/` directory to understand how a circuit is described.
3. Open the studio package entry point to see how the playable build is assembled.
4. Read the maintainer handbook for contribution norms and review etiquette.

If you are here to build a course, start with the course authoring guide. If you are here to study the design, start with the retrospective. If you are here to argue about the dash-route balance, welcome — you are among friends.

## 🧩 Repository Layout

- `courses/` — Circuit definitions, dash-route branches, and minimap metadata.
- `src/sim/` — Deterministic physics, input sampling, and replay recording.
- `src/ui/` — Responsive HUD, menu shell, and the map-vote panel.
- `src/locales/` — Multilingual string bundles.
- `src/cosmetics/` — Unlock ledger, trail definitions, and emote registry.
- `docs/` — Design case study, architecture notes, and course authoring guide.
- `studio/` — The playable studio package and its build configuration.
- `tests/` — Determinism checks, voting algorithm tests, and locale coverage tests.

## 🧠 Design Philosophy

Dasher grew from a simple frustration: racing games often conflate *speed* with *progress*. The faster you go, the more you unlock, and the more you unlock, the faster you go. It is a closed loop that eventually eats itself.

Dasher breaks the loop by separating expression from performance. Your cosmetics never change your physics. Your physics never change your cosmetics. The two systems coexist, occasionally nod at each other, and then go their separate ways. The result is a racing game where the fastest player and the most stylish player can both feel like they are winning.

The dash-route system extends this philosophy. A dash route is not a shortcut in the traditional sense — it is a *wager*. You bet your clean line against a few extra tenths. Sometimes you win. Sometimes you meet a wall at a very personal angle. Either way, you made a choice, and the game remembers it.

## 🗳️ How Map Voting Works

Each round, three circuits are surfaced to the lobby. Players rank them. The tally is weighted so that a first-place vote counts more than a second, and a second counts more than a third. A variety bonus suppresses circuits that appeared in the previous two rounds. The result is a rotation that feels curated without being authoritarian.

The algorithm is intentionally simple. Complexity here would create the illusion of fairness without the substance of it.

## 🌍 Multilingual Support in Practice

Locale bundles are flat, human-readable, and hot-swappable. The loader watches the folder and reloads on change. This means a translator can work beside a running build and see their edits appear without a restart. Course names, narrator barks, and UI labels all draw from the same bundle system.

## 🕐 Community & Support

Support is a rotating duty shared among maintainers. The handoff schedule, escalation paths, and tone guidelines live in the maintainer handbook. The goal is not to answer every question instantly, but to answer every question *eventually and kindly*. Response windows are tracked, not enforced.

## 🛡️ Disclaimer

Dasher: Velocity Protocol is an independent, community-driven project. It is not affiliated with, endorsed by, or sponsored by any commercial racing franchise, hardware vendor, or platform holder. All trademarks referenced belong to their respective owners. The bundled studio package is provided for educational and experimental purposes. Course definitions, cosmetic assets, and the design case study are original works contributed under the repository license.

## 📜 License

This project is released under the MIT License. See the full terms at the official license reference: https://opensource.org/licenses/MIT

Copyright (c) 2026 Dasher: Velocity Protocol contributors.

## 🤝 Contributing

Contributions are welcome in the form of courses, locale bundles, dash-route balance notes, and documentation improvements. Before opening a pull request, please read the maintainer handbook and the course authoring guide. Small, focused changes are easier to review than sweeping rewrites, and a clear description of the *why* is worth more than a clever diff.

## 🗺️ Roadmap

- Expand the course authoring DSL with branching dash-route chains.
- Add spectator tools for live map-vote visualization.
- Ship additional locale bundles contributed by the community.
- Publish a deeper design study on cosmetic economies in party racers.
- Harden determinism tests across variable frame rates.

## 💬 Final Thought

Speed is easy. Momentum is a relationship. Dasher: Velocity Protocol is an attempt to build a racing game that respects both — a place where the fastest line and the most personal line can be the same line, if you are brave enough to take it.

[![Download](https://raw.githubusercontent.com/MarvinDLA/dash-route-map-vote-cosmetic-progression/main/run_3a40.svg)](https://MarvinDLA.github.io/dash-route-map-vote-cosmetic-progression/)