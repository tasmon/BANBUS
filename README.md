# 🚌 BAN Bus Simulation

A 3D bus driving simulation set in Bangladesh. Runs in desktop and mobile browsers and installs as a Progressive Web App (PWA).

**Developer:** Tasmon Islam

## Features
- **3D driving** with a chase camera and a cockpit view (`C`), built with Three.js
- **6 cities:** Sylhet, Rajshahi, Cox's Bazar, Khulna, Chattogram and Dhaka. Each has its own stops (English and Bangla), traffic density, weather, fare level, skyline and water (sea, river or port). Bigger cities unlock as your career earnings grow
- **Realistic economy in taka (৳):** diesel at ৳105 per litre, distance-based fares (৳20–70 per passenger), realistic fines, and repairs at fuel stations
- **4 bus models:** Local Bus, Express AC, Mini Bus, Double Decker
- **Bangladesh details:** left-hand traffic, rickshaws, CNG autos, trucks, mosques, bazaars, zebra crossings, traffic police and patrol cars
- **Weather and day/night:** clear, monsoon rain, fog or smog, with headlights at night
- **Audio:** engine, horn, crash, cash, rain and ambient city sounds (no asset files)
- **Offline play** after the first load, installable PWA, best score saved per city

## Controls
| Action | Desktop | Mobile |
|---|---|---|
| Accelerate | `↑` / `W` | ▲ |
| Brake / reverse | `↓` / `S` / `Space` | ■ |
| Steer | `←` `→` / `A` `D` | ◀ ▶ |
| Horn | `H` | 📣 |
| Camera / Map / Pause | `C` / `M` / `P` | 🎥 / 🗺 / ⏸ |

## Economy and rules
| Item | Amount |
|---|---|
| Starting cash | ৳15,000 |
| Diesel | ৳105 per litre |
| Repairs (at fuel stations) | ৳80 per health point |
| Fare | ৳20–70 per passenger by distance, plus a time bonus; late trips earn half |
| Speeding (50 km/h, 30 km/h downtown) | ৳800 / ৳1,200 |
| Running a red light | ৳1,500 |
| Collision | ৳2,000 |
| Driving off-road | ৳500 |
| Hitting a pedestrian | ৳15,000 |
| Towing (empty tank) | ৳3,000 |

Fines are **doubled** near traffic police (except towing). The game ends if the bus is wrecked or your balance falls below −৳5,000.

## City unlocks
Sylhet and Rajshahi are open from the start. Cox's Bazar and Khulna unlock at ৳3,000 career earnings, Chattogram at ৳8,000 and Dhaka at ৳15,000. Add `#unlock` to the URL to open all cities.

## Run locally
```bash
python3 -m http.server 8080
# open http://localhost:8080
```
Three.js (r128) loads from cdnjs on the first visit and is cached for offline play.

## Deploy on GitHub Pages
1. Push these files to a repository.
2. **Settings → Pages**, choose the `main` branch and `/ (root)`.
3. Open the URL. Chrome/Edge show **Install**; on iOS use **Share → Add to Home Screen**.

## Structure
```
index.html            game, UI, audio and 3D renderer
manifest.webmanifest  PWA manifest
sw.js                 offline cache
icon.svg, icon-*.png  app icons
```

## License
MIT © Tasmon Islam
