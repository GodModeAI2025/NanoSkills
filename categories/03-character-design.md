# Character Design - Prompt-Patterns

> Staerke dieser Kategorie: Chibi-3D-Charaktere, Photo-to-Illustration-Konvertierung, Pixar-Style-Doppelgaenger, Fashion-Editorial mit Cartoon-Elementen. Ideal fuer personalisierte Avatare, Social-Media-Content und kreative Portraets.

## Empfohlenes Format
JSON (detaillierte Charakter-Definitionen mit Subject, Art Style, Environment, Composition)

## Best Practice Patterns

### Pattern 1: Chibi-Style 3D Character (JSON-Charakter-Sheet)
Dieses Pattern definiert einen vollstaendigen 3D-Charakter im Chibi-Stil mit detaillierten Outfit-, Haar- und Umgebungsspezifikationen. Besonders stark: Die Trennung von subject, art_style und environment.

```json
{
  "subject": {
    "type": "chibi-style 3D character",
    "gender": "female",
    "features": {
      "hair": "pastel pink bob cut with soft bangs, stylized 3D strands",
      "eyes": "large expressive dark eyes, looking upward and to the side",
      "expression": "dreamy, slightly surprised, open mouth",
      "skin": "fair with soft pink blush on cheeks",
      "accessories": ["small gold hoop earrings", "delicate gold necklace with heart pendant"]
    },
    "outfit": {
      "top": "tight-fitting dark brown long-sleeved crop top",
      "bottom": "high-waisted peach-colored joggers or harem pants",
      "shoes": "brown and tan platform sneakers"
    }
  },
  "art_style": {
    "type": "3D render / C4D / Octane Render",
    "aesthetic": "soft claymorphism, smooth textures, toy-like aesthetic",
    "lighting": "soft cinematic lighting, warm sunlight, gentle shadows",
    "camera": "full body shot, eye-level, shallow depth of field (bokeh)"
  },
  "environment": {
    "background": "blurred Mediterranean-style street, soft orange and cream buildings, arched doorway",
    "color_palette": ["pastel pink", "peach", "warm brown", "cream"]
  }
}
```

### Pattern 2: Pixar-Style Doppelgaenger (JSON mit Negative Prompt)
Dieses Pattern erzeugt eine Szene, in der eine reale Person neben ihrer Pixar-3D-Version steht. Besonders wertvoll: Die detaillierten Anweisungen zur Koerperproportionen-Kontrolle und Gesichts-Matching.

```json
{
  "prompt": "Hyper-realistic studio photo of a stylish person using the uploaded reference face with exact facial likeness, proportions, and expression. The person is standing casually with legs crossed at the ankles, one arm wrapped around a giant Pixar-style 3D version of themselves. Outfit: navy blue hoodie, beige chinos, cream-colored sneakers. The Pixar 3D character has a slim, athletic body (NOT chubby or fat), identical outfit, same height scale as shown, same confident stance, one hand on hip. The Pixar character has the SAME playful facial expression as reference: clear mischievous smile with a DISTINCT wink (one eye closed, one eye open). Facial structure, eyebrows, jawline, nose, and smile must closely match the uploaded face. Clean soft pink backdrop, studio lighting, soft shadows, high detail, smooth Pixar-quality materials, realistic human skin texture on the real person, polished 3D render on the Pixar character.",
  "negative_prompt": "fat body, chubby Pixar character, oversized head, wrong face shape, missing wink, both eyes open, different pose, different expression, stiff pose, exaggerated cartoon distortion, mismatched clothing, incorrect proportions, blurry, low detail, glossy plastic skin on human, uncanny face",
  "size": "4:5",
  "reference": "100% use uploaded image for face, pose, body proportions, and expression accuracy"
}
```

### Pattern 3: Doodle Art Portrait (JSON-Varianten-System)
Dieses Pattern verwandelt Fotos in energetische Doodle-Art-Illustrationen auf Notizbuch-Papier. Besonders stark: Das Varianten-System mit verschiedenen Farbpaletten und Stimmungen.

```json
{
  "image_generation_task": {
    "task_type": "img2img",
    "input_source": "uploaded_user_image",
    "constraint": "preserve_full_likeness",
    
    "base_configuration": {
      "medium": {
        "substrate": "lined notebook paper",
        "tools": ["ballpoint pen", "neon markers", "ink"],
        "texture_details": [
          "realistic ink absorption",
          "layered pen pressure",
          "stained edges",
          "smudges",
          "subtle paper wrinkles"
        ]
      },
      "art_style": {
        "genre": ["doodle art", "comic annotations", "sketch"],
        "line_work": "thick-thin variation, loose freestyle, messy strokes, dynamic hatch shading",
        "atmosphere": "chaotic, energetic, spontaneous, dense"
      },
      "rendering": {
        "resolution": "4K",
        "detail_level": "high",
        "lighting": "bold outer glow, vibrant contrast"
      }
    },

    "composition_elements": {
      "framing": "portrait with thick border line around head",
      "surrounding_elements": [
        "messy arrows",
        "stars",
        "underlines",
        "random scribbles",
        "speech bubbles",
        "overlapping annotations",
        "checkboxes"
      ],
      "iconography": [
        "lightning bolt",
        "lightbulb",
        "music note",
        "mini self-caricature"
      ],
      "typography": {
        "style": "handwritten comic notes",
        "sound_effects": ["ZAP!", "WHOOSH!"]
      }
    },

    "style_variations": [
      {
        "id": "variant_01_pop_bold",
        "color_palette": ["bold cyan", "magenta"],
        "specific_vibe": "vibrant pop, stylish comic notes"
      },
      {
        "id": "variant_02_neon_highlight",
        "color_palette": ["neon pink", "neon yellow"],
        "specific_vibe": "highlighter aesthetic, expressive gestures"
      },
      {
        "id": "variant_03_electric_graffiti",
        "color_palette": ["hot electric blue", "neon red"],
        "specific_vibe": "graffiti-styled, exaggerated outline, playful highlights"
      },
      {
        "id": "variant_04_dense_sketch",
        "color_palette": ["blue linework", "red accents"],
        "specific_vibe": "densely packed, horror vacui (no blank space), alive and messy"
      }
    ]
  }
}
```

### Pattern 4: Watercolor Portrait auf Skizzenbuch (JSON-Kamera-Detail)
Dieses Pattern erzeugt hyperrealistische Szenen eines Aquarell-Portraits auf einem Kuenstler-Schreibtisch. Besonders stark: Die Top-Down-Kamera-Perspektive und die Textur-Details von Farbe und Papier.

```json
{
  "image_generation": {
    "type": "hyper_realistic_cinematic_ultra_close_up",
    "camera": {
      "angle": "top-down",
      "focus": "extreme close-up",
      "depth_of_field": "shallow",
      "sharp_focus_on": [
        "painted watercolor details",
        "paper grain",
        "wet pigment textures"
      ]
    },
    "subject": {
      "object": "white sketchbook lying half-open on an artist's wooden desk",
      "illustration": {
        "style": "soft watercolor fashion illustration",
        "subject_match": {
          "reference_person": true,
          "description": "The illustration shows the same person from the uploaded photo in the same outfit and pose, painted in flowing watercolor strokes."
        },
        "details": [
          "visible pigment texture",
          "soft gradients",
          "flowing brushwork"
        ]
      },
      "tools": {
        "paintbrush": {
          "description": "a slightly wet paintbrush resting on the sketchbook page edge"
        }
      }
    },
    "environment": {
      "setting": "artist's wooden desk",
      "lighting": {
        "source": "warm natural daylight",
        "effects": [
          "light streaming from the side",
          "reflections on wet paint",
          "soft shadows on textured paper"
        ]
      }
    },
    "mood": "artistic, serene, tactile, cinematic watercolor-in-progress aesthetic"
  }
}
```

## Kategoriespezifische Tipps
- Fuer Face-Matching immer explizit "preserve_full_likeness" oder "exact facial likeness" angeben
- Pixar-Style-Charaktere neigen zu uebergrossen Koepfen -- explizit "NOT chubby, slim athletic body" erwaehnen
- Haende sind kritisch: immer "perfect hands, five fingers each, no warping" in den Prompt einbauen
- C4D / Octane Render als Rendering-Engine erwaehnen fuer konsistenten 3D-Look
- "Claymorphism" und "toy-like aesthetic" erzeugen den modernen Chibi-Look
- Varianten-Systeme (style_variations) sind ideal fuer A/B-Testing verschiedener Looks
- Aspect Ratios: 4:5 fuer Instagram, 9:16 fuer Stories/Reels

## Empfohlene Negative Prompts
```
fat body, chubby character, oversized head, wrong face shape, different expression, stiff pose, exaggerated cartoon distortion, mismatched clothing, incorrect proportions, blurry, low detail, glossy plastic skin, uncanny face, extra fingers, warped hands, deformed nails, identity change, face drift
```
