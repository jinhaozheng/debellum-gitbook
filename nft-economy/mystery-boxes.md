# Mystery Boxes

Mystery Boxes are Debellum's gacha-style reward mechanic. You spend currency to open a box and receive a randomized reward, with a **pity system** that guarantees high-quality drops within a bounded number of opens — so luck never leaves you empty-handed forever.

## The three box tiers

| Box | Cost | Currency | Hero drop rate | NFT chance |
|-----|------|----------|----------------|------------|
| **Standard** | 1,500 | Gold | ~2% | 0% |
| **Premium** | 50 | Gems | ~5% | 60% |
| **Legendary** | 150 | Gems | ~10% | 72% |

- **Standard** boxes are the everyday, Gold-funded option — generous on common rewards, but they never produce NFTs.
- **Premium** and **Legendary** boxes cost Gems and have a high chance to produce **on-chain NFT cosmetics**, with Legendary offering the best odds at the rarest items.

## The pity system

Every box tier tracks **pity counters** — the number of opens since you last received each rarity. When a counter reaches its threshold, your **next** open is guaranteed to contain at least that rarity, and the counter resets.

| Box | Rare pity | Epic pity | Legendary pity | Hero pity |
|-----|-----------|-----------|----------------|-----------|
| **Standard** | 15 | — | — | 50 |
| **Premium** | 10 | 30 | — | 25 |
| **Legendary** | 5 | 15 | 40 | 15 |

### How pity works

1. Counters are **visible in the UI** in real time.
2. Each open that doesn't hit a given rarity **increments** that rarity's counter.
3. On reaching a threshold, the **next** open **forces** a drop of that rarity.
4. Triggering a pity **resets** that counter to zero.
5. Counters **persist across sessions** — they're saved with your account.
6. Each rarity tier is tracked **independently** (hitting a Rare pity doesn't affect the Epic counter).

This means the worst-case luck is bounded: you always know the maximum number of opens before a guaranteed result.

## Drop quality philosophy

Drop tables are deliberately tiered:

- **Standard:** no NFTs at all; weighted heavily toward common rewards (Rare-or-better only ~8%).
- **Premium:** a 60% chance at NFT cosmetics.
- **Legendary:** a 72% chance at NFT cosmetics, split across Rare, Epic, and Legendary results.

NFT drops from boxes have **limited supply** and are flagged as **tradeable**, making rare box pulls genuinely collectible.

## Duplicates

If a box gives you something you already own, it isn't wasted — duplicates are **converted** into Hero Shards and Gold:

| Box | Shards | Gold |
|-----|--------|------|
| Standard | 15 | 500 |
| Premium | 25 | 1,000 |
| Legendary | 40 | 2,000 |

This keeps every open meaningful, feeding back into hero upgrades and crafting.

## Server-authoritative and fair

Box opening is fully **server-authoritative**: the client sends an open request, the server rolls the result (applying pity rules), deducts currency, handles duplicates, and returns the outcome. The client only displays what the server decided. This prevents tampering and guarantees the published odds and pity thresholds are honored for everyone.

## The Bellum Box

Alongside the three standard tiers, the **Bellum Box** is opened with **Bellum Points (BP)** (around 2,000 BP), tying the betting economy into the reward loop. See [Currencies](currencies.md) for how BP is earned and spent.
