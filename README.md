# Google Map Quest

A tiny single-file browser game. You're a delivery driver: a **📦 pickup** and **two 🏠 houses**
sit on a city grid. **Press the pickup, then drag your finger/mouse along the roads** through both
houses to deliver. The route you trace *is* your distance — the aim is the **shortest route possible**.

- Your traced distance and the **shortest possible** distance are shown live.
- Deliver to both houses, then you're scored: ⭐⭐⭐ for the optimal route, fewer stars the more
  you wander.
- **New Map** for a fresh layout, **Reset** to retry the same one.

## Play

Open **`index.html`** in any modern browser. No build, no dependencies, no server required.
Works with mouse (drag) and touch.

## How it works

`index.html` is fully self-contained (HTML + CSS + vanilla JS, Canvas 2D):

- A grid road graph; the **shortest possible** delivery is the better of the two visit orders,
  computed with Dijkstra.
- As you drag, the truck steps along the roads toward your cursor one block at a time — it can't
  teleport, so wandering down the wrong street adds real distance.
- Score = your traced distance vs the optimal distance.

🤖 Built with [Claude Code](https://claude.com/claude-code)
