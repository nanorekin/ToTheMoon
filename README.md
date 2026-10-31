# To the moon

A free, single-file browser asteroid-shooting game with Nano at its heart. Steer your rocket, blast asteroids before they reach you, and scoop up the occasional XNO coin. No build step, no backend, no fees.

## Play

- **Steer** by dragging your finger (or mouse) across the board, or with the arrow keys / A and D. Your rocket fires automatically.
- **Splitting asteroids:** large asteroids break into two medium ones when hit; medium ones break into two small ones. Only small asteroids are destroyed outright, so a big rock pays off if you can clear the whole cluster.
- **XNO coin:** drifts down now and then. Shoot it or fly into it for a bonus — no danger if you miss it.
- **Daily challenge:** the same asteroid field for everyone, new every day at 00:00 UTC. Destroy 40 asteroids to clear the day and keep your streak.
- **Quick 60:** 60 seconds, score as much as you can.
- **Survival:** endless — asteroids get faster and more frequent the longer you last.
- **Lives:** 3 to start (4 for supporters), with a brief shield after each hit.
- **Scoring:** points scale up with your combo (asteroids destroyed back to back without taking a hit); getting hit or letting one slip past resets it.
- **Ranks** (by total asteroids destroyed): Newbie, Hodler (200), Diamond Hands (700), Whale (2,000), Satoshi (5,000).

Everything is stored in the player's browser.

## Deploy on GitHub Pages

1. Create a new repository, for example `to-the-moon`.
2. Upload `index.html` and `README.md` to the root of the repository.
3. Open **Settings > Pages**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, then save.
4. After a minute the game is live at `https://<your-username>.github.io/to-the-moon/`.

## Donations

The tip card works the same way as in the other Feeless games:

- A `nano:` payment link with the chosen amount, shown as a QR code and an **Open in wallet** button.
- A **Copy address** button.
- An **I've sent it, check** button that asks public Nano nodes whether a matching payment arrived, and unlocks the supporter perks (Gold, Mint and Neon accent colours, and a 4th life) on that browser.

To use a different wallet, change `NANO_ADDRESS` near the top of the script in `index.html`. If the public RPC endpoints in `RPCS` ever block browser requests, point them at your own proxy.

The supporter unlock is stored in `localStorage`, so it is a thank-you perk, not secure access control.

Add `?selftest` to the URL to expose a small `window.__ms` object for automated tests.
