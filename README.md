# 🎲 Ludo Online

A single-file Ludo game — no build step, no server, no install.

**Play online:** https://prashantbhandari-code.github.io/ludo/

## How to play with friends
1. Open the link, tap **Play Online**.
2. Tap **Create Room** — you get a 4-letter code.
3. Friends open the same link, tap **Play Online → Join Room**, and enter the code.
4. Host taps **Start Game** when everyone's in.

## Modes
- **Online with room codes** — peer-to-peer WebRTC over public nostr relays (Trystero, bundled locally — no backend, no keys, no CDN), up to 4 players
- **Play vs Computer** — 3 bots that capture, escape, and finish
- **Pass & Play** — 4 humans on one device

Full Ludo rules: roll a 6 to leave the yard, extra turns on 6 / capture / finish,
three 6s skips your turn, safe ★ cells, blocks, exact roll to reach home.
If someone disconnects mid-game, a bot takes over their seat.

## Tech
One `index.html` plus a vendored `vendor/trystero.js` (~60 KB) — vanilla JS, WebRTC data channels with nostr-relay signaling (Trystero), Tone.js for sound.
`test.html` is a self-contained E2E harness: open it and two game instances auto-join the same room and play each other.
Host it anywhere static (GitHub Pages works) or just open the file locally.
