# Asset Pipeline

This document describes how free / open assets become content that the 3.3.5 client and AzerothCore can use.

## High-level flow

```
Free source asset
    ↓
assets/source/          (original download, license noted)
    ↓
Clean / retarget / simplify in Blender
    ↓
assets/intermediate/    (glTF, OBJ, cleaned textures, etc.)
    ↓
Convert to native 3.3.5 formats
    ↓
assets/final/           (M2, skin, WMO, BLP, ADT…)
    ↓
Package into custom patch MPQ
    ↓
client-patches/
    ↓
Client loads patch → in-game verification
    ↓
Server extractors run (maps / vmaps / mmaps) if needed
```

## Supported source types (preferred order)

1. **CC0 / Public Domain** – safest
2. Clear permissive licenses that allow conversion and redistribution
3. Unreal Engine Marketplace free assets **only when the license permits this use** (check carefully; many do not allow re-export into other engines)

Avoid anything with “non-commercial only”, “no derivatives”, or unclear terms unless the human explicitly approves.

## Format targets

| Content type       | Target format(s)          | Primary tools                          |
|--------------------|---------------------------|----------------------------------------|
| Characters / creatures | M2 + .skin (+ .anim)   | WoW Blender Studio, MultiConverter    |
| Static world objects  | WMO (root + groups)     | WoW Blender Studio                    |
| Small props / doodads | M2                      | Same as characters                    |
| Textures             | BLP                     | BLPLab / BLPConverter                 |
| Terrain               | ADT + WDT               | Noggit, FuTa, ObjToADT, adtcreator    |
| Database entries      | SQL + DBC overrides     | Keira3, WDBX, Azeroth World Editor    |

## Critical conversion notes

- **Scale and orientation** must match WoW’s coordinate system (X north, Y west, Z up). Most modern assets need adjustment.
- **Animations** are the hardest part. Prefer reusing existing humanoid or creature skeletons whenever possible so the original animation set continues to work.
- **Collision** for WMOs and larger M2s must be correct or NPCs and players will fall through or get stuck.
- **LODs** and texture size should be reasonable for a 2008-era client. Extremely high-poly or 4K textures will hurt performance.

## Packaging rules

- All new content goes into numbered custom patches (e.g. `patch-Z.MPQ`, `patch-enUS-Z.MPQ`).
- Never modify the original `common.MPQ`, `expansion.MPQ`, etc.
- Keep a clear mapping from source asset → final files in the field note.

## Verification checklist (minimum)

- [ ] Model / texture appears in WoW Model Viewer or in-game
- [ ] Correct scale and orientation
- [ ] No missing textures (pink/black)
- [ ] Collision works (for placeable objects)
- [ ] Server can extract the necessary data if the content is a map
- [ ] No original Blizzard files were added to the repository
