# Nature & Landscapes - Prompt-Patterns

> Staerken: Makro-Fantasy-Szenen, epische Berglandschaften, Vier-Jahreszeiten-Kompositionen, Wolkenformationen und Mixed-Media-Uebergaenge zwischen Illustration und Fotorealismus. Mischung aus JSON und Fliesstext.

## Empfohlenes Format
Hybrid (JSON fuer detaillierte Landschafts-Szenen, Fliesstext fuer konzeptuelle und Template-basierte Prompts)

## Best Practice Patterns

### Pattern 1: Miniatur-Person in Makro-Natur (Surrealer Groessenkontrast)
JSON-Struktur fuer surreale Makro-Fantasy-Szenen mit extremem Groessenunterschied. Kombiniert Macro-Photography-Techniken mit Fantasy-Elementen fuer traumhafte Naturszenen.

```json
{
  "image_generation_prompt": {
    "subject": {
      "description": "A tiny man sitting and leaning against a tall young bean sprout",
      "clothing": "Casual pink t-shirt and black shorts",
      "pose": "Sitting relaxed on the ground, resting under a giant plant stem"
    },
    "environment": {
      "setting": "Surreal macro-fantasy scene, extreme close-up",
      "elements": "Detailed textures of soil, pebbles, roots, and young seedlings",
      "plant_details": "Bean sprout towering above with fresh green leaves, pale stems, and visible seed halves still attached"
    },
    "technical_specs": {
      "style": "Macro photography, Hyper-realistic, Cinematic",
      "lighting": "Natural outdoor lighting, realistic shadows, vibrant colors",
      "camera_effects": "Shallow depth of field, soft blurred background (bokeh), crisp highly detailed foreground",
      "resolution": "8K, Ultra-detailed"
    },
    "full_prompt_text": "A surreal macro-fantasy scene showing a tiny man wearing a pink t-shirt and black shorts, sitting and leaning against a tall young bean sprout. The environment is captured in extreme close-up macro style, revealing detailed textures of soil, pebbles, roots, and young seedlings. The bean sprout towers above him with fresh green leaves, pale stems, and visible seed halves. Shallow depth of field with soft blurred background, crisp foreground. Natural outdoor lighting, realistic shadows, vibrant colors, whimsical scale difference, hyper-realistic clarity."
  }
}
```

### Pattern 2: Epische Alpine Landschaft (Fantasy-Realismus)
Umfassendes JSON fuer epische Berglandschaften mit Fantasy-Realismus-Aesthetik. Definiert praezise Kamera-Settings, Farbpaletten und Negative Prompts fuer maximale Bildqualitaet.

```json
{
  "prompt_name": "High Alpine Sanctuary Village",
  "aesthetic_goal": "epic fantasy realism, ultra clear daylight, cinematic natural beauty, impossibly pristine and peaceful",
  "scene": {
    "environment": "steep emerald-green mountain terraces with bright mossy grass and scattered pink alpine flowers, layered with old trees and cliffs",
    "architecture": "small wooden highland houses and temples built on stone foundations, handcrafted timber, weathered roofs, clustered on ledges and plateaus",
    "background_scale": "towering icy mountain peak with dramatic ridgelines and snow, sharp sunlight hitting glacier edges, long depth all the way to the summit",
    "atmosphere": "thin mountain air, cool blue clarity, low drifting clouds and mist wrapping around the slopes, untouched sacred place",
    "tone": "utopian, peaceful, ancient, safe"
  },
  "lighting": {
    "style": "bright clean midday sunlight from upper right, high-elevation alpine light",
    "shadow_behavior": "soft but defined terrain shadows, gentle falloff into the valleys",
    "color_temperature": "cool sky blue mixed with fresh spring green bounce light from grass",
    "mood": "fresh, crisp, holy air feeling"
  },
  "camera": {
    "framing": "cinematic aerial wide shot looking slightly downward across the terraces toward the snow mountain in the distance",
    "lens": "full-frame equivalent ~18mm ultra wide landscape lens, deep depth of field",
    "focus": "sharp across entire frame, no blur, extreme detail in foliage, stone, wood, and snow texture",
    "composition_notes": "village in lower/mid frame leading the eye up the valley toward the sacred peak in the top of frame"
  },
  "style": {
    "keywords": [
      "fantasy landscape realism",
      "4K cinematic environment",
      "photoreal terrain detail",
      "lush micro-detail vegetation",
      "studio-grade color grading"
    ],
    "color_palette": "saturated alpine greens, icy whites, sky-deep cobalt blues"
  },
  "output_settings": {
    "aspect_ratio": "9:16",
    "format": "high detail still image",
    "quality_target": "ultra high resolution, sharp, no noise"
  },
  "negative_prompt": [
    "blurry, low detail, washed out, haze blocking the mountain",
    "cartoon, anime, game UI, infographic style",
    "text, captions, watermarks, logos, interface elements",
    "distorted perspective, warped buildings, melted terrain",
    "oversaturated neon color, unnatural purple grass, plastic look"
  ]
}
```

### Pattern 3: Vier-Jahreszeiten-Panorama (Template)
Fliesstext-Template fuer nahtlose Vier-Jahreszeiten-Kompositionen. Nutzt einen {Scene}-Platzhalter fuer flexible Anwendung auf beliebige Landschaften oder Stadtszenen.

```
Hyper-realistic digital illustration of {Scene}, presented as a single continuous composition showcasing the cycle of seasons. The scene flows seamlessly from left to right in a natural progression: Winter, Spring, Summer, and Autumn.

The left side features cold snowy winter elements, gradually thawing into the fresh green buds and blooms of spring, then morphing into the lush vibrant vegetation and bright sunlight of summer, and finally transitioning into the golden, orange, and red hues of autumn on the far right.

There are no visible dividing lines between seasons; the weather, lighting, and vegetation blend smoothly to create a unified and harmonious panorama. Rich in detail, symbolic of the passage of time, cinematic lighting, 8k resolution, highly detailed textures. --ar 4:3

----
Scene: [z.B. a majestic single oak tree on a rolling hillside]
```

### Pattern 4: Mixed-Media Dimensions-Uebergang (2D zu 3D)
Kreativer Prompt fuer Szenen, in denen eine illustrierte 2D-Welt nahtlos in eine photorealistische 3D-Umgebung uebergeht. Perfekt fuer whimsische Natur-Fantasy.

```
A cozy room where the wall looks like a giant paper illustration, flat ink lines and watercolor washes, yet a corner of the "paper wall" is peeled back, revealing a fully 3D forest behind it. The peeled edge curls outward like thick cardstock, casting a real shadow on the illustrated surface. The illusion: the 2D drawn objects (a drawn lamp, drawn shelf) cast realistic 3D shadows, while the 3D forest casts faint "ink" shadows as if it's becoming a drawing. A cat sits half-in, half-out: front paws in 3D forest moss, back body in 2D sketch form, seamlessly blended. Soft morning light, gentle pastel palette, tactile paper fibers visible, high detail, whimsical but believable "mixed-dimension" realism.
```

## Kategoriespezifische Tipps
- Makro-Szenen leben von extremem Groessenkontrast und Shallow Depth of Field
- Berglandschaften brauchen praezise Lichtrichtung und Farbtemperatur-Angaben
- Vier-Jahreszeiten-Bilder funktionieren am besten mit "no visible dividing lines" als explizite Anweisung
- Cloud-Formationen: "found shape" Ansatz nutzen - die Form soll natuerlich wirken, nicht kuenstlich
- Fuer Wolkenkunst: "A dramatic sky photo where swirling storm clouds naturally form the unmistakable shape of a [SUBJECT]"
- Mixed-Media-Uebergaenge benoetigen explizite Schattenbeschreibungen fuer beide "Dimensionen"
- Einfache Natur-Prompts koennen erstaunlich effektiv sein: "A photorealistic image of a leaf that looks like it's in the shape of a dragon"

## Empfohlene Negative Prompts
```
blurry, low detail, washed out, haze blocking the mountain, cartoon, anime, game UI, infographic style, text, captions, watermarks, logos, interface elements, distorted perspective, warped buildings, melted terrain, oversaturated neon color, unnatural purple grass, plastic look, CGI artifacts
```
