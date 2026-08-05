# Code Projects

Overview of public/private GitHub repos and local workspace projects.
Organised by domain. GitHub: https://github.com/akaRicane

---

## ASTAR Ecosystem

The main creative coding software for live VJing and stage performance.
Multiple repos forming the full lifecycle from beta to distribution.

| Repo | Visibility | Description |
|---|---|---|
| `astar.studio.monorepo` | private | Main codebase — "One repository for them all". Electron + Solid + TypeScript + GLSL + C |
| `astar.studio.devtest` | private | Dev/test branch of ASTAR software |
| `astar.studio.lite` | local | Lightweight variant |
| `astar.hub` | private | ASTAR HUB — HTML/JS/TypeScript |
| `astar.beta` | private | LBSS.art ASTAR Beta |
| `astar.rs` | private | ASTAR rewrite exploration in Rust + TypeScript |
| `astar-boilerplate` | private | Electron TypeScript bundled boilerplate with launch validation |
| `astar-distribution` | public | Release/distribution repo |

**Core tech:** Electron.js, Solid.js, TypeScript, three.js, p5.js, GLSL/WebGL, MIDI, OSC, DMX, UDP

---

## LBSS.art — Collective & Creative

| Repo | Visibility | Description |
|---|---|---|
| `www.lbss.art` | private | Main website — AdonisJS + React + Tailwind |
| `lbss.engineering` | public | lbss.engineering website — Next.js |
| `lbss-creative` | private | Creative coding scripts — CSS/GLSL/HTML/JS |
| `lbss-generativeart` | private | Generative art experiments |
| `lbss-lights` | public | Lighting control code — C/C++/JS/Python/Shell |
| `lbss-core` | private | Core shared code |
| `lbss-website-astro` | private | Website iteration in Astro |
| `lbss.art.lectures` | public | Lectures/resources — CSS/HTML/JS/SCSS |
| `lbss.art-fast-website` | private | Fast static variant of the website |

---

## Websites

| Repo / Project | Visibility | Stack | Notes |
|---|---|---|---|
| `www.artistes-assistance.com` | private | AdonisJS, React, TypeScript, PostgreSQL, S3 | Client site with custom admin dashboard |
| `www.flagada.art` | private | AdonisJS, TypeScript, Docker | Active |
| `preprod-flagada` | private | same | Pre-prod environment |
| `www.ricane.art` | public | AdonisJS, TypeScript, Docker | Personal website |
| `ricane.art` | private | TypeScript, Docker, HTML | (iteration/variant) |
| `www.coursepoursuite.com` | local | — | Website for Course Poursuite (formerly Collectif Le Bol), Marseille |

---

## Desktop Applications

| Project | Visibility | Stack | Description |
|---|---|---|---|
| `master-metadata` | local | Electron, Solid.js, TypeScript, fluent-ffmpeg, music-metadata | Desktop app for audio file metadata management |
| `zuno` | private | AdonisJS 6 (backend + webapp), TypeScript, Python | Concert history tracker — manage artists seen and venues visited |
| `rawdio` | private | C++, CMake, Electron.js, HTML/JS | C++ Audio DSP interface wrapped in Electron |

---

## Audio & DSP Tools

| Repo | Visibility | Stack | Description |
|---|---|---|---|
| `ricane-plugins` | public | C++, JUCE 8, CMake | Bank of audio plugins built to learn plugin dev from the ground up — Gain, Panner, Delay. Each plugin self-contained (own `CMakeLists.txt`), JUCE and pluginval as pinned submodules, docs split into setup / DSP theory / per-plugin / tooling. Started July 2026 |
| `filter-design-tool` | public | CSS, HTML, JS, Python | Design loudspeaker filtering parameters |
| `audio-electronjs` | public | HTML, JS | Audio tooling in Electron |
| `audio-sandbox` | public | HTML, JS, Python, Shell | Multipurpose audio sandbox |
| `enttec-dmx-python` | public | Python | Python wrapper to control a DMX Universe |
| `lbss-lights` | public | C, C++, JS, Python | Lighting control (live events) |

---

## Games

| Repo | Visibility | Stack | Description |
|---|---|---|---|
| `paris-metro-guessr` | public | Vanilla JS, Leaflet, Python (build scripts) | Pin-the-station map game on the Paris métro/RER network. Live at [lutece-guessr.ricane.dev](https://lutece-guessr.ricane.dev). Started July 2026 |

No framework, no build step — ~2.9k lines split so the rules (`game.js`) and the maths (`geo.js`)
are pure and testable without DOM or Leaflet. Data is generated from Île-de-France Mobilités open
data: 536 stations, 660 track segments, plus the IGN Paris commune contour for the intra-muros
pool. Geometry is simplified with Douglas-Peucker to the point where it stays visually and
*logically* identical (the boundary ring is validated against the full-resolution point-in-polygon
verdict for all 536 stations). Bilingual EN/FR, exponential-decay scoring, deathmatch modes,
label-free basemap so the tiles can't leak the answer.

---

## Infrastructure

| Repo / Project | Visibility | Stack | Description |
|---|---|---|---|
| `infraweb` | private | Dockerfile, HCL (Terraform), Jinja, Ansible, Shell | Full infra-as-code for personal cloud: VPS, Coolify, DNS, deployments |
| `admin` | local | Shell, Docker Compose, MCP | Operating repo for the web infrastructure I run — Coolify CLI wrapper, monitoring stacks, runbooks. Started August 2026 |

Local structure: `infraweb/` contains `ansible/`, `apps/`, `infra-lbss/`, `sandbox/`, `local.debian`

`admin/` is the day-to-day operations counterpart to `infraweb/`'s provisioning: one folder per
administered system (`coolify/` first), a token-safe CLI wrapper, a Coolify MCP server wired into
Claude Code, a pre-commit secret scanner, and committed docs that carry names and public domains
only — IPs and UUIDs stay in a gitignored inventory. Estate today: 3 nodes, 8 projects, 7 apps,
9 services. Monitoring is Prometheus + blackbox + Loki + Grafana with agents on all three nodes,
Alpha and Beta reaching the master over WireGuard, nothing exposed publicly but Grafana. Umami
for website analytics.

---

## Templates & Boilerplates

| Repo | Visibility | Stack | Description |
|---|---|---|---|
| `adonis_solidts_template` | public | AdonisJS, Solid.js, TypeScript, Tailwind, Shadcn-solid, Docker | Go-to template for new web projects |
| `create-adonis-application` | local | — | CLI to scaffold from the template |
| `electron-boilerplate` | local | Electron | Base Electron setup |
| `astar-boilerplate` | private | Electron, TypeScript | ASTAR-specific Electron boilerplate |

---

## Mobile

| Project | Visibility | Stack | Description |
|---|---|---|---|
| `iziring` | local | React Native, Expo | Mobile app (in development) |
| `ENSIM_KFET` | public | Java, Android | Student project — Android cafeteria app (ENSIM) |

---

## Tools & Utilities

| Repo | Visibility | Stack | Description |
|---|---|---|---|
| `knowledge-bank` | public | HTML, CSS, Python | Personal documentation library |
| `politiscales-report` | public | Python | Generate group analysis report from Politiscales results |
| `healthcheck-nextjs` | public | Next.js, TypeScript | CI/CD health check endpoint |
| `healthcheck-static` | public | HTML, JS | Static health check for VPS CI/CD |
| `assets-handler` | public | React.js | File/asset management tool |
| `Integrate-P5-in-ReactJs` | public | React.js, p5.js | Template: p5.js in React |

---

## Student / Early Projects

| Repo | Visibility | Stack | Description |
|---|---|---|---|
| `RPiSoftware` | public | C, C++, Makefile | Raspberry Pi software — likely from robotics (ENSIM) |
| `ENSIM_KFET` | public | Java | Android cafeteria app (ENSIM student project) |
| `doxfood` + `doxfood-client` + `doxfood-api` | public/private | React.js, Python/Flask | Internal DXOMARK food app (full stack: React client + Flask API) |

---

## Local-only / Exploratory

| Project | Notes |
|---|---|
| `creative/` | Lab, dev, devtest, gooffy — generative art and visual experiments |
| `holophonix/` | Work-related code for current job at Holophonix |
| `__bin__/ricanespace` | Personal space / sandbox |
| `__bin__/ricane.dev` | Dev iteration of personal site |
| `__all__/room-acoustics` | Room acoustics tooling |
| `__all__/python-sarah` | Python project (unknown) |
| `__all__/ineedaudio` | Audio-related tool |
| `__all__/portaudio` | PortAudio integration |
| `__all__/open-fixture-library` | Fixture library (likely for lighting/DMX) |
| `mobiledev/poc` | Mobile proof of concept |
