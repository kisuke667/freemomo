# FREEMOMO v2 — CODE MOTION

> **Noir obsidienne · Lime électrique · 100% CODE · Zéro API** — le studio motion qui n'est PAS une pâle copie de FREE HIGGS.
> 15 styles MG commerciaux en code Canvas — comme [mg-styles-15](https://vincentwei1021.github.io/mg-styles-15/) — chaque 10s est généré par `f(t)`, pas par une API.

[![Live](https://img.shields.io/badge/Live-freemomo.vercel.app-E8FF42?style=for-the-badge)](https://freemomo.vercel.app)
[![Version](https://img.shields.io/badge/version-v2_CODE_MOTION-111113?style=flat-square)](CHANGELOG.md)
[![No API](https://img.shields.io/badge/API-AUCUNE_—_100%25_CODE-00e5ff?style=flat-square)](#zéro-api)

## ✨ Démo

**→ https://freemomo.vercel.app** — ouvre `index.html`. Aucune clé, aucun backend.

## 🧬 Pourquoi ce n'est PAS FREE HIGGS

| FREE HIGGS | FREEMOMO v2 |
|------------|-------------|
| Studio **cinéma IA** par API (Agnès, Kling, Veo…) | Studio **motion CODE-ONLY** par Canvas |
| Pipeline scénario → images → vidéos (API) | Gallery 15 styles → Studio `f(t)` → preview → export |
| Besoin de clés API payantes | **Zéro clé** — tout tourne dans le navigateur |
| Génération asynchrone (polling 30min) | **Prévisualisation instantanée**, déterminisme `frame = f(t)` |
| Higgsfield Soul Cinema (référence visuelle) | [mg-styles-15](https://vincentwei1021.github.io/mg-styles-15/) (recette code) |

**Héritage assumé** : FREEMOMO est un *fork d'idée* de FREE HIGGS HIGGSFIELD (même exigence Higgsfield — obsidienne/lime, Space Grotesk, blur 16px) mais **refonte totale du moteur**.

## 🎬 15 styles — la galerie

Chaque carte : n° + nom FR/CN, film d'origine (mp4), signature, tech, palette, **▶ Film**, **⎘ Prompt** (1-shot), **Source**, **⦿ Utiliser**.

| n° | Style | CN | Signature | Tech |
|---|---|---|---|---|
| 01 | Frame-by-Frame | 逐帧手绘 | boil 2f · on 2s · smear · papier 12% | Canvas2D brush + paper |
| 02 | Isometric 2.5D | 等轴 2.5D | 30° iso · SSR 86.6% · parallax | Three.js ortho |
| 03 | Flat Vector | 扁平矢量 | stagger 2-4f · overshoot · shape wipe | SVG + GSAP |
| 04 | Line Art | 线条动画 | 3px champagne · dashoffset · line→fill | SVG dasharray |
| 05 | 3D Render | 3D 渲染 | SSS · cloner · long-tail 80/20 | Blender bpy |
| 06 | Shape Morph | 形变动画 | flubber · circle intermédiaire | SVG flubber |
| 07 | Sticker Explainer | 贴纸风 | peel · wobble spring | CSS spring |
| 08 | Cyberpunk HUD | 赛博朋克 | grid scan · iris sweep · CA | Canvas2D + WebGL |
| 09 | Collage | 拼贴剪贴 | cut edge · halftone · 12fps | Canvas multiply |
| 10 | Aurora & Glass | 弥散渐变 | mesh gradient · blur 24px · grain 3% | radial gradients |
| 11 | Bauhaus Geometric | 几何构成 | grid 12col · RYB · on-grid | SVG matrix |
| 12 | Synthwave 80s | 复古 | striped sun · grid scroll · VHS | linear gradients |
| 13 | Pixel Art | 像素风 | 8px · 4-color · 12fps | pixelate false |
| 14 | Liquid Motion | 液态流动 | metaball · marching squares | distance field + blur |
| 15 | Variety Captions | 综艺花字 | stroke 8px · bounce 1.56 · particles | GSAP bounce |

Chaque **prompt** est le 1-shot original mg-styles-15 (Creative Seed + Signature + Output 10.000s + How to work) — colle-le dans un dossier vide avec Claude Code (Node+Chrome+ffmpeg) pour un `video.mp4` natif H.264/AAC -14 LUFS.

## 🛠 Studio

1. **Galerie** → clique **⦿ Utiliser** (ou la carte)
2. **Studio — Creative Seed** : Brand, Tagline, Histoire, Palette 4 couleurs (injectée en `opts.colors`), FPS 24/30
3. **Preview** : canvas 1920×1080, lecture `t : 0→10s` en `f(t)` déterministe, scrub, plein écran
4. **Export** : `● Rec 10s → WebM` (`canvas.captureStream(30)` + `MediaRecorder` → `freemomo-<style>.webm`), **⎘ Copier source** / **⬇ Source .html** (squelette `for f in 0..fps*10: t=f/fps; draw(t)` pour rendu headless + ffmpeg)

> Recette ffmpeg (mp4 parfait) : `ffmpeg -framerate 30 -i frame_%04d.png -c:v libx264 -pix_fmt yuv420p -r 30 video.mp4`

## 📦 Stack

`single-file HTML` · `58090 bytes` · vanilla JS · Canvas2D · `Space Grotesk` / `JetBrains Mono` / `Inter` · 15 drawers `f(ctx,t,opts)` · MediaRecorder · déterministe `t` (pas de `Date.now`, pas de CSS transition).

## 📝 Philosophie mg-styles-15 (intégrée)

- **Hook 0.5s**, escalation, hero 60-75%, hold final 0.8-1.2s avec micro-motion
- Chaque style garde ses **signature features** (ne pas les supprimer)
- **Cue sheet** unique (image + son lisent les mêmes beats)
- **Deterministic** : `frame = f(t)` (seeded random only, precomputed physics)
- Seules sources **CC0/OFL/free-commercial**

## 🙏 Crédits

- 15 styles, vidéos, prompts : [vincentwei1021/mg-styles-15](https://vincentwei1021.github.io/mg-styles-15/) (inspiration directe)
- FREE HIGGS → [free-higgs](https://github.com/kisuke667/free-higgs) (Higgsfield-grade UI, fork d'idée)
- CINÉ-GENESIS · Laurent Voan Ho (origine)

## 📄 Licence

MIT
