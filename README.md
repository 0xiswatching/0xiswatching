<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/name-dark.svg">
  <img src="assets/name-light.svg" alt="0xiswatching" width="100%">
</picture>

I build software that watches on-chain state and acts on it: bots that trade on a timer, treasury flows that claim fees and buy back, and a coordination layer that pays robots for verified work. Mostly TypeScript on Node, across Solana and EVM chains, running on Linux boxes I operate myself.

## Work

### [bumpbot-evm](https://github.com/0xiswatching/bumpbot-evm)

Timed micro buy/sell bot for Pons V2 bonding-curve launches. It buys a sliver, waits about ten seconds, sells it back, and repeats, so a pair keeps appearing in the launchpad's activity ranking. One profile file per token. Curve, pair asset, creator tax and graduation state are read from the factory at startup, so a profile can't drift out of date. Comes with a token-gated dashboard and Telegram control. TypeScript and viem.

### [dragon-treasury](https://github.com/0xiswatching/dragon-treasury)

Node backend for a Pump.fun creator-fee buyback loop on Solana. Each cycle claims fees, spends them on the configured token minus a reserve, and moves what it bought to a dead wallet, so the whole flow is verifiable on-chain. Runs in simulate or live mode and exposes JSON endpoints for a dashboard. Express, web3.js and spl-token.

### [DeMech](https://github.com/0xiswatching/DeMech)

Coordination and payments layer connecting physical robots to Solana. Robots hash telemetry into Merkle roots, an oracle attests with an ed25519 signature, and an Anchor program releases SPL tokens from a per-task escrow vault. Edge agent with a ROS2 bridge, FastAPI coordinator, Rust on-chain program.

## Now

A token launchpad on Uniswap v4 for BNB Smart Chain, and a multiplayer shooter in Unity. Both private until they are less rough.

## Tools

TypeScript and Node for most things. Solidity and viem on EVM chains; Anchor, web3.js and Rust on Solana. Python where a coordinator or a model is involved, C# inside Unity. Postgres, Linux servers and a lot of shell.
