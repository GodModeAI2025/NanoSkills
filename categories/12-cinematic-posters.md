# Cinematic Posters - Prompt-Patterns

> Exzellent fuer Filmplakate, Storyboards und cineastische Szenen. JSON-Strukturen ermoeglichen praezise Kontrolle ueber Typografie, Beleuchtung und Komposition.

## Empfohlenes Format

Verschachtelte JSON-Objekte mit separaten Sektionen fuer Szene, Komposition, Garderobe, Beleuchtung und Typografie. Fuer einfachere Szenen funktioniert auch strukturierter Fliesstext.

## Best Practice Patterns

### Pattern 1: Romantisches Filmplakat im Studio-Stil

Erzeugt professionelle Filmposter mit praeziser Typografie-Kontrolle, Garderobe-Spezifikation und Studio-Beleuchtung.

```json
{
  "scene_summary": "Clean early-2000s rom-com studio poster composite. Two adults stand back-to-back in a playful confident stance, both glancing sideways at each other with amused expressions.",
  "composition": "Woman on the left, arms crossed, elegant posture. Man on the right, hands in pockets, relaxed lean. Full-body visible with generous negative space for title.",
  "wardrobe": "Woman: sleeveless/strapless satin yellow-gold floor-length gown with smooth sheen, minimal jewelry. Man: dark charcoal or black tailored suit, white shirt, no tie or subtle tie.",
  "props": "None.",
  "background": "Warm pale yellow/cream sky gradient with extremely subtle city/park blur at the bottom; clean studio cutout feel.",
  "lighting": "High-key studio lighting with softbox key + gentle rim light; crisp edges, natural shadows.",
  "typography": {
    "title_text_exact": "HOW TO LOSE A GUY IN 10 DAYS",
    "font_vibe": "classic rom-com serif with refined spacing",
    "color_and_harmony": "primary black with tasteful red/green accents that match the warm background without clashing",
    "placement": "center-lower, stacked like a classic rom-com poster"
  }
}
```

### Pattern 2: Cineastische Atmosphaere mit JSON-Stilkontrolle

Minimales JSON fuer maximale atmosphaerische Wirkung. Ideal fuer stimmungsvolle Einzelszenen mit Filmkoernung.

```json
{
  "description": "A lone figure in a long coat walking across a barren landscape in thick orange-red fog.",
  "subject": {
    "type": "lone figure",
    "attire": "long coat",
    "action": "walking"
  },
  "setting": {
    "location": "barren landscape",
    "atmosphere": "thick orange-red fog"
  },
  "visual_style": {
    "composition": "cinematic silhouette",
    "color_palette": "warm monochrome",
    "texture": "subtle film grain",
    "lighting": "high contrast",
    "realism": "photorealistic"
  }
}
```

### Pattern 3: Emotionales 9-Panel-Storyboard

Erzeugt zusammenhaengende Bildsequenzen mit einheitlicher Stimmung und Farbpalette. Perfekt fuer narrative Visualisierungen.

```
Create a 9-panel cinematic storyboard set in a rainy, melancholic atmosphere. Show a young woman in a soaked dress standing beneath stone arches as a man walks away into the rain. Include close-ups of her emotional expression, a moment of their hands parting, shots of her crying against a pillar, and a final wide shot of her standing alone. Use soft, moody lighting, blue-gray tones, shallow depth of field, and dramatic raindrops. Panels should feel emotional, poetic, and film-like
```

## Kategoriespezifische Tipps

- **Typografie**: `title_text_exact` und `strict_spelling_rule` fuer exakte Textwiedergabe
- **Poster-Komposition**: "generous negative space for title" reserviert Platz fuer Titeltext
- **Beleuchtung**: "high-key studio lighting with softbox key + gentle rim light" fuer professionellen Look
- **Storyboards**: Panelanzahl und Uebergaenge explizit beschreiben
- **Historische Szenen**: `use_search_grounding: true` fuer periodengerechte Details aktivieren
- **Negative-Space**: Fuer Poster immer Freiraum fuer Titel einplanen

## Empfohlene Negative Prompts

```json
[
  "extra people",
  "extra faces",
  "identity drift",
  "face blending",
  "plastic skin",
  "cartoon",
  "anime",
  "cgi look",
  "blurry faces",
  "deformed hands",
  "extra fingers",
  "extra text",
  "watermark",
  "logo",
  "credits block"
]
```
