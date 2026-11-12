# Mesa Dash

A 3D kart racer that runs in the browser. Three laps against eleven rivals, with twelve racers to choose from, with drifting, boost pads, and items.

There are three tracks:

- **Red Rock Run**: a desert circuit through red-rock buttes.
- **Geyser Meadows**: a wide dirt road through a mountain meadow, where bison wander across the track and geysers erupt under it. Both spin you out.
- **Acadia Coast**: a sunrise loop through fall woods and under stone arch bridges, out across a sandbar to an island and back. The tide floods the sandbars and slows you down, and Thunder Hole throws spray across the ocean side of the road.

The whole game is one file, `index.html`. It loads three.js (r128) from cdnjs and two fonts from Google Fonts; there is no build step.

## Play locally

Open `index.html` in a browser, or serve the folder:

```
npx serve .
```

## Controls

| Action | Keyboard | Touch |
| --- | --- | --- |
| Drive | Arrow keys or WASD | Accelerates on its own; ◀ ▶ to steer |
| Drift | Hold Space while turning, release for a boost | Drift button |
| Use item | E | Item button |

Items: 🌶️ speed burst, ⚡ zapper that chases the racer ahead, 🫧 goo dropped behind you.

## Host on GitHub Pages

1. Push this folder to a GitHub repository.
2. In the repository, open Settings, then Pages.
3. Under "Build and deployment", choose "Deploy from a branch", pick `main` and `/ (root)`, and save.
4. After a minute the game is live at `https://<your-username>.github.io/<repo-name>/`.

## LAN party mode

Split-screen on one screen for up to four players, each using a phone as the controller. Computer rivals fill the rest of the 12-kart grid.

1. Open the game on a laptop and show it on the TV (an HDMI cable has less delay than casting).
2. On the start screen choose "Host on this screen". A QR code and a four-letter party code appear.
3. On each phone, scan the code (or open the address shown), enter a name, pick a racer, and tap Done.
4. Pick a track on the laptop and start the race.

The phones and the laptop find each other through the free public PeerJS pairing service, so every device needs an internet connection. The game loads PeerJS and a QR code library from jsDelivr only when this mode is used.

## Online multiplayer

The "Racing together" lobby uses a live-room feature that only exists when the game is opened as a Claude artifact. On GitHub Pages or any other host that feature is absent, so the lobby stays hidden. Racing with friends on their own screens from your own hosting would need a small relay server (for example a WebSocket server), which a static host such as GitHub Pages cannot run.
