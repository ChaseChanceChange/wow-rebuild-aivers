# Vision

## What this project is

A long-term, multi-agent laboratory that treats World of Warcraft 3.3.5 (Wrath of the Lich King) as a reusable **engine + gameplay framework**.

We keep:
- The client executable and its systems
- AzerothCore as the authoritative server
- Combat, targeting, casting, inventory, talents, quests, grouping, pathfinding, SmartAI, networking, and the FrameXML/Lua UI framework

We replace, over time:
- Character and creature models
- World objects (M2 / WMO)
- Terrain textures and height data where it improves the result
- Spell visual effects
- UI artwork and some sound

The end state is a game that *feels* like classic Wrath in its systems and pacing, but looks like a fresh, high-quality world built from free and open assets.

## What this project is not

- A cyberpunk, sci-fi, or themed total conversion (that idea was deliberately set aside)
- A commercial product
- A redistribution of Blizzard assets
- An attempt to rewrite the client or server from scratch
- A project that tries to rebuild the entire world in one pass

## Core principles

1. **Gameplay first**  
   The original feel of movement, combat, and progression is sacred. Visual changes must not break it.

2. **Small, verified steps**  
   Every piece of work is a mission with clear success criteria and mandatory in-game verification.

3. **Knowledge compounds**  
   Agents write field notes. Later agents (and humans) start from those notes instead of repeating the same research.

4. **Legal cleanliness**  
   Only assets with clear permissive licenses are used. Original client files stay on the user’s machine and are never committed.

5. **Open collaboration between humans and agents**  
   Multiple coding agents (Claude, Cursor, Codex, local models, etc.) can work on the same repository as long as they obey `AGENTS.md` and the mission files.

## Long-term success looks like

- A working modular character appearance system built on the original humanoid skeletons (so animations keep working)
- A growing library of free-asset-derived M2 and WMO content that can be placed with existing tools
- At least one fully playable starter zone that uses predominantly new visuals while retaining original quest flow and geography
- A documented, repeatable pipeline that any competent agent can follow to add more content
- A public knowledge base of what actually works for 3.3.5 asset conversion in 2026+

## Non-goals (for the foreseeable future)

- Full Eastern Kingdoms + Kalimdor visual rebuild
- Retail model parity or modern rendering features
- Cross-expansion client support
- Automated “AI generates the entire world” pipelines without human review
