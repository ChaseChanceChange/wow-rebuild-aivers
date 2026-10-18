# Mission 02 — Character Base (Humanoid)

**Status**: Blocked until Mission 01 is complete  
**Priority**: High

## Goal

Establish a clean, reusable humanoid character foundation that preserves the original animation set while allowing future modular appearance work.

## Success Criteria

1. A working male and female humanoid base derived from (or compatible with) the original human skeletons so that existing animations continue to function.
2. The bases are visible in the client (character creation or via a test creature/NPC).
3. Basic texture / material setup works (no missing textures).
4. Documentation exists explaining:
   - How the bases were created or cleaned
   - How new body/head/hair pieces should be added later
   - Any limitations discovered
5. Field note at `knowledge/character-base.md`.

## Out of Scope

- Full customisation UI
- Multiple races
- High-detail cybernetic or heavily stylised variants
- Animation authoring
- Item appearance system beyond the minimum needed to display the base

## Design intent

We want the original animation system to keep working.  
Therefore the safest path is to start from the existing human male/female skeletons and geometry, clean them up, and treat them as the canonical base for future modular pieces.

If a completely new skeleton is proposed, the agent must first prove that a useful subset of the original animations can still play correctly. Otherwise prefer the existing skeletons.

## Notes for the agent

- Mission 01 must already have proven that *some* custom M2 can appear in-game.
- Keep the first version deliberately plain. Visual style decisions come later.
- Record every tool and version used for mesh and skin export.
