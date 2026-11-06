# Squeek Dash — Beat the Wheel

A one-button arcade mini-game about a hamster, a wheel, and perfect timing.

**Play:** the bead rides the rim of the wheel. Tap (or press SPACE) the moment it
crosses the golden zone to snatch the seed. Bad taps cost a heart. The wheel
breathes like a real hamster — naps, jogs, and sudden zoomies — and it only
speeds up as you level.

**Live sync:** the game polls the real Squeekchain wheel status
(`api.squeekchain.com/v1/status`). When the actual hamster is running, the
ZOOMIES BONUS doubles every seed you catch. The game is fully playable offline;
the live feed is seasoning, not a crutch.

Built for Squeekchain Genesis — the hamster-powered toychain on Ethereum
(Sepolia testnet era). A community project by Squeekbo; not affiliated with
the Squeekchain team.

## Run it

Any static host works. Locally:

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Tech

Single self-contained `index.html` — vanilla JS + SVG, no build step, no
dependencies, no tracking.
