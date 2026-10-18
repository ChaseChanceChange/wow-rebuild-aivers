# Mission 01 — First Replacement Model

**Status**: Blocked until Mission 00 is complete  
**Priority**: High

## Goal

Prove the full asset pipeline works end-to-end by taking **one simple free prop**, converting it into a native 3.3.5 M2, packaging it, and making it appear in-game as a usable gameobject.

## Suggested starting asset

A simple, low-poly prop with a clear CC0 or public-domain license, for example:
- A wooden crate or barrel
- A simple rock or tree stump
- Any single-mesh object from a trusted CC0 source (Kenney, CC0Tree, Poly Haven, etc.)

Record the exact source URL and license in the field note.

## Success Criteria

1. Source asset is stored under `assets/source/` with license information.
2. Cleaned intermediate files are under `assets/intermediate/`.
3. Final M2 + required skin/texture files are under `assets/final/`.
4. The model is packaged into a custom patch MPQ.
5. A new (or existing) gameobject entry uses the new display ID / model.
6. The object can be spawned in-game (`.gobject add` or equivalent) and is visible with correct textures and reasonable scale.
7. A field note exists at `knowledge/first-model.md` containing exact commands, tool versions, and gotchas.

## Out of Scope

- Characters or animated creatures
- WMOs
- Terrain changes
- Complex materials or particles
- Creating a full prop library

## Recommended approach

1. Choose one simple CC0 asset.
2. Import into Blender, fix scale/orientation, reduce poly count if necessary, export clean intermediate.
3. Convert to M2 using the current best toolchain (document what actually worked).
4. Convert textures to BLP.
5. Create the patch MPQ and place the files with correct internal paths.
6. Register the model so the client and server know about it.
7. Spawn and screenshot it in-game.

## Notes for the agent

- This mission is deliberately tiny. Its only job is to prove the pipeline.
- Prefer existing community conversion knowledge over inventing new methods.
- If a conversion step fails, document the failure clearly and stop rather than expanding into a multi-week research project.
