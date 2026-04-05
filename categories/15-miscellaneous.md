# Miscellaneous - Prompt-Patterns

> Vielseitige Kategorie fuer detaillierte Szenenkomposition, Portraitfotografie und komplexe Mehpersonen-Arrangements. JSON-Strukturen ermoeglichen praezise Kontrolle ueber Posen, Kleidung und Umgebung.

## Empfohlenes Format

Tiefverschachtelte JSON-Objekte mit separaten Sektionen fuer Kamera, Subjekte (als Array), Umgebung, Beleuchtung und Qualitaets-Tags. Alternativ detaillierter Fliesstext mit klaren Absaetzen.

## Best Practice Patterns

### Pattern 1: Mehpersonen-Szenenfoto mit detaillierter Posenkontrolle

Praezise JSON-Struktur fuer Gruppenfotos mit individueller Kontrolle ueber jede Person (Pose, Ausdruck, Kleidung, Position).

```json
{
  "aspect_ratio": "9:16",
  "scene_type": "indoor sports team photo",
  "camera": {
    "device": "smartphone or digital camera",
    "angle": "eye-level",
    "framing": "full body of three subjects, vertical framing",
    "focus": "sharp focus on subjects and background text",
    "style": "casual team snapshot"
  },
  "subjects": [
    {
      "position": "left",
      "gender": "female",
      "build": "athletic",
      "hair": {
        "color": "light brown",
        "length": "long",
        "style": "straight, worn loose over shoulders"
      },
      "face": {
        "shape": "oval",
        "expression": "broad smile",
        "eyes": "open, looking at camera",
        "emotion": "happy and confident"
      },
      "body_posture": {
        "stance": "standing upright",
        "arms": "one hand resting on hip, other arm relaxed",
        "feet": "barefoot, flat on floor"
      },
      "clothing": {
        "type": "gymnastics leotard",
        "primary_color": "maroon",
        "details": "long sleeves with mesh and rhinestone accents"
      }
    }
  ],
  "environment": {
    "location": "indoor athletic facility",
    "background": {
      "wall_material": "horizontal wooden panels",
      "text": {
        "words": "Maroon & Gold",
        "font_style": "bold sans-serif",
        "colors": ["maroon", "gold"],
        "placement": "centered behind subjects"
      }
    }
  },
  "lighting": {
    "type": "indoor ambient lighting",
    "direction": "even frontal",
    "quality": "soft, no harsh shadows"
  },
  "quality_tags": [
    "clear facial expressions",
    "accurate body posture",
    "detailed uniforms",
    "vertical framing",
    "no watermark"
  ]
}
```

### Pattern 2: Detailliertes Portrait mit Beleuchtungs- und Farbkontrolle

Umfassendes JSON mit technischen Kameraspezifikationen, Farbprofil und kuenstlerischen Elementen fuer maximale Kontrolle.

```json
{
  "lighting": {
    "quality": "hard flash with soft ambient",
    "shadows": "sharp shadows cast by the flash",
    "direction": "frontal",
    "ambient_source": "warm LED Christmas lights on tree",
    "primary_source": "on-camera flash"
  },
  "composition": {
    "frame_type": "medium shot",
    "focus_point": "subject's face",
    "orientation": "vertical",
    "camera_angle": "eye-level",
    "depth_of_field": "shallow",
    "subject_placement": "centered"
  },
  "color_profile": {
    "contrast": "high",
    "saturation": "moderate",
    "color_balance": "warm",
    "dominant_colors": ["#FFFFFF", "#E10000", "#4A5D48", "#C9A082"],
    "palette_description": "warm and festive palette dominated by white and red"
  },
  "technical_specs": {
    "iso": "high",
    "aperture": "wide (shallow depth of field)",
    "image_type": "digital photograph",
    "camera_type": "smartphone camera",
    "shutter_speed": "fast (due to flash)"
  },
  "subject_analysis": {
    "pose": "standing, hands pressed to cheeks",
    "makeup": "dewy skin, defined eyebrows, long eyelashes, rosy blush, glossy lips",
    "clothing": "oversized white knit sweater with a red Fair Isle pattern featuring snowflakes",
    "expression": "playful, pouting kiss"
  },
  "artistic_elements": {
    "mood": "playful, festive, cozy",
    "style": "candid portrait",
    "texture": "soft knit of the sweater, glossy reflection on the window"
  },
  "generation_parameters": {
    "aspect_ratio": "4:5",
    "negative_prompt": "daylight, bright sun, plain wall, no flash"
  }
}
```

### Pattern 3: Hyper-realistisches Cafe-Portrait mit Film-Aesthetik

Detaillierter Fliesstext-Prompt mit klaren Absaetzen fuer Mode, Hintergrund, Beleuchtung und Kamerastil.

```
Create a hyper-realistic portrait of a cute Asian woman. She is sitting with her chin resting on her hand at a dark wooden table in front of a vintage-style cafe.

Fashion & Outfit:
She wears a shiny black leather jacket, slightly open to reveal a white inner top, showing a beautiful neckline. Matched with a fitted black mini-skirt set. She also wears black fishnet stockings. Add a fluffy fur hat over her outfit.

Background:
In front of a marble-grey cafe exterior, decorated with a Christmas theme. Include a realistic Christmas tree, pine decorations, and festive ornaments.

Lighting & Tone:
Warm orange tungsten lighting for an inviting, cozy atmosphere, combined with a strong direct flash hitting the subject straight on, making her skin bright and glowing, contrasting with the slightly darker background.
The photo should feel Y2K digital compact-camera style--sharp 8K resolution, realistic skin texture, with light film grain.

Hair & Makeup:
Long dark-brown hair blowing slightly in the wind, messy layered strands with a few pieces softly covering part of her face--stylish, cool, and subtly sexy.
Her skin is very fair.
Makeup style: Douyin/Korean--long curled lashes, soft flushed pink blush on cheeks and nose tip, glossy pink lips.

Props:
On the table: A large bouquet wrapped in brown kraft paper, containing cotton flowers and pine leaves.

Additional Visual Style:
The flash creates extremely bright, slightly yellow-tinted skin with a hard shadow behind her.
High-contrast, ultra-sharp 8K image.
Warm ambient sunlight.
Fuji Film Pro 400H color style with old-lens filter and light film grain.
The subject should appear bright and stand out clearly from the background.
```

## Kategoriespezifische Tipps

- **Mehpersonen-Szenen**: Jede Person als separates Objekt im `subjects`-Array mit individuellen Attributen
- **Farbcodes**: Hex-Farbwerte (`#FFFFFF`) im `dominant_colors`-Array fuer praezise Farbkontrolle
- **Kameraspezifikationen**: ISO, Blende und Verschlusszeit im `technical_specs`-Objekt fuer authentischen Look
- **Film-Emulation**: "Fuji Film Pro 400H" oder aehnliche Filmstocks als Stilreferenz
- **Beleuchtungsmix**: Kombination aus Flash und Ambient-Licht ("hard flash with soft ambient") erzeugt natuerliche Tiefe
- **Posenbeschreibung**: Separate Felder fuer Stance, Arms, Feet, Torso fuer maximale Praezision

## Empfohlene Negative Prompts

```
daylight when indoor scene intended, bright sun, plain wall, blurry faces, extra limbs, deformed hands, extra fingers, watermark, logo, text overlay, overexposed, underexposed, flat lighting, plastic skin, uncanny valley
```
