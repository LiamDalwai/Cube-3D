# Card Wardens (Demo)

An original, fully customizable deck-building card battler in a **single HTML file** — no installs, no build step. Just open `CardWardens.html` in any browser and play.

> Inspired by the deck-builder genre (energy each turn, a hand of cards, telegraphed enemy intents, card rewards after every fight) — with all-original characters, cards and enemies that are yours to change.

## Play it

Open `CardWardens.html` in a browser. That's it — works on desktop and phones (touch controls: tap a card to pick it up, tap again or tap an enemy to play it).

To get a shareable URL you can play from any phone, enable GitHub Pages for this repo (Settings → Pages → Deploy from a branch → `main`), then play at `https://liamdalwai.github.io/Cube-3D/CardWardens.html`.

**Demo content:** 1 playable Warden (Kaela — Thorn and Zyra show as locked, coming soon), 33 cards, and two full chapters in one continuous run:

1. **Chapter 1: The Slime Meadows** — 5 zones of sunny hills and mischievous slimes (Gloop, Bloop, Zap, Blush) ending at King Gloopius on the Gel Throne
2. **Chapter 2: The Whispering Woods** — 4 zones of misty forest (Gloomcaps, the Bog Croaker, Thistle Imps, the Bramble Beast) ending at the Hollow King

Areas 3 and 4 (*Ember Caverns*, *Skyspire Peaks*) show on the map as coming soon — we're building them one at a time.

**UI/UX:** built like a mobile card-battler — your full-body hero stands on the battlefield facing the enemies, intents appear as speech bubbles over enemies' heads, your hand fans out in an arc at the bottom, with an energy gem, draw/discard piles and a round End Turn button around it; between fights you walk a winding node path across the chapter map and collect gold.

**Graphics:** every character and enemy is an original hand-drawn vector (SVG) sprite — infinitely sharp at any resolution — with per-area animated backdrops (rolling meadow hills with drifting bubbles, dark forest with blinking fireflies), idle squish/bob/float animations, attack lunges, hit sparks, floating damage numbers and dealt-card animations. Swap any sprite in the `ART` library for your own SVG, or delete one and the game falls back to that character's emoji.

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

- [x] Area 1 — The Slime Meadows (5 zones)
- [x] Area 2 — The Whispering Woods (4 zones)
- [ ] Area 3 — The Ember Caverns
- [ ] Area 4 — The Skyspire Peaks
- [ ] Relics / artifacts, card upgrades, save progress
