# Rocket-duo-Nasa-Space-X-challenge

**Rocket Workshop** is a two-player cooperative browser game about launching a real satellite. One player builds and flies the rocket and can't see any of the data. The other has all the data and can't touch the controls. You only reach orbit by talking to each other.

The game is also meant to teach. Each step follows a real launch campaign: signing a contract, designing the vehicle, picking a weather window, the go/no-go poll, handling problems in flight, and putting the payload precisely into its target orbit.

---

## The story

It's 2031. You and your partner have just started **Rocket Workshop**, a two-person launch company with one pad on the coast and one week of rented pad time. Three customers have sent contracts. Each one has a different payload, target orbit, budget and deadline.

**You only need to fly one of them.** Put any one payload into its target orbit and Rocket Workshop has its first successful launch.

---

## How to play

### Two players, one screen

| | Left · **Engineer** | Right · **Manual reader** |
|---|---|---|
| Input | Keyboard only | Mouse only |
| Sees | The rocket, the parts (by colour and letter), the weather grid, the flight gauges, the warning codes | The **Manual**: mission specs, parts catalogue, ready-made designs, weather rules, budget rules, emergency procedures |
| Can't | Look anything up | Touch the controls |

The Engineer describes what's on screen ("red light, code W-21, gauge ⑧ is glowing"). The Manual reader looks it up and gives exact instructions ("Stage 1: engine B, count 1, tank T3, one tank").

### The six steps

| Step | What you do | Real-world link |
|---|---|---|
| **1 Mission** | Pick one of three contracts | A launch contract sets the payload, orbit and schedule |
| **2 Assembly** | Stack stages (engine type, engine count, tank type, tank count) and run **INSPECT** | The rocket equation, staging, thrust-to-weight |
| **3 Launch plan** | Choose a day and time slot that passes all four weather rules before the deadline | Launch weather criteria and scrubs |
| **4 Launch prep** | 10 seconds to get ready, then **START LAUNCH** | The go/no-go poll |
| **5 Flight** | Handle in-flight warnings as a team | Flight controllers and emergency procedures |
| **6 Result** | Orbit insertion and debrief | Post-flight review |

A short briefing pops up the first time you reach each step. A 4-page tutorial opens on launch and can be reopened any time from the **? Tutorial** button.

### Controls

**Engineer (keyboard)**
- `W` `S` / `↑` `↓`: move up/down or change a value
- `A` `D` / `←` `→`: move left/right (in flight: small pitch nudge, which the autopilot corrects)
- `Enter`: select / edit / confirm

**Manual reader (mouse)**
- **Contents**, **◀ ▶** to turn pages, **⚠ EMERGENCY** for the emergency codes page, **? Tutorial** to reopen the tutorial

---

## The missions

Target orbits are based on real missions:

| Code | Mission | Payload | Target orbit | Budget | Deadline | Real-world basis |
|---|---|---|---|---|---|---|
| **M-1** | Dawn-1 | 4 × 1U university CubeSats | 525 km circular, sun-synchronous | 80 | Day 7 | SpaceX Transporter rideshares deploy CubeSats at about 510–525 km |
| **M-2** | Wingspan | 3U tech-demo satellite with a new folding solar panel | 590 km circular, sun-synchronous | 130 | Day 6 | Rideshares often drop a second group of satellites at about 590–600 km |
| **M-3** | Supply Line | Supply capsule for the International Space Station | 415 km circular (ISS orbit) | 85 | Day 5 | The ISS orbits at about 412 × 420 km |

A mission succeeds when the payload is inserted **within ± 15 km of its target orbit** and its antenna deploys.

---

## Things to watch

### Budget
The budget doesn't only pay for parts:

| Cost | Affected by |
|---|---|
| Hardware | Engines, tanks, payload integration |
| Propellant & loading | **Fuel tank design**: more fuel costs more |
| Pad standby | **Launch date**: every day you wait costs money |
| Scrub | **Weather + tank design**: a launch called off for weather costs more the bigger your tanks are (fuel has to be drained and reloaded) |
| Marginal weather | **Weather**: launching in borderline wind costs extra |

Launching after the mission's **deadline** fails the mission, however good the rocket is.

### Inspection codes
| Code | Meaning |
|---|---|
| E-01 | Stage 1 thrust too low to leave the pad |
| E-02 | Not enough total Δv for the target orbit |
| E-03 | Over budget |
| E-04 | Upper stage too weak (thrust-to-weight under 0.9) |
| E-05 | Upper stage too small (under 3,700 m/s of Δv on its own) |

### In-flight warnings
Four warnings can happen during flight: **W-12** (wind shear / dynamic pressure), **W-21** (engine overheating), **W-30** (stage separation fault) and **W-40** (antenna not deployed). When one appears, the flight pauses and the team has **10 seconds**. The Engineer reads out the code, light colour and highlighted gauge, and the Manual reader finds the keys to press. A wrong key shows why it was wrong and clears the input, so you can try again while the timer runs.

The key sequences are only in the in-game Manual, so the Manual reader has to look them up.

---

## How the rocket reaches orbit

The flight computer follows the same profile real rideshare launches use:

1. **Ascent burn:** stage 1, then the upper stage, burn until apogee reaches the target altitude (SECO-1). If stage 1 alone is powerful enough, it cuts off early and separates (early MECO).
2. **Coast:** engine off; the rocket glides up to apogee (time is sped up).
3. **Circularization burn:** at apogee the upper stage restarts and burns sideways until the orbit is round, throttling down at the end for precision.
4. **Orbit insertion:** engine cutoff, payload separation, antenna check, then a 10-second success screen showing the satellite in its orbit before returning to mission select.

The simulation uses real orbital mechanics (gravity, an exponential atmosphere, drag, sea-level vs. vacuum engine efficiency and Kepler orbits). Engine and tank stats are made-up teaching values.

---

## Running the game

The whole game is one self-contained HTML file. There's nothing to build or install.

1. Download `rocket-duo.html`.
2. Open it in a modern desktop browser (Chrome, Edge, Firefox or Safari).
3. Play full screen on a 16:9 display (designed for 1920 × 1080), with one keyboard and one mouse shared by two people sitting side by side.

An internet connection is only needed to load web fonts. The game still works without one.

---

## Sources

| Source | Used in the game for |
|---|---|
| NASA, [Artemis II Weather Criteria](https://www.nasa.gov/artemis-ii-weather-criteria) | Peak wind limit (29 kt), temperature limits (49–94 °F) |
| NASA, [Falcon 9 Crew Dragon Launch Weather Criteria](https://www.nasa.gov/wp-content/uploads/2021/07/falcon9_crewdragon_launch_weather_criteria_fact_sheet.pdf) (fact sheet) | Lightning and cumulus-cloud limits (10 nautical miles) |
| NASA Space Station Blog, [NASA, SpaceX Complete Dragon Space Station Reboost](https://www.nasa.gov/blogs/spacestation/2025/09/03/nasa-spacex-complete-dragon-space-station-reboost/) (Sept. 3, 2025) | ISS orbit, 260.9 × 256.3 miles (about 420 × 412 km): M-3 target of 415 km |
| NASASpaceflight, [SpaceX launches Transporter-11](https://www.nasaspaceflight.com/2024/08/transporter-11/) (Aug. 2024) | Rideshare deployment orbits of about 510–520 km and 590–600 km (M-1 and M-2 targets); circularization burn before deployment |
| Cal Poly, [CubeSat Design Specification Rev. 14.1](https://www.nasa.gov/wp-content/uploads/2018/01/cubesatdesignspecificationrev14_12022-02-09.pdf) (2022) | CubeSat mass limits (1U 2 kg, 3U 6 kg); 30-minute wait before deploying antennas (§2.4.4); 45-minute wait before transmitting (§2.4.5) |
| NASA CubeSat Launch Initiative, [CubeSat 101](https://www.nasa.gov/wp-content/uploads/2017/03/nasa_csli_cubesat_101_508.pdf) (Oct. 2017) | Burn wires and deployable antennas (W-40) |

Engines, tanks, prices, events and scoring are game values for teaching. Weather limits use the strictest end of each real range: Artemis II's peak-wind limit runs from 29 to 39 knots depending on height, and its cold limit from 38 to 49 °F depending on wind and humidity.

---

## Disclaimer

This is an independent educational project. It is not affiliated with, endorsed by, or an official product of NASA or SpaceX.
