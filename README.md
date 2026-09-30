# Procedurally Generated Educational Dungeon Crawler (Unity / C#)

> Final-year dissertation: a hybrid procedural content generation (PCG) pipeline that combines graph rewriting and cellular automata to build varied, replayable dungeons for an educational game.

🔒 **The source code is in a private repository** because this is my university dissertation project at King's College London. I'm happy to walk through the code on request.

## Overview
This is a 2D top-down dungeon crawler aimed at KS2 learners (around age 10). It takes a "game-first, education-second" approach, where the learning content is built into the gameplay. The main technical contribution is the dungeon generator. The project is a working prototype and some planned features were left unfinished (see Status).

## Hybrid PCG pipeline
1. **Graph rewriting (macro layout):** builds a 12-room dungeon graph and assigns room types (NPC, Puzzle, Mob) using weighted randomness that adapts to the player's previous run. It then applies rewriting rules to create branches and merges.
2. **Room instantiation:** uses Unity Tilemaps with randomly sized rooms, blended transition tiles near doors, and rule-based object placement.
3. **Cellular automata (micro structure):** Moore-neighbourhood rules run over separate tile and object grids, which produces natural-looking clustering and texture.
4. **Room-specific post-processing:** places NPCs, hides puzzle objects, spawns enemies in clusters and positions bosses. Puzzle timers are calculated from room size.

## Other systems implemented
- A player stats model covering HP, ATK, DEF, EXP and levelling, stamina, and a death/respawn feedback loop
- A gear system built on ScriptableObjects, with randomly rolled sub-stats and an inventory UI
- Cosmetic classes that change with the equipped weapon
- A village hub, a merchant, and a full menu/options/pause/HUD UI

## Status
PCG, world, stats, gear and UI are functional. Combat and the in-room question mechanics were designed but not completed.

## Skills demonstrated
Procedural generation algorithms · game architecture · Unity · C# · systems design · academic research and write-up

## Tech stack
Unity · C# · Unity Tilemap · ScriptableObjects · Unity UI
