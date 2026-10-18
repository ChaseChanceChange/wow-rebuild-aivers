# AGENTS.md — Rules for every AI coding agent working on wow-rebuild

You are an AI coding agent helping rebuild the *visual layer* of World of Warcraft 3.3.5 while preserving the original gameplay systems.

This project uses Universal Modder methods. Follow the standard 10-step loop, but you are **strictly constrained** by the mission file you are given.

## Hard Rules (never break these)

1. **Never expand scope.**  
   Do only what the current `MISSION.md` asks for. If you discover something interesting, write it in the field note under “Future work” and stop.

2. **Never ship original Blizzard files.**  
   No extracted MPQ contents, no decompiled client code, no retail assets in any commit.

3. **Verify in the real client + server.**  
   A change is not finished until it is visible and functional in a running 3.3.5 client connected to AzerothCore. Screenshots or a short recording are required.

4. **Prefer free / CC0 assets.**  
   Only use assets whose licenses clearly allow conversion and redistribution in a non-commercial total-conversion context. Prefer CC0. When in doubt, ask the human.

5. **One vertical slice at a time.**  
   Finish one complete path (source → intermediate → final format → in-game) before starting the next.

6. **Write a field note.**  
   At the end of every mission, create a clear field note in `knowledge/` that contains:
   - Exact tool versions
   - Commands that worked
   - Gotchas (symptom → cause → fix)
   - What was verified and what was not

7. **Ask before destructive actions.**  
   Do not overwrite the human’s client, server, or existing patches without explicit permission. Always work in isolated folders or new patch MPQs.

8. **Keep the gameplay systems intact.**  
   Do not change core combat, networking, SmartAI behaviour, or database schemas unless the mission explicitly requires it.

## Preferred Tools (use these first)

- **Client / Server**: 3.3.5a client + AzerothCore
- **Map editing**: Noggit Red (or current stable Noggit)
- **Models**: WoW Blender Studio (WBS), WoW Model Viewer r252, MultiConverter
- **Textures**: BLPLab / BLPConverter
- **Database**: Keira3, Azeroth World Editor
- **Packaging**: Ladik’s MPQ Editor (or equivalent)
- **Agent method**: Universal Modder (`um` CLI + skills)

## How to Start a Mission

1. Read this file.
2. Read `docs/vision.md` and `docs/pipeline.md`.
3. Open the assigned `missions/XX-name/MISSION.md`.
4. Search `knowledge/` and Universal Modder knowledge base for prior art.
5. Execute the mission.
6. Commit only the files that belong to the mission.
7. Write the field note.
8. Stop and wait for human review.

## Success Definition

A mission is successful only when:
- The stated success criteria in the mission file are met.
- The change is visible/functional in-game.
- A field note exists and is accurate.
- No original Blizzard assets were committed.
- Scope was not expanded.
