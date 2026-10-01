# 🏓 Pong

A fast, polished, single-file Pong game built with vanilla HTML5 Canvas and JavaScript. No dependencies, no build step, and it works fully offline.

![HTML5](https://img.shields.io/badge/HTML5-Canvas-e34f26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-f7df1e?logo=javascript&logoColor=black)
![Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)
![Offline](https://img.shields.io/badge/works-offline-blue)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

## ✨ Features

- **Smooth gameplay at any refresh rate**: delta-time physics keep the speed identical on 60, 120 and 144 Hz displays.
- **Multiple controls**: mouse, touch drag, arrow keys, or `W` / `S`.
- **Beatable CPU opponent**: limited speed and a random aiming error on each return.
- **Angle-based bounces**: where the ball hits the paddle decides where it goes.
- **Progressive difficulty**: the ball speeds up 5% on every paddle hit, up to a cap.
- **Match flow**: start screen, pause/resume, and first to 7 wins.
- **Visual polish**: glowing paddles and ball, ball trail, particle bursts, and screen shake.
- **Procedural sound effects**: generated with the Web Audio API, so there are no audio files. Press `M` to mute.
- **Responsive and crisp**: scales to any screen and renders sharply on high-DPI displays.
- **Auto-pause** when you switch tabs.

## 🎮 Controls

| Action | Input |
|---|---|
| Move paddle | Mouse / touch drag, `↑` `↓`, or `W` `S` |
| Start / pause / resume | `Space`, `Enter`, `P`, or click / tap |
| Mute / unmute | `M` |

## 🚀 Getting Started

```bash
git clone https://github.com/andhony07/pong-game.git
cd pong-game
```

Then open `index.html` in any modern browser. No server or install is needed.

To host it free on GitHub Pages: **Settings → Pages → Deploy from branch → `main` / root**.

## 🛠️ Configuration

Tweak the game feel by editing the constants in `index.html`:

| What | Where | Default |
|---|---|---|
| Points to win | `WIN` | `7` |
| Max ball speed | `MAX_SPEED` | `14` |
| CPU speed (higher = harder) | `max = 4.8 * dt` in `update()` | `4.8` |
| CPU mistake range (lower = harder) | `cpu.err` in `paddleHit()` | `70` |
| Player keyboard speed | `keyDir * 9 * dt` in `update()` | `9` |

## 🧠 How It Works

- **Fixed logical resolution**: the game runs in 800×500 units and is scaled to the screen, with pointer input converted back into game coordinates.
- **Delta-time loop**: `requestAnimationFrame` with a clamped time step prevents tunneling after tab switches or lag spikes.
- **Circle vs. rectangle collisions**: edges are handled correctly, and the ball is snapped out of walls and paddles to avoid sticking.
- **State machine**: `ready → playing ⇄ paused → over` keeps the game flow predictable.
- **Zero assets**: all visuals are drawn on canvas and all sounds are synthesized.

## 🌐 Browser Support

Works in current versions of Chrome, Edge, Firefox and Safari, on desktop and mobile.

## 🗺️ Roadmap

- [ ] Difficulty selector (Easy / Normal / Hard)
- [ ] Two-player local mode
- [ ] High-score persistence with `localStorage`
- [ ] Power-ups

## 🤝 Contributing

Contributions are welcome. Fork the repo, create a branch, and open a pull request.

## 📄 License

Released under the [MIT License](LICENSE).

## 👤 Author

**Andhony** · [@andhony07](https://github.com/andhony07)
