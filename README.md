# Merge

A free, single-file browser coin-merging puzzle with Nano at its heart. Slide tiles up a ladder of coins — Dogecoin all the way to Nano — in the style of 2048. No build step, no backend, no fees.

## Play

- **Move** with swipe, the arrow keys / WASD, or the on-screen pad. Every coin on the board slides as far as it can; two coins of the same kind merge into the next coin up the ladder.
- **Ladder:** Dogecoin → Litecoin → XRP → Cardano → BNB → Solana → Polkadot → Monero → Ethereum → Bitcoin → **Nano**. Reaching an XNO tile wins the round — keep playing afterwards for a higher score, or finish there.
- **Daily challenge:** the same starting board and coin draws for everyone, new every day at 00:00 UTC. Play until the board is full, or finish early once you've reached Nano, to keep your streak.
- **Blitz 90:** 90 seconds on the clock. If the board fills up, it clears itself and your score carries on.
- **Endless:** free play, no clock. The round ends when the board is full and no merges are left.
- **Undo:** once per round, free of charge (twice for supporters).
- **Ranks** (by times reached Nano): Newbie, Hodler (5), Diamond Hands (15), Whale (40), Satoshi (100).

Everything is stored in the player's browser.

## Deploy on GitHub Pages

1. Create a new repository, for example `merge`.
2. Upload `index.html` and `README.md` to the root of the repository.
3. Open **Settings > Pages**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, then save.
4. After a minute the game is live at `https://<your-username>.github.io/merge/`.

## Donations

The tip card works the same way as in the other Feeless games:

- A `nano:` payment link with the chosen amount, shown as a QR code and an **Open in wallet** button.
- A **Copy address** button.
- An **I've sent it, check** button that asks public Nano nodes whether a matching payment arrived, and unlocks the supporter perks (Gold, Mint and Neon accent colours, and a second undo) on that browser.

To use a different wallet, change `NANO_ADDRESS` near the top of the script in `index.html`. If the public RPC endpoints in `RPCS` ever block browser requests, point them at your own proxy.

The supporter unlock is stored in `localStorage`, so it is a thank-you perk, not secure access control. Coin tickers and colours are used for fun and are not endorsements.

Add `?selftest` to the URL to expose a small `window.__mg` object for automated tests.
