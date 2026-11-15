# Rocket Duo · Data Sources

Every real-world fact or number used in **Rocket Duo** (`rocket-duo.html`), with where it appears in the game and the link it comes from.

**Legend**

| Mark | Meaning |
|---|---|
| ✅ | Official NASA source (or a NASA-hosted standard), checked against the page |
| 📰 | Non-official source (news, reference site, enthusiast blog). Useful context, **not** NASA data |
| ⚠️ | Claim in the game that still needs a source |
| 🎮 | Value made up for the game (teaching simplification) |

> Rocket Duo is not an official NASA product. NASA logos and mission insignia are not used.

---

## 1. Official NASA sources (NASA Data)

| What the game uses | Where in the game | Source | Status |
|---|---|---|---|
| CubeSat maximum mass: 1U 2.00 kg, 3U 6.00 kg, 6U 12.00 kg | Manual › Part 1 Missions | CubeSat Design Specification Rev 14.1 (Feb 2022), hosted by NASA CSLI · https://www.nasa.gov/wp-content/uploads/2018/01/cubesatdesignspecificationrev14_12022-02-09.pdf | ✅ |
| CubeSats may not transmit radio signals for the first 45 minutes after deployment | Manual › W-40 Antenna not deployed | Same document as above (Section 2.4.5) | ✅ |
| Deployable parts should use two burn wires | Manual › W-40 Antenna not deployed | NASA CubeSat Launch Initiative, *CubeSat 101* (2017) · https://www.nasa.gov/wp-content/uploads/2017/03/nasa_csli_cubesat_101_508.pdf | ✅ |
| Launch weather: peak wind at liftoff (29 kt limit), temperature limits (49–94 °F) | Weather grid ① ② · Manual › Part 5 Weather | NASA, *Artemis II Weather Criteria* · https://www.nasa.gov/artemis-ii-weather-criteria/ | ✅ |
| Launch weather: no launch with lightning or freezing-top cumulus clouds within 10 nmi | Weather grid ③ ④ · Manual › Part 5 Weather | NASA, *Falcon 9 / Crew Dragon Launch Weather Criteria* fact sheet · https://www.nasa.gov/wp-content/uploads/2021/07/falcon9_crewdragon_launch_weather_criteria_fact_sheet.pdf | ✅ |
| ISS orbit about 412 × 420 km | Mission M-3 · Manual › Part 1 Missions | NASA Space Station Blog, *NASA, SpaceX Complete Dragon Space Station Reboost* (3 Sept 2025): orbit of 260.9 × 256.3 miles (≈ 420 × 412 km) · https://www.nasa.gov/blogs/spacestation/2025/09/03/nasa-spacex-complete-dragon-space-station-reboost/ | ✅ |
| Background reference (named on the Sources page; no numbers from it are used in the game yet) | Manual › Glossary & sources | NASA, *State-of-the-Art of Small Spacecraft Technology* · https://www.nasa.gov/smallsat-institute/sst-soa/ | ✅ |

**Simplifications:** real wind and temperature limits change with measurement height, wind and humidity; the game uses one value for each. Real lightning and cloud rules have exceptions that the game leaves out.

---

## 2. Non-official sources (context only)

| What the game uses | Where in the game | Source | Status |
|---|---|---|---|
| Rideshare missions deploy CubeSats into sun-synchronous orbits of about 510–525 km | Mission M-1 real-world note | eoPortal, *Transporter-5* (SSO, 525 km) · https://www.eoportal.org/other-space-activities/transporter-5 | 📰 |
| Same, plus a second deployment group around 590 km | Missions M-1 and M-2 real-world notes | NASASpaceflight, *SpaceX Transporter-12 launches more than 100 satellites* (510–520 km and 590–620 km) · https://www.nasaspaceflight.com/2025/01/transporter-12/ | 📰 |
| Second deployment group around 590–600 km | Mission M-2 real-world note | Everyday Astronaut, *Transporter-10* (second deployment at ~590 km) · https://everydayastronaut.com/transporter-10-falcon-9-block-5/ | 📰 |
| Transporter-9: the second stage first entered a 207 × 537 km transfer orbit, coasted, then circularized | Manual › Part 6 Flight profile | Personal enthusiast blog · https://from-that-neighborhood-rocket-fan.blogspot.com/2023/11/spacex-transporter-9.html | 📰 ⚠️ weak source; the blog gives a 42-minute coast, the game says "almost an hour" |
| Failed antenna / solar panel deployment is a common reason small satellites fail | Manual › W-40 real-world note | *Improving Mission Success of CubeSats* (Aerospace Corporation report TOR-2017-01689, 2017; hosted on nasa.gov, not written by NASA) · https://www.nasa.gov/wp-content/uploads/2017/03/improving_mission_success_of_cubesats_-_tor-2017-01689.pdf | 📰 (not cited in the game yet) |


---

## 3. Game values 🎮

Made up for teaching and labelled as such in the Manual:

- Engines A–D (thrust, Isp, mass, price) and fuel tanks T1–T3
- Mission budgets, deadlines, payload masses, and Δv requirements
- Budget rates: pad standby, propellant & loading, scrub cost, marginal-wind surcharge
- Flight warnings W-12, W-21, W-30, W-40 and their key sequences, timers, and consequences
- Scores and the ± 15 km orbit-insertion tolerance

---

*Last updated: 14 Nov 2026.*
