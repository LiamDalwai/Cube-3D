# Card Wardens (Demo)

An original, fully customizable deck-building card battler in a **single HTML file** — no installs, no build step. Just open `CardWardens.html` in any browser and play.

> Inspired by the deck-builder genre (energy each turn, a hand of cards, telegraphed enemy intents, card rewards after every fight) — with all-original characters, cards and enemies that are yours to change.

## Play it

Open `CardWardens.html` in a browser. That's it — works on desktop and phones (touch controls: tap a card to pick it up, tap again or tap an enemy to play it).

To get a shareable URL you can play from any phone, enable GitHub Pages for this repo (Settings → Pages → Deploy from a branch → `main`), then play at `https://liamdalwai.github.io/Cube-3D/CardWardens.html`.

**Demo content:** 3 playable Wardens, 33 cards, Level 1 — *The Whispering Woods* (3 battles + a boss). Levels 2 and 3 are shown on the map as coming soon; we're building them one at a time.

## The Wardens

| Warden | Style |
|---|---|
| 🦁 **Kaela**, the Flame Warden | Aggressive — big damage, Burn, Strength |
| 🦉 **Thorn**, the Grove Warden | Defensive — Poison, Block, healing and Regen |
| 🐉 **Zyra**, the Storm Warden | Tricky — card draw, extra energy, multi-hits |

## Make it your own

Everything lives in the **`GAME DATA`** section near the top of the `<script>` in `CardWardens.html`. No engine knowledge needed:

- **`CONFIG`** — game title, energy per turn, hand size, reward rules, healing amounts.
- **`CARDS`** — every card is one line. Effects are plain fields: `dmg`, `hits`, `aoe`, `block`, `heal`, `draw`, `energy`, `enemyStatus`, `selfStatus`, `exhaust`. Mix them however you like.
- **`HEROES`** — name, emoji portrait, HP, starter deck, and the card pool offered as rewards. Add a fourth hero by copying a block; the select screen updates automatically.
- **`ENEMIES`** — HP, moves (attack / block / buff / debuff) and the `pattern` they loop through.
- **`LEVELS`** — each level is just a list of battles, and each battle a list of enemy ids. To add Level 2, copy the Level 1 block, fill in new enemies, and set `locked: false` — the map updates by itself.

Status effects available out of the box: 💪 Strength, 🌀 Weak, 💔 Vulnerable, ☠️ Poison, 🔥 Burn, 💚 Regen.

## Also in this repo

- `Cube.html` — a reflective burgundy 3D cube (Three.js).

## Roadmap

- [x] Level 1 — The Whispering Woods
- [ ] Level 2 — The Ember Caverns
- [ ] Level 3 — The Skyspire Peaks
- [ ] Relics / artifacts, card upgrades, save progress
