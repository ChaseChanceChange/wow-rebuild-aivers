# wow-rebuild

**A structured, multi-agent laboratory for rebuilding the visual layer of World of Warcraft 3.3.5 (Wrath of the Lich King) while preserving the original gameplay systems.**

This project uses [AzerothCore](https://github.com/azerothcore/azerothcore-wotlk) as the server and the official 3.3.5a client as the engine.  
We keep the combat, quests, SmartAI, pathfinding, networking, and UI framework.  
We progressively replace models, textures, terrain, effects, and UI art with high-quality free and open assets that can be converted into native 3.3.5 formats.

The work is done through **small, verifiable missions**.  
AI coding agents (Claude Code, Cursor, Codex, OpenCode, local models, etc.) are directed via [Universal Modder](https://github.com/rehan-remade/universal-modder) and the rules in `AGENTS.md`.  
Every finished mission produces a field note so the next agent starts ahead instead of rediscovering the same problems.

## Vision

See [`docs/vision.md`](docs/vision.md).

## Quick Start for Humans

1. Clone this repository.
2. Install a clean 3.3.5a client and a working AzerothCore server.
3. Install Universal Modder into your preferred coding agent(s).
4. Read `AGENTS.md` and `docs/pipeline.md`.
5. Start with `missions/00-bootstrap/MISSION.md`.

## Quick Start for Agents

1. Read `AGENTS.md` completely.
2. Search existing knowledge: `um kb search "world of warcraft"` or look in `knowledge/`.
3. Open the assigned mission file under `missions/`.
4. Follow the Universal Modder 10-step loop, constrained by the mission success criteria.
5. Never expand scope. Finish the vertical slice, verify in-game, write the field note, and stop.

## Repository Layout

```
wow-rebuild/
├── AGENTS.md                 # Hard rules for every AI agent
├── docs/
│   ├── vision.md             # Project philosophy and non-goals
│   ├── pipeline.md           # How free assets become client content
│   └── style-bible.md        # Visual guidelines (filled in later)
├── missions/                 # Discrete, reviewable work units
├── knowledge/                # Field notes written by agents
├── tools/                    # Conversion scripts and helpers
├── assets/
│   ├── source/               # Original free assets (CC0, etc.)
│   ├── intermediate/         # Blender / glTF / cleaned files
│   └── final/                # M2, WMO, BLP, ADT ready for patches
├── client-patches/           # Content that goes into custom MPQs
└── server/                   # AzerothCore customisations and SQL
```

## License

- Code and documentation in this repository: MIT
- Original Blizzard assets: never redistributed
- Third-party assets: only those with licenses that explicitly allow this use (CC0 preferred)

## Status

Very early. Bootstrap mission not yet completed.
