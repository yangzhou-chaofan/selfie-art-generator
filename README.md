# Selfie Art Generator

Transform any selfie into stunning AI art — cinematic portrait, anime illustration, oil painting, or artistic photo makeover. Generate profile pictures, social media avatars, and personal portrait art with a single command.

## Install

```bash
npx skills add yangzhou-chaofan/selfie-art-generator
```

```bash
clawhub install selfie-art-generator
```

## Token Setup

This skill requires a Neta API token.

1. Get your free trial token at <https://www.neta.art/open/>
2. Pass it via the `--token` flag:

```bash
export NETA_TOKEN=your_token_here
node selfieartgenerator.js "your prompt" --token "$NETA_TOKEN"
```

> Note: The `NETA_API_BASE_URL` environment variable can be used to override the API base URL if needed.

## Usage

```bash
# Basic usage
node selfieartgenerator.js "artistic portrait photo, vibrant cinematic color grading, sharp facial details, golden hour lighting, professional photography style, high resolution" --token "$NETA_TOKEN"

# Anime style portrait
node selfieartgenerator.js "anime illustration portrait, soft pastel colors, detailed eyes, Studio Ghibli inspired" --size portrait --style anime --token "$NETA_TOKEN"

# Landscape cinematic shot
node selfieartgenerator.js "cinematic outdoor portrait, dramatic lighting, bokeh background" --size landscape --style cinematic --token "$NETA_TOKEN"

# Use a reference image (by picture UUID)
node selfieartgenerator.js "oil painting portrait style, classic renaissance look" --ref <picture_uuid> --token "$NETA_TOKEN"
```

## Options

| Option | Values | Default | Description |
|--------|--------|---------|-------------|
| `--size` | `portrait`, `landscape`, `square`, `tall` | `portrait` | Output image dimensions |
| `--style` | `anime`, `cinematic`, `realistic` | `cinematic` | Art style preset |
| `--token` | string | — | Neta API token (required) |
| `--ref` | picture_uuid | — | Reference image UUID for style inheritance |

### Size Dimensions

| Size | Width | Height |
|------|-------|--------|
| `square` | 1024 | 1024 |
| `portrait` | 832 | 1216 |
| `landscape` | 1216 | 832 |
| `tall` | 704 | 1408 |

## Output

On success, the script prints the generated image URL to stdout:

```
https://cdn.talesofai.cn/.../<image>.jpg
```

You can pipe this directly to a download command:

```bash
curl -o output.jpg "$(node selfieartgenerator.js "cinematic portrait" --token "$NETA_TOKEN")"
```

## Examples

**Cinematic profile picture:**
```bash
node selfieartgenerator.js "cinematic portrait, golden hour lighting, sharp facial features, professional headshot" --size portrait --style cinematic --token "$NETA_TOKEN"
```

**Anime avatar:**
```bash
node selfieartgenerator.js "anime style portrait, vibrant colors, detailed illustration, character art" --size square --style anime --token "$NETA_TOKEN"
```

**Oil painting:**
```bash
node selfieartgenerator.js "classical oil painting portrait, renaissance style, rich warm tones, museum quality" --size portrait --token "$NETA_TOKEN"
```

## Example Output

```bash
node selfieartgenerator.js "artistic portrait photo, vibrant cinematic color grading, sharp facial details, golden hour lighting, professional photography style, high resolution"
```

![Example output](https://oss.talesofai.cn/picture/4df8cb1b-745d-4af7-a80b-60aef36f6637.webp)

> Prompt: *"artistic portrait photo, vibrant cinematic color grading, sharp facial details, golden hour lighting, professional photography style, high resolution"*
