# Game Modes

Debellum offers several ways to play, built on a single shared combat engine. The skills, heroes, and items you learn carry across all of them.

## MOBA

The classic Debellum experience: teams battle across a lane-based map, farming gold and experience, taking objectives, and pushing to destroy the enemy base. MOBA matches reward coordination, lane control, and decisive team fights.

## Battle Royale

A survival mode where multiple teams drop in and fight to be the last standing. A safe zone steadily shrinks, forcing players together, while loot, extraction points, and environmental hazards shape every decision. See [Battle Royale](battle-royale.md) for the full mechanics.

Battle Royale comes in two flavors:

- **Offline / local** — practice and learn against bots, no server required.
- **Online** — full networked matches against other players.

## Ranked

Ranked is the competitive ladder layered on top of MOBA play. Wins and losses adjust your Ranking Points (RP) and move you through a series of tiers and divisions. Ranked feeds directly into the [progression systems](progression.md) and seasonal rewards.

## Practice

A safe sandbox to learn heroes, test skill combos, and experiment with builds without affecting your rank. Practice mode uses the same combat engine so everything you learn transfers directly to real matches.

## Replay & Spectator

- **Replay** — matches are recorded as deterministic frames, so they can be played back exactly as they happened.
- **Spectator** — watch live matches, useful for tournaments and competitive viewing.

## Mode summary

| Mode | Players | Goal | Notes |
|------|---------|------|-------|
| MOBA | Teams | Destroy enemy base | The core competitive mode |
| Battle Royale (Online) | Many teams | Be the last standing | Shrinking safe zone, loot, extraction |
| Battle Royale (Offline) | vs. Bots | Survive | Practice/learning |
| Ranked | Teams | Climb RP tiers | Competitive ladder over MOBA |
| Practice | Solo | Learn & test | No rank impact |
| Replay / Spectator | — | Watch | Exact deterministic playback |

## Under the hood

All modes share the same deterministic, fixed-point simulation. The mode is selected at launch, and a dedicated set of systems (for example, the safe-zone and extraction logic) activates only for Battle Royale. This shared foundation is why a skill learned in Practice plays identically in a Ranked match.
