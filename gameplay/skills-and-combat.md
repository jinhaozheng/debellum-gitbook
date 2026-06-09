# Skills & Combat

Combat is where Debellum is won or lost. Every hero has a kit of abilities mapped to skill slots, and every hit is resolved by a precise, deterministic damage system.

## Skill slots

A hero's abilities are organized into slots, each with a familiar role:

| Slot | Typical role |
|------|--------------|
| **Basic Attack (A)** | Auto-attack; the bread-and-butter damage. |
| **Q / W / E** | Core active abilities — the hero's signature tools. |
| **R (Ultimate)** | The hero's most powerful, defining ability. |
| **Passive (P)** | An always-on effect that shapes the hero's playstyle. |
| **Item & special slots** | Abilities granted by items, vision tools (e.g. an "eye"), and hero-specific extras. |

Some heroes have additional mechanics layered on top — charge-up attacks, instant actions, battle-pattern switches, and passive triggers — handled by the skill engine so they feel responsive and consistent.

## How abilities work

Each ability is built as an **action graph** — a structured sequence of states (windup, cast, effect, cooldown) that the engine runs deterministically. This is what lets complex abilities — channels, charges, multi-stage casts, crowd control — behave identically for every player in the match.

Skills are aimed and launched using indicators that show range and direction before you commit, so you can line up that game-winning ability with precision.

## Damage types

All damage in Debellum falls into one of four categories, each interacting differently with a target's defenses:

| Damage type | Reduced by | Notes |
|-------------|-----------|-------|
| **Physical** | Armor | Mitigated by the target's armor value. |
| **Magic** | Magic Resist | Mitigated by magic resistance. |
| **Real (True)** | Nothing | Ignores defenses entirely. |
| **Cure** | — | Healing rather than damage. |

On top of the type, the damage formula accounts for **critical hits, dodge, armor, and magic resistance**, all computed with fixed-point math for perfect determinism.

## Projectiles and area effects

Many abilities and basic attacks create **bullets** (projectiles) that travel, collide, and seek targets. The simulation tracks their movement and collisions frame-by-frame, so a dodged skillshot is a real, earned dodge — not a network artifact.

## Buffs and crowd control

Abilities and items apply **buffs** and **debuffs** — temporary effects that modify stats, apply damage over time, or impose crowd control (stuns, slows, and other "be-controlled" states). The buff system manages stacking, duration, and expiry consistently across client and server.

## Why it stays fair

Combat runs on the same **deterministic, lockstep simulation** described in the [overview](README.md):

- The client **predicts** your actions instantly for a snappy feel.
- The server holds the **authoritative** state.
- If prediction and authority ever diverge, the client corrects (rolls back) to match the server.

Because everything uses fixed-point math and a shared rule set, two players watching the same fight always see the same outcome. Skill — not latency or hardware — decides the result.
