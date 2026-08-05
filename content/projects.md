# Projects

## ricane-plugins — JUCE Audio Plugin Bank
**Since July 2026** — [github.com/akaRicane/ricane-plugins](https://github.com/akaRicane/ricane-plugins) (public, MIT)

A personal bank of audio plugins built with JUCE 8, written to learn plugin development from the
ground up — one self-contained plugin at a time, clarity over cleverness, with the theory written
down alongside the code.

- **GainPlugin** — decibel volume control, click-free via `juce::dsp::Gain` smoothing
- **PannerPlugin** — mono/stereo in → stereo out, −6 dB pan law, per-sample smoothing
- **DelayPlugin** — first time-based plugin: ring buffer, interpolated reads, tape-style time
  smoothing, dry/wet
- Each plugin builds in isolation (own `CMakeLists.txt`, no cross-dependencies); JUCE 8.0.13 and
  pluginval are pinned git submodules
- `utils/` scripts for build, open, and host validation; documentation split into setup, DSP
  theory (`knowledge/`), per-plugin pages, and tooling
- Known gaps and next steps tracked in a roadmap chosen by *what it teaches*, not by product value

**Tech:** C++, JUCE 8, CMake, pluginval, clang-format, DSP

---

## Paris Métro Guessr
**Since July 2026** — [github.com/akaRicane/paris-metro-guessr](https://github.com/akaRicane/paris-metro-guessr) (public) · live at [lutece-guessr.ricane.dev](https://lutece-guessr.ricane.dev)

A station is named, you pin it on the map, the closer you land the more you score. Vanilla JS and
Leaflet, no framework and no build step.

- Scoring decays exponentially with the miss (`5000·e^(−km/2.5)`), tuned to Paris scale
- Five station pools (Paris intra muros, métro, RER-only, pick-your-lines, everything), four
  difficulty/time settings, and a deathmatch mode with a draining life bar
- Data generated from [Île-de-France Mobilités](https://data.iledefrance-mobilites.fr) open data:
  536 stations (merged on interchange, with the genuinely-ambiguous names disambiguated), 660 track
  segments simplified by Douglas-Peucker from 370 kB to 82 kB, and the IGN Paris commune contour
  reduced 532 → 164 points while provably preserving the in/out verdict for every station
- The real line geometry is drawn on the reveal in official IDFM colours — the point where it stops
  being a quiz and starts teaching the map
- Bilingual EN/FR (keys, not sentences, in the rules layer), label-free basemap so the tiles never
  leak the answer, wall-clock timers so a backgrounded tab can't cheat
- Self-hosted on my own Coolify estate, with Umami analytics

**Tech:** JavaScript (vanilla), Leaflet, Python (data pipeline), HTML/CSS, geospatial processing

---

## Personal Infrastructure — `admin`
**Since August 2026** — private, local

Operating repo for the web infrastructure I own and run: the day-to-day counterpart to `infraweb`'s
provisioning. One folder per administered system.

- Token-safe Coolify CLI wrapper (never prints or argv-passes the token; writes require `--yes`)
- Coolify MCP server wired into Claude Code
- Full monitoring stack deployed as compose stacks: Prometheus + blackbox + Loki + Grafana, with
  node-exporter/cadvisor/alloy agents on all three nodes, remote nodes reaching the master over
  WireGuard, nothing but Grafana publicly exposed
- Alerting rules including domain-expiry monitoring
- Umami for website analytics
- Pre-commit secret scanner (gitleaks-aware); committed docs carry names and public domains only,
  with IPs and UUIDs confined to a gitignored inventory
- Estate: 3 nodes, 8 projects, 7 applications, 9 services, 1 database

**Tech:** Docker Compose, Coolify, Prometheus, Grafana, Loki, Alloy, WireGuard, Bash, Ansible, MCP

---

## LBSS.art & ASTAR
**2020 – 2025 (on pause since 2026)**

### ASTAR
Live creative coding software — built between 2021 and 2024. Used as a creative medium
for live VJing performance and stage design via creative coding.

- Real-time inference of code variables
- Control via MIDI, OSC, UDP
- Visual script development for VJing and events
- Used on stage in France and Belgium

**Tech:** JavaScript, HTML/CSS, Solid.js, Electron.js, three.js, p5.js, shaders,
WebGL/OpenGL, Audio React, MIDI, DMX, OSC, UDP

### lbss.art website
On pause since 2026 — website inactive. Cloud infrastructure, automated deployment.

**Tech:** Adonis.js, JavaScript/TypeScript, HTML/CSS, React.js, Tailwind,
DNS, VPS, Coolify, Terraform, Ansible, Docker

---

## flagada.art
**Since 2020** — Active project, web development & hosting.

**Tech:** Same stack as lbss.art

---

## artistes-assistance.com
**Since 2025**

Takeover and complete redesign of an abandoned WordPress site. Fixed broken features.
Hosting and maintenance. Added a custom admin dashboard (CMS-like) tailored to the
client's needs.

**Tech:** Adonis.js, TypeScript, HTML/CSS, React.js, PostgreSQL, Authentication

---

## Music Production — Mixing & Mastering
**2010 – present**

Mixing and mastering for own projects and external clients. Work spans singles, EPs, and double singles across various genres projects and artists.

| Artist | Project | Format | Date | Mix | Master | Link |
|--------|---------|--------|------|-----|--------|------|
| M.Toe | La Dose | Single | 23/04/2023 | ❌ | ✅ | [Spotify](https://open.spotify.com/album/1ZbTNfaFJWnhzKeuWRSaOI?si=ioNlbTT7QO6hwK8MPxDoWA) |
| M.Toe | La Gare | Single | 23/04/2023 | ❌ | ✅ | [Spotify](https://open.spotify.com/track/3G2uCFipBBeWMfUNePgOfk?si=c03ac50713344bde) |
| M.Toe | Plantés | Single | 23/06/2024 | ❌ | ✅ | [Spotify](https://open.spotify.com/album/4CRjdWd1X0v2D0QMYGAWte?si=CgDI_QvYQJuYuhRcf8Bemw) |
| Jaigh | For The Homies | EP (4 tracks) | 11/10/2024 | ❌ | ✅ | [Spotify](https://open.spotify.com/album/7G3zSaMrRzBFGd8LnN7OE8?si=hZxE0HDjQcSAse_9SPrAtQ) |
| M.Toe | Seulement danser | Single double | 21/11/2024 | ❌ | ✅ | [SoundCloud](https://soundcloud.com/user-457025761/seulement-danser-original-mix) |
| M.Toe | L'Agonie | Single | 21/06/2025 | ❌ | ✅ | [Spotify](https://open.spotify.com/track/1A4i3BmZzwUoyb7TxPLB6R?si=eaebb5e0154f4e2f) |
| Le Wanski | Odyssée | Single double | 10/11/2025 | ❌ | ✅ | [Spotify](https://open.spotify.com/album/6RhNvPYOqa9qyH0l4VI0UP?si=GSfXu884Tfm6pkIpRFjHnQ) |

---

## TG Animation — Electronic Control Box Integration
**September 2018 – November 2018**

Integration of a centralized electronic control box prototype into small tourist trains.

---

## ENSIM Associations Website Redesign
**October 2017 – May 2018** — Associated with ENSIM

Full redesign of the student associations website for ENSIM / Université du Mans.

---

## Android App Development
**July 2017 – August 2017**

Android application development.

**Tech:** Android Studio, Java, UML, XML, SQLite

---

## Coupe de France de Robotique — 5th place France
**September 2016 – June 2017** — Associated with ENSIM

Built a robot for the French Robotics Cup. Out of 150 qualified teams: **3rd in qualifying, 5th overall** — new record for ENSIM.

- Main robot: strategy development, LIDAR communication protocols, positioning
- Secondary robot: programming, strategy, mechanical and electronic design
- R&D team (4 members): odometry, opponent tracking, decision-making, mapping via LIDAR

**Tech:** C, C++, network programming, LIDAR, 3D modelling, electronics, Raspberry Pi

---

## Robotique Pédagogique (MERITE project)
**February 2016 – May 2016** — Associated with ENSIM

Teaching technology and programming to primary school children (CM1–CM2) via a multifunctional robot. Interdisciplinary team (Acoustics + CS students).

Role: **Project manager** — managed the robot interface team, client communication, conflict resolution.
