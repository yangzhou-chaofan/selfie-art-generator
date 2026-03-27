---
name: selfie-art-generator
description: Transform any selfie into stunning AI art — cinematic portrait, anime illustration, oil painting, or artistic photo makeover. AI selfie art generator for profile pictures, social media avatars, and personal portrait creation via the Neta AI image generation API (free trial at neta.art/open).
tools: Bash
---

# Selfie Art Generator

Transform any selfie into stunning AI art — cinematic portrait, anime illustration, oil painting, or artistic photo makeover. AI selfie art generator for profile pictures, social media avatars, and personal portrait creation.

## Token

Requires a Neta API token. Free trial available at <https://www.neta.art/open/>.

```bash
export NETA_TOKEN=your_token_here
node <script> "your prompt" --token "$NETA_TOKEN"
```

## When to use
Use when someone asks to generate or create selfie art generator images.

## Quick start
```bash
node selfieartgenerator.js "your description here" --token YOUR_TOKEN
```

## Options
- `--size` — `portrait`, `landscape`, `square`, `tall` (default: `portrait`)
- `--style` — `anime`, `cinematic`, `realistic` (default: `cinematic`)

## Install
```bash
npx skills add yangzhou-chaofan/selfie-art-generator
```
