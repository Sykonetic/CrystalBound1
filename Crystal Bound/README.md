# Crystalbound ARPG (FFV x D&D) – Modular Starter

This is a **lightweight, modular** version of the browser ARPG so we can keep shipping features without hitting editor size limits.

## Run locally
Just open `index.html` in a modern browser. No build step needed.

## Multiplayer
- **Same-computer tabs:** Works out of the box via `BroadcastChannel`. Open two tabs and join the same room name.
- **Over the Internet:** Run the tiny WebSocket relay:
  ```bash
  npm init -y
  npm i ws
  node server/relay.js
  ```
  Then in the game UI, paste `ws://YOUR_IP:8080` and click **Start/Join**.

## GitHub Pages (free hosting)
1. Create a GitHub repo (e.g., `crystalbound-arpg`).
2. Upload **all files** from this folder.
3. In the repo: **Settings → Pages →** set Branch to `main` (or `master`), folder `/root`, save.
4. After a minute, your game will be live at `https://<your-username>.github.io/crystalbound-arpg/`.
5. Share the link with friends.

## Features in this starter
- 24×24 tile look, free movement, WASD + Shift (run), **Space = dodge (i-frames)**, **J = attack**.
- Boss **telegraphs** (circle/line) that fire after ~1s. Tough but fair.
- **Keybind remapping** UI with persistent localStorage saves.
- Basic multiplayer sync (positions) via BroadcastChannel or WS relay.

## Roadmap (we can add next)
- Class skills & unlocks per level, shops/quests, inventories, drops.
- Enemy archetypes (ranged/casters), better VFX, damage numbers.
- Authoritative server (optional) if you want real co-op combat.

## Troubleshooting
- If nothing appears: check the **console** for errors. Any missing CORS or path issues usually mean files weren’t uploaded to the right place.
- If multiplayer over the internet isn’t working, make sure port **8080** is open on your router or use a VPS. 

Enjoy!
