# Feeless Flap

A free, single-file browser flyer. You are an XNO coin trying to avoid fees: flap through the gaps in the red fee gates and see how far you can get. No build step, no backend, no fees.

## Play

- **Flap:** tap, click or press Space (or Up / W) to flap upwards. Gravity does the rest.
- **Gates:** every gate you pass scores one point. The course speeds up and the gaps shrink slightly as you go, up to a limit.
- **Medals:** Bronze at 10 gates, Silver at 25, Gold at 50, Diamond at 100.
- **Daily course:** the same gate layout for everyone, new every day at 00:00 UTC. Pass 15 gates to clear it and keep your daily streak.
- **Free play:** your best run is stored per device.

Everything is stored in the player's browser.

## Deploy on GitHub Pages

1. Create a new repository, for example `feeless-flap`.
2. Upload `index.html` and `README.md` to the root of the repository.
3. Open **Settings > Pages**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, then save.
4. After a minute the game is live at `https://<your-username>.github.io/feeless-flap/`.

## Donations

The tip card works the same way as in the other Feeless games:

- A `nano:` payment link with the chosen amount, shown as a QR code and an **Open in wallet** button.
- A **Copy address** button.
- An **I've sent it, check** button that asks public Nano nodes whether a matching payment arrived, and unlocks the supporter coin skins (ETH, SOL, XMR, DOGE colours) on that browser.

To use a different wallet, change `NANO_ADDRESS` near the top of the script in `index.html`. If the public RPC endpoints in `RPCS` ever block browser requests, point them at your own proxy.

The supporter unlock is stored in `localStorage`, so it is a thank-you perk, not secure access control. Coin names and tickers are used for fun and are not endorsements.

Add `?selftest` to the URL to expose a small `window.__ff` object for automated tests.
