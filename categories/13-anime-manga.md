# Anime & Manga - Prompt-Patterns

> Perfekt fuer Anime-Poster, Manga-Panels, Comic-Strips und hybride Real/Anime-Portraits. JSON-Strukturen ermoeglichen mehrteilige Poster-Serien und Split-Effekte.

## Empfohlenes Format

Verschachtelte JSON-Objekte mit Arrays fuer Multi-Panel-Poster, Farbpaletten und Umgebungspanels. Fuer Split-Portraits detaillierte Spezifikation beider Haelften.

## Best Practice Patterns

### Pattern 1: GTA-V-Style City-Life Anime-Poster-Serie

Erzeugt stilisierte Anime-Poster im GTA-V-Comicgrid-Layout mit Zentral- und Umgebungspanels. Template fuer beliebige Laender und Staedte.

```json
{
  "posters": [
    {
      "title": "[COUNTRY] Side Stories: City Life -- Volume 1",
      "art_style": "Anime-style digital poster, GTA V--inspired comic grid, cinematic anime tone, nostalgic warmth mixed with urban energy",
      "center_panel": "A young character in casual streetwear standing between tradition and modernity, with the [CITY] skyline, [LANDMARK 1], and [LANDMARK 2] behind them.",
      "surrounding_panels": [
        "[BUSY SCENE] crowd motion blur",
        "Quiet shrine/historic moment",
        "[LOCAL FOOD] shop steam and late-night warmth",
        "School kids biking home at sunset",
        "[TRANSPORT] speeding past countryside",
        "Rainy [CITY] alley glowing with neon signs"
      ],
      "palette": [
        "Beige",
        "Indigo",
        "Neon red accents",
        "Soft film grain"
      ]
    }
  ]
}
```

### Pattern 2: Hybrider Real/Anime Split-Portrait

Erzeugt kreative Portraits, die auf einer Haelfte fotorealistisch und auf der anderen im Anime-Stil gerendert sind. Mit Kawaii-Dekorationselementen.

```json
{
  "image_generation": {
    "requirements": {
      "face_preservation": {
        "preserve_original": true,
        "accuracy_level": "100% identical to reference",
        "details": [
          "real facial proportions",
          "exact skin texture",
          "true eye shape and color",
          "natural soft makeup"
        ]
      },
      "pose": {
        "match_reference_pose": true,
        "description": "Chest-up portrait, face facing forward but gently tilted to the right from the viewer's perspective."
      }
    },
    "composition": {
      "frame": "chest-up portrait",
      "orientation": "frontal with slight rightward tilt",
      "style": "hyper-realistic with split real/cartoon effect"
    },
    "special_effects": {
      "split_effect": {
        "type": "irregular centered tear",
        "edges": "white angled torn-paper look",
        "description": "image appears ripped down the middle"
      },
      "realistic_side": {
        "background": "soft, neutral, slightly bluish environment",
        "filters": [
          "soft analog grain",
          "lightly aged texture",
          "reduced saturation",
          "subtle film imperfections"
        ]
      },
      "illustrated_side": {
        "art_style": "bold cartoon, digital illustration",
        "color_palette": "bright, vibrant, saturated",
        "background": "vibrant light pink pop-art style",
        "decorations": {
          "kawaii_elements": [
            "pixel-art mascot character",
            "yellow stars",
            "pink hearts",
            "colorful planets"
          ]
        }
      }
    },
    "output": {
      "style": "hyper-realistic + digital cartoon fusion",
      "quality": "ultra-high-resolution",
      "filters": [
        "subtle analog vintage film filter",
        "soft grain"
      ]
    }
  }
}
```

### Pattern 3: Cartoon-Charakter mit realem Menschen kombiniert

Einfacher Fliesstext-Prompt fuer die Kombination von realen Personen mit Cartoon-Charakteren im Studio-Setting.

```
Ultra-high-resolution 8K studio portrait featuring a real human woman standing beside a stylized cartoon character of choice, full-body composition, both subjects clearly visible and centered.

Human subject: young adult woman with natural smile, relaxed confident posture, realistic facial features, natural makeup, wearing modern casual clothing such as a knit sweater, fitted jeans or pants, and casual sneakers, photorealistic skin texture, detailed hair strands, soft facial highlights.

Cartoon character: [INSERT CARTOON CHARACTER NAME OR STYLE], fully animated and stylized, vibrant saturated colors, smooth or plush-like surface texture, expressive large eyes, friendly confident expression, exaggerated cartoon proportions, standing upright in a human-like pose, interacting naturally with the human subject by standing close or leaning slightly.

Lighting: soft professional studio lighting, even illumination, no harsh shadows, subtle rim light separating subjects from background.

Background: clean minimal studio backdrop, solid color or smooth gradient, color-coordinated with subjects, no props, no text.

Style & Quality: hyper-detailed, photorealistic human + high-quality 3D cartoon render, ultra-sharp focus, cinematic clarity, commercial advertising look, premium finish, no watermark, no logos, no text, perfectly balanced realism and animation.
```

## Kategoriespezifische Tipps

- **GTA-V-Grid**: 6 "surrounding_panels" plus 1 "center_panel" fuer authentischen GTA-Look
- **Farbpaletten**: 3-4 Farben pro Poster, "Soft film grain" als Stilmittel
- **Split-Portraits**: "irregular centered tear" mit "torn-paper look" fuer den Riss-Effekt
- **Kawaii-Elemente**: Pixel-Art-Maskottchen und Sterne fuer den japanischen Pop-Art-Stil
- **Multi-Poster**: Array von Postern im JSON fuer zusammenhaengende Serien

## Empfohlene Negative Prompts

```
photorealistic CGI, uncanny valley, blurry lines, inconsistent art style, western cartoon style, 3D render look, low resolution, watermark, extra limbs, deformed faces, mixed aspect ratios
```
