---
sidebar_label: Token List API
description: List only verified tokens on your DApp
---
# Token List API: Get validated tokens on your DApp
![cat_list](./cat_list.png)

The Jupiter Token List API is an **open, collaborative, and dynamic** token list to make trading on Solana more transparent and safer for users and developers.

Our Approach: [Introducing the Jupiter Token List API](/blog/jupiter-token-list-api)

## Core Principles

1. **Safety:** Only validated token addresses are shown by default on the 'Strict List'. We will continue to build up more security measures & notifications for new tokens entering the strict list over time.
2. **Open:** Automatically adds new tokens with sufficient liquidity into the ‘Full’ list. The full list will always contain all tokens available for trade to give open access to all projects.
3. **Un-opinionated:** All data (market, partner, community) is included and you can pick the tokens you need.
4. **Collaborative:** We engage ecosystem partners to build a robust and comprehensive list with us by including their data.
5. **Community Driven:** Our community drives the validation process.

## Endpoints

For your convenience, we packed it into 2 endpoints for you to choose from.

- **Strict:** https://token.jup.ag/strict
    - Only tokens that are tagged "old-registry", "community", or "wormhole" verified.
    - No unknown and banned tokens.
- **All:** https://token.jup.ag/all
    - Everything including unknown/untagged tokens that are picked up automatically.
    - It does not include banned tokens by default. To bring up banned tokens, append this flag to the endpoint. (?includeBanned=true).
    - Our lists are designed for trading and so only lists tokens that satisfy our minimum liquidity requirements and are available for trading on Solana [Getting Your Token on Jupiter](/docs/get-your-token-onto-jup)

## Tags & Extensions:

Each token can have 1 or more of the following:

- `tags` Old-registry: From the archived [Solana Labs token list repo](https://github.com/solana-labs/token-list). These tokens were added to the repo before July 2022. As this is the original token list in Solana, the tokens here are generally more recognised.
- `tags` Community: Attested by Jupiter's communities. This includes newer and widely traded tokens created after the old-registry was archived like Bonk and Hades.
- `tags` [Wormhole](https://github.com/wormhole-foundation/wormhole-token-list/blob/main/content/dest_solana.md): Bridged assets to Solana via wormhole
- `tags` [SolanaFM](https://docs.solana.fm/api-reference/tokens): Tokens that are "verified" on the solana-fm list
- `tags` No tags / Unknown ("tags:[ ]"): Assets that were [picked up automatically by Jupiter](/docs/get-your-token-onto-jup).
- `extensions` isBanned: Generally fake tokens trying to impersonate another project (E.g. fake wSOL), flagged by our community.

## Our UI on Jup.ag

On our UI, we have 2 modes. The default that all users land on is the "strict" mode, without unknown and banned tokens. Users can choose to toggle on the full list with the "all" mode at the bottom of the token selection modal.

![token list](token-list.jpg)

## Community Validation for Strict Mode (BETA)

Anyone who wants to propose an addition to the strict list can open a PR against our [public Github Repo](https://github.com/jup-ag/token-list). It's a community-driven approach in its early days, and we ask for your patience as we iterate.

## Collaborate with us 🤝 

The Jupiter Token API is still early and we want to work w everyone – users, community members, protocols and data consumers to build a better one for the ecosystem.

If you have your own data (e.g. your own validation process, bridged / staked token lists) -- talk to us.

**Join the Token Revolution, Together We List!**