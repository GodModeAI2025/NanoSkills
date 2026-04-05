# Fashion Photography - Prompt-Patterns

> Zweitgroesste Kategorie mit ~50 Prompts. Deckt Editorial Grids, Streetwear, Outdoor, Casual Lifestyle, High Fashion und Vintage-Styles ab. Besonders stark bei Multi-Panel-Collagen und detaillierten Outfit-Beschreibungen.

## Empfohlenes Format
JSON mit Panel-Architektur fuer Grids, verschachteltes JSON fuer Einzelbilder. Fashion-Prompts profitieren stark von separaten Sektionen fuer `subject`, `outfit/apparel`, `environment`, `lighting` und `camera`/`technical_specs`.

## Best Practice Patterns

### Pattern 1: Editorial Fashion Collage (2x2 Grid)

**Sub-Genre:** Multi-Panel Beauty Editorial mit konsistentem Subject ueber alle Panels  
**Staerke:** Strukturierte `panel_architecture` mit individuellen Shot-Types, Posen und Visual Anchors pro Panel. Globale Assets (Subject, Wardrobe, Environment) werden einmal definiert und in allen Panels wiederverwendet.

```json
{
  "project_specifications": {
    "format": "2x2 Grid Collage",
    "aspect_ratio": "4:5",
    "aesthetic_style": "High-end Beauty Editorial",
    "rendering_engine_hints": {
      "realism_level": "Ultra-photorealistic",
      "texture_quality": "8k",
      "lighting_simulation": "Ray-traced studio lighting"
    }
  },
  "global_assets": {
    "subject_definition": {
      "hair": {
        "style": "Long, loosely wavy, voluminous",
        "texture": "Natural, individual strands defined",
        "behavior": "Messy but styled, framing face and shoulders"
      },
      "complexion": {
        "skin_texture": "Porous, hyper-realistic",
        "finish": "Dewy, glass-skin effect",
        "makeup": {
          "cheeks": "Heavy flush/blush",
          "lips": "High-gloss, plump, natural pink",
          "eyes": "Clean, defined lashes, natural brows"
        }
      },
      "wardrobe": {
        "item": "Mini dress",
        "fit": "Bodycon / Tight",
        "fabric": {
          "material": "Soft textured knit / Boucle",
          "tactility": "Fuzzy, light-catching fibers",
          "color": "Soft mauve or neutral taupe"
        },
        "details": "Spaghetti straps, mid-thigh length"
      }
    },
    "environment_definition": {
      "studio_setup": {
        "background": "Seamless paper, soft off-white/beige",
        "atmosphere": "Clean, warm, intimate"
      },
      "lighting_rig": {
        "key_light": "Large diffuse softbox (Front-Left)",
        "fill_light": "Reflector (Right)",
        "highlights": "Specular highlights on lips, cheekbones, and shoulders"
      }
    }
  },
  "panel_architecture": [
    {
      "position": "Top-Left (1)",
      "shot_type": "Extreme Close-Up (Macro)",
      "composition": {
        "angle": "Low angle, looking up slightly",
        "focus": "Mouth and nose area",
        "depth_of_field": "Shallow"
      },
      "action": {
        "primary": "Eating a strawberry",
        "nuance": "Delicate finger hold, lips slightly parted"
      },
      "visual_anchors": [
        "Moisture on strawberry surface",
        "Gloss reflection on lips",
        "Baby hairs at temple"
      ]
    },
    {
      "position": "Top-Right (2)",
      "shot_type": "Medium Shot (Thigh-up)",
      "composition": {
        "angle": "Eye level",
        "pose_dynamic": "Leaning forward slightly towards lens"
      },
      "action": {
        "stance": "Standing straight on",
        "arms": "Relaxed at sides",
        "expression": "Direct gaze, alluring pout"
      },
      "visual_anchors": [
        "Texture of knit dress",
        "Collarbone shadows",
        "Curvature of waist"
      ]
    },
    {
      "position": "Bottom-Left (3)",
      "shot_type": "Full Body (Seated)",
      "composition": {
        "angle": "Side profile",
        "framing": "Subject compacted on floor"
      },
      "action": {
        "pose": "Knees to chest (fetal position variation)",
        "interaction": "Cheek resting on knee, arms embracing legs",
        "hair_flow": "Cascading onto the floor"
      },
      "visual_anchors": [
        "Smooth leg definition",
        "Dress stretching over thigh",
        "Dreamy gaze"
      ]
    },
    {
      "position": "Bottom-Right (4)",
      "shot_type": "Beauty Portrait (Head & Hands)",
      "composition": {
        "angle": "Frontal close-up",
        "framing": "Chin to hairline"
      },
      "action": {
        "gesture": "Chin resting on interlaced fingers",
        "expression": "Soft smile, looking off-camera"
      },
      "visual_anchors": [
        "Hand detail and manicure",
        "Eye clarity",
        "Flush on cheeks"
      ]
    }
  ]
}
```

---

### Pattern 2: Streetwear Urban (Moody Night Scene)

**Sub-Genre:** Cinematic Urban Streetwear mit Nacht-Atmosphaere  
**Staerke:** Kompakter Prompt mit starkem Mood durch `color_grading` und spezifische Location-Elemente (nasses Pflaster, Reflektionen). Zeigt, dass Fashion-Prompts auch mit weniger Verschachtelung funktionieren.

```json
{
  "prompt": {
    "scene": {
      "location": "gas station",
      "time_of_day": "night",
      "elements": [
        "black sports car",
        "wet ground reflecting colorful urban lights",
        "gas station elements",
        "building with signs"
      ]
    },
    "subject": {
      "gender": "female",
      "pose": "leaning against sports car",
      "clothing": {
        "type": "tracksuit",
        "color": "black",
        "detailing": "distinct orange and yellow lettering"
      },
      "hair": {
        "style": "wavy",
        "details": "slightly wavy"
      }
    },
    "image_quality": {
      "style": "ultra-realistic",
      "resolution": "8k",
      "features": [
        "cinematic night lighting",
        "HDR cinematic sharpness",
        "hyper-detailed textures"
      ],
      "camera": {
        "photo_characteristics": [
          "natural proportions",
          "realistic textures",
          "vibrant reflections from artificial lights"
        ]
      }
    },
    "color_grading": {
      "mood": "dark and moody",
      "lighting": "vibrant reflections from urban lights"
    }
  }
}
```

---

### Pattern 3: Garden/Outdoor Fashion

**Sub-Genre:** Romantische Outdoor-Fashion in formaler Gartenumgebung  
**Staerke:** Detaillierte Environment-Beschreibung mit architektonischen Elementen, die das Outfit ergaenzen. Klare `technical_specs` Sektion mit Lighting und Camera-Angaben.

```json
{
  "image_prompt": {
    "subject": {
      "demographics": "Young woman, fit physique, sun-kissed skin tone",
      "hair": "Long, voluminous, dark brown wavy hair, side-parted and flowing over the back",
      "expression": "Calm, looking away to the right in profile view",
      "pose": "Standing upright, legs crossed at the ankles, holding a flower near the chest, slightly lifting the skirt edge with the other hand"
    },
    "attire": {
      "garment": "Short, pale yellow mini dress with a delicate floral pattern",
      "details": [
        "Puff sleeves",
        "Sweetheart neckline with a center tie string",
        "Corset-style fitted bodice",
        "Pleated, flared A-line skirt",
        "Vintage cottagecore aesthetic"
      ],
      "footwear": "White pointed-toe heels"
    },
    "accessories": {
      "items": [
        "Single long-stemmed pink rose held in left hand",
        "Gold ring on left ring finger"
      ]
    },
    "setting": {
      "location": "Formal estate garden",
      "elements": [
        "Manicured geometric boxwood hedges",
        "Green grassy lawn",
        "Stone fountain with a statue (mid-ground right)",
        "Large tiered stone fountain base (foreground left)",
        "Grand stone staircase and white pergola structure in background",
        "Palm trees and lush greenery in distance"
      ]
    },
    "lighting_and_atmosphere": {
      "time_of_day": "Mid-day, bright sunlight",
      "sky": "Clear, vibrant blue sky",
      "lighting_quality": "High contrast, sharp shadows, natural hard light",
      "mood": "Romantic, summery, elegant, serene"
    },
    "technical_specs": {
      "style": "Realistic photography",
      "shot_type": "Full-body shot",
      "angle": "Eye-level",
      "focus": "Sharp focus on subject, deep depth of field"
    }
  }
}
```

---

### Pattern 4: Casual Lifestyle Fashion

**Sub-Genre:** Entspannte Lifestyle-Fotografie an ikonischem Ort  
**Staerke:** Verbindet Fashion mit Location-Storytelling. Detaillierte `foreground_elements` und `background`-Beschreibungen schaffen Kontext. Zeigt wie Accessoires und Handlungen die Szene beleben.

```json
{
  "prompt_type": "Ultra-Photorealistic Lifestyle Photography",
  "subject": {
    "description": "Young woman with a chic, luxurious aesthetic",
    "hair": "Blonde, styled in a messy yet elegant updo with loose strands framing the face",
    "apparel": {
      "outfit": "White structured mini dress or romper with a square neckline, short sleeves, and large white buttons down the front",
      "accessories": [
        "Black oval sunglasses",
        "Silver luxury logo brooch on the left chest",
        "Silver bracelet/watch on left wrist",
        "Small rings"
      ],
      "footwear": "Not visible, implied chic heels or sandals"
    },
    "pose": "Seated on a cafe chair, legs crossed at the knee, body slightly angled towards the camera, right hand raised near the face in a posing gesture, left hand resting on the chair frame"
  },
  "environment": {
    "location": "Outdoor street-side cafe in Paris",
    "background": {
      "landmark": "The Eiffel Tower visible in the distance down the street center",
      "architecture": "Classic Parisian Haussmann-style limestone buildings with balconies",
      "street": "Parked cars lining the right side, paved sidewalk"
    },
    "foreground_elements": {
      "furniture": "Typical round bistro table, grey metal cafe chair",
      "items": "Black quilted luxury handbag sitting on the table, wine glasses, white napkins",
      "decor": "Black and white striped awning overhead"
    }
  },
  "lighting": {
    "type": "Natural daylight",
    "quality": "Soft afternoon sun, creating gentle shadows and highlights on the subject's skin and dress",
    "sky": "Blue sky with scattered white clouds"
  },
  "camera_settings": {
    "style": "High-end lifestyle photography, influencer travel aesthetic",
    "lens": "35mm or 50mm portrait lens",
    "aperture": "f/2.8 to f/4",
    "resolution": "8k, Ultra HD",
    "focus": "Sharp focus on the subject and immediate foreground",
    "texture_quality": "High fidelity textures on the fabric of the dress, the quilted bag leather, and the stone buildings"
  },
  "mood": "Chic, elegant, cosmopolitan, relaxed luxury, travel wanderlust"
}
```

---

### Pattern 5: High Fashion (Studio Editorial)

**Sub-Genre:** Dramatisches Studio-Editorial mit Lichteffekten  
**Staerke:** Sehr detaillierte `creative_prompt`-Struktur mit separaten Sektionen fuer Pose, Wardrobe, Effects, Lighting und Composition. Zeigt fortgeschrittene Techniken wie simulierte Langzeitbelichtung fuer Light-Streaks bei gleichzeitig scharfem Gesicht.

```json
{
  "generation_request": {
    "output_settings": {
      "aspect_ratio": "4:5",
      "orientation": "portrait",
      "resolution": "ultra_high_res",
      "render_style": "photorealistic_high_fashion_editorial",
      "sharpness": "high",
      "film_grain": "subtle"
    },
    "creative_prompt": {
      "scene_summary": "A moody high-fashion editorial portrait. Dark studio background. Dramatic beauty lighting with warm light streak/motion blur across the torso (long-exposure light-painting effect). Silver chainmail/metal mesh dress. One arm raised over head, hand resting on forehead. Elegant intense gaze.",
      "subject": {
        "expression": "serious, seductive editorial, confident gaze",
        "makeup": "defined eyeliner, softly smoky eyes, bronzed contour, satin nude lips",
        "hair": "sleek straight hair or smooth blowout, tucked behind ears"
      },
      "wardrobe_and_accessories": {
        "dress": "silver metallic chainmail / crystal mesh slip dress with draped neckline, reflective micro-texture, high-end couture feel",
        "earrings": "long statement crystal fringe earrings (sparkly)",
        "nails": "long clean nude nails (almond/stiletto)"
      },
      "pose": {
        "upper_body": "right arm raised over head, hand resting on forehead, elbow bent; left hand near chest/waist",
        "posture": "elongated neck, shoulders angled slightly, elegant fashion stance"
      },
      "effects": {
        "light_streaks": "warm golden light streaks / motion blur sweeping diagonally across the dress and torso, like handheld light painting during a long exposure; keep face mostly sharp",
        "motion_blur_rule": "blur only affects the light streaks and a small portion of dress; do NOT blur the facial features"
      },
      "environment": {
        "background": "deep charcoal/black studio backdrop with subtle gradient, no props"
      },
      "lighting_and_camera": {
        "lighting": "dramatic studio key light from upper-left with soft fill; warm gelled streak light; controlled highlights on metallic fabric",
        "camera": "full-frame DSLR look",
        "lens": "85mm prime",
        "aperture": "f/2.8",
        "shutter_effect": "simulate long exposure for light streaks while keeping face sharp",
        "focus": "tack-sharp eyes and lips; detailed dress texture; background falls off smoothly"
      },
      "composition": {
        "framing": "portrait mid-shot (upper torso to head), centered, cinematic negative space around",
        "vibe": "luxury editorial, magazine cover quality"
      },
      "strict_rules": [
        "NO text",
        "NO logos",
        "NO watermark",
        "single subject only",
        "keep face sharp; blur only in light streak effect",
        "no extra objects"
      ]
    },
    "negative_prompt": [
      "text", "logo", "watermark", "extra people",
      "face drift, identity change",
      "heavy blur on face",
      "low resolution, noise artifacts",
      "bad hands, fused fingers, missing fingers",
      "over-smoothed skin, waxy face"
    ]
  }
}
```

---

### Pattern 6: Vintage/Retro Fashion (Multi-Panel Collage)

**Sub-Genre:** Retro-inspirierter Streetstyle als Editorial-Collage mit UI-Overlays  
**Staerke:** Kombiniert Fashion-Collage mit digitalen UI-Elementen (Music Player, Grid-Overlays). Zeigt wie `composition_layout` einzelne Frames mit unterschiedlichen Kamerawinkeln und Effekten definiert. Starke `aesthetic_theme` mit konsistenter Farbpalette.

```json
{
  "project_title": "Urban Streetwear Editorial Collage",
  "aspect_ratio": "9:16",
  "aesthetic_theme": {
    "style": "Editorial poster-style multi-panel collage",
    "mood": "Retro analog-digital fusion",
    "color_palette": [
      "Warm ambers",
      "Washed neutrals",
      "Soft greys",
      "Muted browns"
    ],
    "textures": [
      "Reflective glass",
      "Wool plaid",
      "Polished leather",
      "Stone pavement"
    ]
  },
  "subject_outfit": {
    "core": "Brown plaid blazer, white button-up shirt, yellow tie, loose dark trousers",
    "accessories": "Brown cap, oversized amber-tinted rectangular sunglasses",
    "tech": "Wired earphones"
  },
  "composition_layout": {
    "frame_1_top_left": {
      "type": "Reflective window shot",
      "pose": "Holding phone in front of face",
      "visual_effects": "Layered ghosting, architectural overlays, curvature distortion"
    },
    "frame_2_top_right": {
      "type": "Close-range, downward-angled ultra-wide portrait",
      "setting": "Cobblestone street",
      "pose": "Leaning forward, hands in pockets, exaggerated pout",
      "visual_effects": "Lens perspective distortion, radiating cobblestones"
    },
    "frame_3_bottom_right": {
      "type": "Intimate overhead selfie",
      "lighting": "Soft overcast",
      "props": "Holding a drink",
      "overlays": "Faint digital-grid, minimal square facial-bounding graphic"
    }
  },
  "ui_elements": {
    "music_player": {
      "style": "Translucent iOS-style mini-player",
      "features": "Artwork, timeline, playback controls (no shadows)"
    },
    "graphics": "Subtle cursor-like frame lines, rectangular highlights"
  },
  "negative_constraints": [
    "Stickers",
    "Extra subjects",
    "Wardrobe changes",
    "Incorrect UI icons",
    "Neon color shifts",
    "Futuristic sci-fi elements"
  ]
}
```

---

## Grid/Collage Kompositions-Regeln

Fashion Photography nutzt haeufig Multi-Panel-Layouts. Bewaehrte Grid-Strukturen:

### 2x2 Grid (4 Panels)
- **Verwendung:** Beauty Editorials, Outfit-Showcases
- **Typische Aufteilung:** Macro Close-Up | Medium Shot | Full Body | Beauty Portrait
- **Key:** `panel_architecture` Array mit `position`, `shot_type`, `composition`, `action`, `visual_anchors` pro Panel
- **Aspect Ratio:** 4:5 (Instagram-optimiert)

### 3x3 Grid (9 Panels)
- **Verwendung:** Beauty Routines, Accessoire-Showcases, Lifestyle-Collagen
- **Typische Aufteilung:** Mix aus Subject-Panels und Detail/Product-Panels
- **Key:** `image_composition.layout: "3x3 Grid"` mit `total_panels: 9`

### Asymmetrische Collage (3 Panels)
- **Verwendung:** Streetwear Editorials, Poster-Style
- **Typische Aufteilung:** Unterschiedlich grosse Panels mit verschiedenen Kamerawinkeln
- **Key:** `composition_layout` mit benannten Frames, `visual_effects` pro Frame
- **Aspect Ratio:** 9:16 (Story-Format)

### Konsistenz-Regeln fuer alle Grids
- **Globale Assets:** Subject, Outfit und Environment einmal definieren, nicht pro Panel wiederholen
- **Visual Consistency Rule:** Explizit angeben: "All frames depict the same subject, outfit, hairstyle"
- **Variation:** Nur Pose, Kamerawinkel, Shot-Type und Expression variieren

## Kategoriespezifische Tipps

1. **Outfit-Beschreibungen dreistufig aufbauen:** Garment-Type > Farbe/Material > Details (Neckline, Fit, Textur)
2. **Fabric Physics erwaehnen:** "Soft drape", "light-catching fibers", "reflective micro-texture" -- steigert Realismus
3. **Accessoires nicht vergessen:** Schmuck, Taschen, Schuhe separat beschreiben
4. **Pose mit Haenden spezifizieren:** "right hand resting on forehead", "left hand on knee" -- vermeidet Hand-Artefakte
5. **Lighting nach Genre waehlen:**
   - Studio Editorial: Softbox + Rim Light
   - Outdoor: Natural daylight mit Tageszeit
   - Night/Urban: Cinematic night lighting + Reflektionen
6. **Camera Specs realistisch halten:** 85mm f/1.8 fuer Portraits, 35mm fuer Lifestyle, 50mm als Allrounder
7. **Mood/Vibe als eigenstaendige Sektion:** Hilft dem Modell, den Gesamtton zu treffen

## Empfohlene Negative Prompts

```json
[
  "text", "logo", "watermark",
  "extra people",
  "bad hands", "fused fingers", "missing fingers",
  "face drift", "identity change",
  "low resolution", "noise artifacts", "blur artifacts",
  "over-smoothed skin", "waxy face",
  "distorted proportions", "extra limbs",
  "artificial looking skin"
]
```

Fuer High Fashion zusaetzlich:
```json
[
  "cheap plastic fabric",
  "hard cut edges", "sloppy masking"
]
```

Fuer Grid/Collagen zusaetzlich:
```json
[
  "wardrobe changes between panels",
  "inconsistent lighting across frames",
  "stickers", "neon color shifts"
]
```
