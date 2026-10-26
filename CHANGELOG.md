# Changelog

## v2 (2026-10-26) — CODE MOTION — 100% CODE, ZÉRO API
- **Refonte totale** : plus une copie de FREE HIGGS — moteur code-only inspiré de [mg-styles-15](https://vincentwei1021.github.io/mg-styles-15/) de Vincent Wei
- **Galerie 15 styles commerciaux** : Frame-by-Frame, Isometric 2.5D, Flat Vector, Line Art, 3D Render, Shape Morph, Sticker, HUD, Collage, Aurora & Glass, Bauhaus, Synthwave, Pixel Art, Liquid, Variety Captions — chaque carte avec film mp4, signature, tech, palette, prompt 1-shot, source
- **Studio Creative Seed** : Brand/Tagline/Histoire/Palette 4 couleurs/FPS — injectés en `opts.colors` dans `f(ctx,t,opts)`
- **Preview déterministe** : 15 drawers `f(ctx,t)` (boil, iso SSR, flat elastic, line dashoffset, 3D cloner, morph flubber, sticker wobble, HUD scan, collage halftone, aurora mesh, bauhaus grid, synthwave sun, pixel 8px, metaballs, hanazi bounce) — `t: 0→10s`, `frame = f(t)` pur, pas de Date.now ni CSS transition
- **Export** : `Rec 10s → WebM` via `canvas.captureStream(30)` + `MediaRecorder` + source `.html` squelette `for f: draw(f/fps)` pour rendu headless Chrome + ffmpeg → `video.mp4` H.264/AAC -14 LUFS
- **Prompts** : 15 prompts 1-shot mg-styles-15 complets (Style/Output/Route/Creative Seed/Signature/How to work/Rules) — copier-coller dans dossier vide Claude Code (Node+Chrome+ffmpeg)
- **Higgsfield-grade UI conservée** : obsidienne #060608, lime #E8FF42, Space Grotesk, blur 16px — mais navigation Galerie/Studio/Prompts (plus pipeline 7 étapes API)
- **58 KB single-file**, `node --check` OK, `html --check` unclosed [], `viewport-fit=cover`, iPhone-safe

## v1 (2026-10-26) — MOTION HIGGSFIELD (archive)
- Fork motion de FREE HIGGS v9 — 6 familles, brand kit, keyframes — archivé en `versions/v1.html`

