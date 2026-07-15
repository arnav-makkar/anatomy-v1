# CORPUS · Interactive Human Anatomy Atlas

An interactive, browser-based **3D anatomy atlas** for medical and pre-med students (MCAT · NEET · med-school anatomy). Explore organs in the browser, click any structure to study it, and switch between a clean labelled **Atlas** view and a realistic **Living** view.

> ⚗️ Personal prototype. Vanilla HTML + [Three.js](https://threejs.org) (CDN). One self-contained file, no build step.

---

## Features

- **13 modules** — Full Body · Heart · Brain · Lungs · Kidney · Pancreas · Gallbladder · Small & Large Intestine · Liver · Spleen · Blood Vessels · Stomach & GI.
- **Two views** — ☀ **Atlas** (clean, colour-coded, dissectable) ⇄ ☾ **Living** (realistic textured specimen, dramatic lighting, motion, optional sound).
- **Labels ⇄ Natural** — colour-coded parts for learning, or natural tissue colour.
- **Explore ⇄ Guided Tour** — free orbit + click-to-study, or an auto-playing camera tour of each organ's key structures.
- **Click any structure** — hover to reveal names; realistic specimens show **guide dots** at each region. Every part carries a curated function / clinical / high-yield note.
- **Full body** — 880+ named parts inside a translucent figure; click an organ to open its own module.
- **Macro-optics** magnified inset · live **ECG** (heart) · synthesized audio · record-to-`.webm`.

## Run it locally

Static site — it **must be served over HTTP** (`file://` blocks ES-module imports and `.glb` fetches):

```bash
python3 -m http.server 4173      # or: npx serve -l 4173
# open http://localhost:4173/
```

Three.js loads from a CDN at runtime. No install, no API keys. A dev-server config is included at `.claude/launch.json`.

## Structure

```
index.html          the app
cardia-demo.html    the original CARDIA heart demo (the inspiration)
assets/
  *.glb             realistic organ models (Living view)
  organs/           HuBMAP CCF reference organs (Atlas view + full body)
  tissue/           heart surface texture (triplanar tissue in Living)
CREDITS.md          model attributions & licences
```

## Credits & licensing

3D models are third-party assets under Creative Commons — see **[CREDITS.md](CREDITS.md)**. Most are **CC BY 4.0** (attribution, satisfied by that file). The **Stomach & GI** model is **CC BY-NC** (non-commercial) and is marked for removal before any commercial use.

App code derives from the MIT-licensed [cardia-survey](https://github.com/carolinacherry/cardia-survey) demo (© Daniel An).
