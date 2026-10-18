# Mission 03 — Tiny Test Zone

**Status**: Blocked until Mission 01 and Mission 02 are complete  
**Priority**: Medium

## Goal

Create one very small, fully playable outdoor area that uses predominantly new visual assets while still functioning under AzerothCore (correct collision, pathfinding, and basic spawns).

## Success Criteria

1. A new or heavily modified set of ADT tiles (ideally 1–4 tiles) exists.
2. Terrain uses new or heavily altered textures derived from free sources.
3. At least several of the props created in earlier missions (or new ones following the same pipeline) are placed.
4. The zone can be entered from the client.
5. A character can walk around without falling through the world.
6. Basic pathfinding works for at least one test NPC.
7. Field note at `knowledge/tiny-zone.md` documents the exact map creation and extraction steps.

## Out of Scope

- Full continent
- Complex indoor WMOs
- Quest design
- Large cities
- Weather or lighting overhauls beyond the minimum needed for visibility

## Recommended approach

- Start from a blank or nearly blank ADT grid (adtcreator / GruulMeWDT + Noggit).
- Keep the area small enough that extraction and testing stay fast.
- Re-use the prop pipeline proven in Mission 01.
- Run the official AzerothCore extractors after the client-side files are ready so vmaps/mmaps exist.

## Notes for the agent

- Geography can be simple. The goal is a working end-to-end zone, not a beautiful landscape.
- Document every extractor command and any custom map.dbc / MapDifficulty entries required.
