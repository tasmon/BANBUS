# 🚌 BAN Bus Simulation

A 3D driving game set in Bangladesh. It runs in desktop and mobile browsers and installs as a Progressive Web App (PWA).

**Developer:** Tasmon Islam

## Game modes
| Mode | What you do |
|---|---|
| **City · Passengers** | Pick up and drop off passengers at named stops. Earn fares, pay for diesel, avoid fines. |
| **City · Free drive** | Explore the city with traffic and rules but no passengers or deadlines. |
| **Highway** | Choose a destination city and drive the long intercity highway (distance estimated from real city locations). Speed cameras fine you; fuel stations are along the way. |
| **Endless drive** | Infinite highway with growing traffic. Score from distance and near misses; no fines, no fuel worries. |
| **Training** | Seven guided lessons: accelerate, steer, brake, drive through a ring, reverse, park, lights and horn. |
| **Demolition derby** | Ram rival cars in an arena. Hits, drifting and honking to taunt build the **road-rage** meter; at 100 you get 8 seconds of ×3 points and extra damage. Clear waves for bonuses and repairs. |

## Vehicles
City Coach, Express AC, Mini Bus, Double Decker and the new **CNG Auto-rickshaw** (tiny, quick, 3 passengers, CNG at ৳43). Pick any colour in the Garage (presets or a custom colour picker).

## Controls
| Action | Keyboard | Touch |
|---|---|---|
| Accelerate | `W` / `↑` | accelerator pedal |
| Brake, then reverse | `S` / `↓` (Space = brake only) | brake pedal, or gear `R` + accelerator |
| Steer | `A` `D` / `←` `→` | « » buttons |
| Horn | `H` | 📣 |
| Lights / hazards / gear / engine key | `L` / `Z` / `R` / `K` | ⋯ menu |
| Cockpit / camera distance | `C` / `V` | ⋯ menu |
| Find fuel / map / pause | `F` / `M` / `P` | ⋯ menu, ⏸ |

## Interface
The start screen shows only the six modes. Vehicle, colour and city are under **Garage**; the controls are under **How to play**. In game, the extra buttons are tucked behind ⋯, and the on-screen steering and pedals only appear on touch screens.

## Camera
A wide chase camera keeps the bus in view. It moves in when a building would block the view, trees are kept away from the road, and a faint silhouette of your vehicle shows through anything that gets in the way.

## Map accuracy
Each city's landmarks (Zindabazar, Farmgate, GEC Circle, Laboni Beach and so on) are placed at approximate real-world coordinates relative to each other, and rivers or the sea are on the correct side (for example the Padma south of Rajshahi, the Buriganga south of Dhaka and the Surma north of Sylhet). The coordinates were entered from memory, so treat them as approximate. The streets themselves are a simplified grid of wide boulevards, not a survey of the real road network. Importing OpenStreetMap data would be the way to get true street layouts.

## Economy
Diesel ৳105 per litre, CNG ৳43. Fares ৳20–150 per passenger by distance; intercity fares scale with kilometres. Fines (City and Highway): speeding ৳800–1,200 (60 km/h, 40 downtown, 80 on highways at cameras ৳1,500), red light ৳1,500, collision ৳2,000, off-road ৳500, pedestrian ৳15,000, towing ৳3,000. Fines are doubled near police. Fuel stations also repair the vehicle (৳80 per point).

## Run locally
```bash
python3 -m http.server 8080
```
Three.js (r128) loads from cdnjs on the first visit and is cached for offline play.

## Deploy on GitHub Pages
Push these files, enable **Settings → Pages** for the `main` branch, then open the URL. Chrome and Edge offer **Install**; on iOS use **Share → Add to Home Screen**. Add `#hq` to the URL to force full graphics on phones, or `#unlock` to open every city.

## Files
`index.html` (game), `manifest.webmanifest`, `sw.js`, `icon.svg`, `icon-192.png`, `icon-512.png`

## License
MIT © Tasmon Islam
