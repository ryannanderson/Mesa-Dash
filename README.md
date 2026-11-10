# Mesa Dash

A 3D kart racer that runs in the browser. Three laps through red-rock desert against five rivals, with drifting, boost pads, and items.

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

## Multiplayer

The "Racing together" lobby uses a live-room feature that only exists when the game is opened as a Claude artifact. On GitHub Pages or any other host that feature is absent, so the lobby stays hidden and the game is single-player. Racing with friends from your own hosting would need a small relay server (for example a WebSocket server), which a static host such as GitHub Pages cannot run.
