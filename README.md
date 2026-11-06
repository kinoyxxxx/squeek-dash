# 🐹 Squeek Dash — The Jumping Challenge

A one-button **endless jumping game** about a very determined hamster, built for
the [Squeekchain](https://squeekchain.com) Genesis community program.

**▶ Play it live: https://squeekdash.duckdns.org**

![Made for Squeekchain Genesis](https://img.shields.io/badge/Squeekchain-Genesis-ffb52e)
![Single file](https://img.shields.io/badge/tech-single%20HTML%20file-2a9d8f)
![No dependencies](https://img.shields.io/badge/dependencies-none-57ff8a)

## 🎮 How to play

The garden path is full of trouble — rocks 🪨, cacti 🌵, puddles 💧 and runaway
cheese wheels 🧀 rolling straight at you.

- **Tap / click / SPACE** — jump
- **Jump again mid-air** — double jump
- **Bounce on a mushroom 🍄** — super jump into high seed trails
- **Grab sunflower seeds 🌻** along the way; rare **golden stars ⭐** are worth 5
- The longer you run, the **faster it gets** (warm-up → jog → zoomies)
- **3 stumbles** end the run — your best distance and harvest are saved

Seed arcs hover over obstacles, so a clean jump literally pays.

## ⚡ Live Squeekchain sync

Squeek Dash is wired into the real chain. Every 15 seconds it polls the public
Squeekchain wheel status API:

```
GET https://api.squeekchain.com/v1/status
    → measurement.rpmMilli, cumulativeWorkUnits
```

- While the **actual hamster wheel is spinning**, the game switches to
  **🔴 LIVE mode**: the hamster runs faster and **every seed is worth double**.
- The footer shows the live wheel state and its lifetime total work units.
- If the API is unreachable, the game simply plays offline — the live feed is
  seasoning, not a crutch.

## 🛠 Tech

- One self-contained `index.html` — vanilla JavaScript + Canvas 2D
- No build step, no dependencies, no tracking, no external assets
- WebAudio bleeps generated in code (no sound files)
- Works on mobile (touch) and desktop (spacebar / arrows)

## 🚀 Run it locally

Any static host works:

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## 📁 Repository layout

| File         | Purpose                                              |
|--------------|------------------------------------------------------|
| `index.html` | The entire game (markup, styles, logic, live sync)   |
| `CNAME`      | Custom domain for GitHub Pages (`squeekdash.duckdns.org`) |
| `LICENSE`    | MIT license                                          |

## 🙌 Credits

A community project by **Squeekbo**, built for the Squeekchain Genesis
"Buildooooor" program. Squeekchain is the hamster-powered toychain on Ethereum
(Sepolia testnet era). Not affiliated with the Squeekchain team.

## 📄 License

MIT — see [LICENSE](LICENSE).
