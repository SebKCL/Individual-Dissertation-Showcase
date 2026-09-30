# Procedurally Generated Educational Dungeon Crawler (Unity / C#)

> My final-year dissertation: a dungeon generator that combines graph rewriting with cellular automata, built into a learning game for primary-school children.

🔒 The code sits in a private repository because this is my King's College London dissertation. Ask me and I'll walk you through it.

## Overview
I built a 2D top-down dungeon crawler for KS2 pupils (about age 10). The game comes first and the questions live inside it. My main contribution is the generator. You can play the prototype, though I ran out of time for combat and the question rooms.

## How the generator works
1. **Graph rewriting (layout):** I start with a 12-room chain and give each room a type (NPC, Puzzle or Mob). The weights shift based on how the player did last run. Rewriting rules then add branches and merges.
2. **Room building:** Unity Tilemaps lay out rooms of random size, blend tiles near doors, and place objects by rule.
3. **Cellular automata (detail):** Moore-neighbourhood rules run over separate tile and object grids to clump rocks, plants and stone into natural shapes.
4. **Room finishing:** each room type gets its own pass. I place NPCs, hide puzzle objects, cluster enemies and centre bosses. Puzzle timers scale with room size.

## Other systems
- Player stats: HP, ATK, DEF, EXP and levels, stamina, and a death penalty that narrows the gap between strong and weak players
- Gear built on ScriptableObjects, with random sub-stats and an inventory screen
- Cosmetic classes that change with the weapon you equip
- A village hub, a merchant, and menus, options, pause screen and HUD

## Status
Generation, world, stats, gear and UI all work. Combat and the in-room questions exist on paper only.

## Skills
Procedural generation · game architecture · Unity · C# · systems design · research writing

## Tech stack
Unity · C# · Tilemap · ScriptableObjects · Unity UI
