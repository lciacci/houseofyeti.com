# House of Yeti — Site Context

## Overview
Single-page marketing site for houseofyeti.com. Built as a plain HTML/CSS/JS file using Tailwind CDN — no build step, deployed via SFTP.

## Local path
`/Users/lorenzociacci/houseofyeti/`

## Repo
`https://github.com/lciacci/houseofyeti.com`

## Deployment
SFTP to own server. SSL is active — all links must use `https://`.

## Structure
```
index.html        — single responsive page
images/
  bg-jungle.jpg   — mobile/tablet background (jungle)
  bg-mountain.jpg — desktop parallax mountain layer
  bg-foliage.jpg  — desktop parallax foliage layer (used x2)
  settempo-app.jpg — Settempo app screenshot (used x3)
```
Images were downloaded from Stitch's Google CDN and are self-hosted. Replace with final assets when available.

## Responsive breakpoints
- **Mobile** (`< md`): tilt portrait card, metadata row (Prototype 004 / Florence coordinates), vertical nav links, mountain glow bg
- **Tablet** (`md → lg`): full-bleed jungle image, 12-col grid — copy left / landscape card right
- **Desktop** (`lg+`): parallax layers with mouse glow, scrollable hero section → Settempo two-column section

## Brand
- **Headline font**: Newsreader (italic, light)
- **Body/Label font**: Plus Jakarta Sans
- **Display font**: Share Tech Mono (mobile Settempo card)
- **Primary colour**: `#83d5c6` (teal)
- **Settempo gold**: `#fabd00`
- **Background**: `#111413`

## Key copy
- Hero tagline: *"DISTANTLY ACCESSIBLE"*
- Hero body: *"A signal from somewhere past the last road. We build things here. Some of them work."*
- Settempo description: *"A precision metronome reimagined for the modern composer. Dark glass aesthetics meet tropical precision, creating a rhythmic companion that feels more like an instrument than a tool."*
- Mobile metadata: Prototype 004 / Release MMXXVI / 43.7696° N, 11.2558° E (Florence, Italy — intentional, on brand)
- Footer: © 2026 House of Yeti. Crafted in the Tropics.

## Links
- Settempo launch: `https://houseofyeti.com/settempo`
- Settempo guide: `https://houseofyeti.com/settempo/guide.html`
- About: `https://lorenzociacci.com`
- Instagram: `https://instagram.com/lonosan`
- Contact/Inquire: obfuscated mailto — `lono@houseofyeti.com` (assembled in JS at runtime, not visible in HTML source)

## Contact email obfuscation
All contact/inquire `<a>` tags use `href="#" data-m="c"`. An IIFE in the script block assembles the address from character arrays and sets the `href` at runtime. Do not add the email address directly to any HTML attribute.

## TODO / future work
- Replace Stitch placeholder images with final photography/assets
- Add Instagram link content (handle: lonosan)
- Add Privacy Policy and Terms pages if needed (currently omitted from mobile footer)
- lorenzociacci.com portfolio site exists locally at one level above this repo — no repo yet
