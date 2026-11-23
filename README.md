# VOIDBLOOM: Planetfall

A procedural 3D horror exploration game made for GitHub Pages.

## Play locally

The game uses JavaScript modules, so serve this folder with any static web server instead of opening `index.html` directly.

```powershell
python -m http.server 8080
```

Then open `http://localhost:8080`.

## Publish on GitHub Pages

1. Upload the contents of this folder to a GitHub repository.
2. Open **Settings → Pages**.
3. Set **Source** to “Deploy from a branch”, choose `main` and `/ (root)`, then save.

No build step or server is required. The 3D engine is included in the project; the optional web fonts fall back cleanly when offline.

## Multiplayer

Multiplayer is a separate peer-to-peer mode with no enforced player limit and no lobby timer:

1. One player selects **Multiplayer → Create Expedition**.
2. They share the six-character room code.
3. Other players choose **Multiplayer**, enter the code, and join.
4. The host chooses a destination and starts whenever the crew is ready. There is no lobby timer.

Player movement, shared objectives, monster positions, and the crew roster are synchronized. Multiplayer requires an internet connection because PeerJS's public signaling service introduces the browsers to each other. After that introduction, gameplay travels directly between players over WebRTC. Some highly restricted school, office, or carrier networks may block peer-to-peer connections. The game does not impose a player cap, although the host browser and connection will naturally determine how many simultaneous players perform smoothly.

## Controls

- **WASD** — Move
- **Mouse** — First-person look
- **Shift** — Sprint
- **F** — Toggle flashlight
- **E** — Interact
- **Esc** — Release the mouse

Complete all three field objectives, avoid the procedurally assembled creatures, and return to the lander alive.

## Included art

- Rocky Terrain PBR maps by Amal Kumar / Poly Haven — CC0
- Alien and Astronaut models by Quaternius — CC0

The terrain uses local albedo, OpenGL normal, roughness, and displacement maps. Models and textures are bundled with the site; no third-party art server is required during play.
