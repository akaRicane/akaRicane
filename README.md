## hi, I'm Philippe — aka Ricane

engineer by training, creative coder by passion. I build the tools that power the performances, then perform with them.

---

### what I make

**[ASTAR](https://github.com/akaRicane/astar-distribution)** — a live creative coding environment I built from scratch for VJing and stage design.
Runs on Electron, speaks WebGL/GLSL, listens to MIDI, controls DMX, reacts to audio.
Currently used on stage across France and Belgium.

```js
// the loop, every frame
render(t) {
  this.scene.update(t, this.midi, this.audio)
  this.shader.draw(this.gl)
  this.dmx.flush()
}
```

**[LBSS.art](https://lbss.art)** — the project I perform under. VJing, scenography, light shows.
Managed by Adequate Production. Toured with Le Wanski, played Dour Festival, Zénith Lille, Reperkusound...

**[Course Poursuite](https://coursepoursuite.com)** — artist collective I co-founded. Marseille-based. Events, stage design, production.

---

### stack

```
lang      →  TypeScript · JavaScript · Python · C / C++  · Bash
runtime   →  Node.js · Electron · Linux (embedded)
web       →  AdonisJS · React · Solid.js · Tailwind
visual    →  WebGL · GLSL · three.js · p5.js
live      →  MIDI · DMX · OSC · Resolume · TouchDesigner · QLC+
infra     →  Docker · Ansible · Terraform · Coolify · AWS
```

---

### currently

building the QA stack at **[HOLOPHONIX](https://holophonix.xyz)** — spatial audio processors for concert halls, theaters, and installations.
software validation, hardware QC, Linux system work, and a custom Electron test app.

---

### also

acoustics engineer by background (ENSIM, Vibrations & Acoustics).
2 papers at AES conventions. 4 years at DXOMARK building the audio benchmark from scratch.

[linkedin](https://linkedin.com/in/philippeguelen) · [lbss.art](https://lbss.art) · [adequateproduction.fr/artiste/lbss-art](https://adequateproduction.fr/artiste/lbss-art/)
