# Wallet & Onboarding

To own and trade Debellum NFTs, you connect a crypto wallet to your account. The game supports several wallet providers and blockchains, and is designed to make onboarding as smooth as possible — including for players new to Web3.

## Two account types

Debellum distinguishes between how a player pays and owns:

| Account type | Description |
|--------------|-------------|
| **Web2** | Traditional account using soft currencies and standard purchases. No wallet required to play. |
| **Web3** | Wallet-connected account that can mint, own, and trade NFTs and use the on-chain token. |

You can enjoy the full game as a Web2 player; connecting a wallet unlocks the ownership layer on top.

## Supported wallets

| Provider | Best for |
|----------|----------|
| **Immutable Passport** | Smooth, gas-efficient onboarding on Immutable zkEVM, including NFT transfers. |
| **MetaMask** (via Nethereum) | The most widely used Ethereum wallet, including web/desktop flows. |
| **TokenPocket** | Mobile-first wallet for signing transactions on the go. |
| **WalletConnect-style flows** | Connecting external wallets through an embedded browser. |

Wallet connection supports message signing (including Sign-In-With-Ethereum) so you can prove ownership of your address securely.

## Supported chains

Debellum's economy spans multiple blockchains, letting assets and the token operate where they make the most sense:

| Chain | Role |
|-------|------|
| **Ethereum** | The base layer for high-value assets. |
| **Immutable zkEVM** | Primary chain for game NFTs and the ACP token. |
| **zkSync** | Low-cost L2 transactions. |
| **BSC (Binance)** | Broad accessibility and liquidity. |
| **Metis (Andromeda)** | Additional L2 support. |
| **Ronin** | Gaming-focused chain support. |
| **Gate Chain** | Additional ecosystem support. |

## Generated wallets and binding

For players who don't already have a wallet, the system can **generate a wallet address bound to your account** (e.g. tied to your email), removing the biggest barrier to entry. Players who do have a wallet can **bind an external wallet** to their account. Either way:

- **One wallet is bound to one account** to prevent abuse.
- Both internal (generated) and external (player-owned) wallets are supported, including holding NFTs across both.

## Deposits and withdrawals

Once connected, you can move crypto in and out through the wallet interface — depositing tokens to use in the game's economy and withdrawing earnings or holdings. A dedicated deposit/withdraw flow handles these transactions across the supported chains.

## Security and anti-abuse

Onboarding includes safeguards to keep the economy healthy:

- **One-wallet-per-account** binding.
- **Device fingerprinting** and multi-account detection.
- **Rate limits** on sensitive actions like minting.
- The ability to **pause minting** during gas spikes to protect players.

## Roadmap: friction-free transactions

A planned **MegaETH L2** integration introduces **sponsored gas** via a paymaster, meaning the game can cover transaction fees for common actions like minting. Combined with batch operations, the goal is an onboarding and ownership experience that feels as smooth as a traditional game while preserving real ownership.
