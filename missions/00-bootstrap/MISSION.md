# Mission 00 — Bootstrap

**Status**: Ready  
**Priority**: Critical  
**Assigned to**: Any agent (or human)

## Goal

Create a clean, reproducible foundation so every later mission can start from the same known-good state.

## Success Criteria

All of the following must be true:

1. A clean 3.3.5a client folder is documented (path + exact build).
2. A working AzerothCore server is documented (commit hash + how it was built).
3. Universal Modder is installed and the `um` CLI works.
4. This repository structure exists and matches the layout in the root README.
5. A short `knowledge/bootstrap.md` field note exists that records:
   - Exact versions of client, server, Universal Modder, Noggit, Blender, WBS, etc.
   - Any gotchas encountered while setting up
   - Commands used to verify the client can connect to the server
6. A simple “hello world” verification: the client logs in and the character can walk in a starting zone.

## Out of Scope

- Any model or texture replacement
- Any database changes beyond what is required for a normal private server
- Installing extra modules that are not needed for basic operation

## Deliverables

- Updated documentation in `docs/` if any paths or versions differ from expectations
- `knowledge/bootstrap.md` field note
- Confirmation that a character can log in and move

## Notes for the agent

- Prefer isolated folders. Do not overwrite the human’s existing installations without asking.
- Record every tool version. “Latest” is not acceptable in the field note.
- If the human already has a working client + server, document *their* setup instead of forcing a reinstall.
