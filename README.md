# 🚌 BAN Bus Simulation

A top-down bus driving simulation that runs in any modern desktop or mobile browser and installs as a Progressive Web App (PWA).

**Developer:** Tasmon Islam

## Features
- **Bangladesh setting:** left-hand traffic, rickshaws, CNG auto-rickshaws, trucks, mosques, bazaars, Bangla place names, taka (৳) currency and a local ambient soundscape (rickshaw bells, honks, crows by day, crickets by night, monsoon rain)
- **Traffic police (পুলিশ):** officers at junctions and patrol cars; any fine near them is doubled
- **Weather:** clear, monsoon rain (slippery, longer braking) and fog (low visibility)
- **Day/night cycle:** headlights and street lamps at night, with a clock in the HUD
- **4 bus models:** Local Bus, Express AC, Mini Bus and Double Decker, each with different speed, tank, health and fare rate
- City map of 8×8 streets with buildings, parks, sidewalks, traffic lights and a live minimap plus full map (`M`)
- Left-hand traffic with AI cars that turn, queue and obey red lights
- Pedestrians crossing at zebra crossings when the light allows
- Missions: pick up passengers at named stops (Zindabazar, Ambarkhana, Subid Bazar…) and deliver them before the timer runs out
- Fuel system with refuelling stations (**৳3 per litre**) and a towing fee if you run dry
- Fines: speeding, red lights, collisions, off-road driving, hitting pedestrians
- Levels that add heavier traffic and tighter deadlines
- Procedural audio: engine, horn, crash, cash and ambient music (no asset files)
- Offline play with a service worker, install prompt, best score saved locally

## Controls
| Action | Desktop | Mobile |
|---|---|---|
| Accelerate | `↑` / `W` | ▲ |
| Brake / reverse | `↓` / `S` / `Space` | ■ |
| Steer | `←` `→` / `A` `D` | ◀ ▶ |
| Horn | `H` | 📣 |
| Map / Pause | `M` / `P` | 🗺 / ⏸ |

## Rules
| Event | Cost |
|---|---|
| Speeding (50 km/h, 30 km/h downtown) | ৳40–৳60 |
| Running a red light | ৳75 |
| Collision | ৳100 |
| Off-road driving | ৳30 |
| Hitting a pedestrian | ৳300 |
| Towing (empty tank) | ৳250 |

All fines except towing are **doubled** near traffic police.

Fares pay ৳12 per passenger plus a time bonus; late trips earn half fare. The game ends if the bus is wrecked or your balance falls below −৳300.

## Run locally
Service workers need HTTP, so serve the folder instead of opening the file directly:
```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Deploy on GitHub Pages
1. Push these files to a repository.
2. Go to **Settings → Pages**, select the `main` branch and `/ (root)`.
3. Open the published URL. Chrome/Edge show an **Install** button; on iOS use **Share → Add to Home Screen**.

## Project structure
```
index.html            game, UI and audio (single file)
manifest.webmanifest  PWA manifest
sw.js                 offline cache
icon.svg, icon-*.png  app icons
```

## License
MIT © Tasmon Islam
