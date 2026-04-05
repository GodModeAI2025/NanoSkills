# Portrait Photography - Prompt-Patterns

> Die umfangreichste Kategorie mit ~50 Prompts. Deckt Studio-Portraits, Beauty-Makro, Lifestyle/Travel, Mirror-Selfies, Night/Urban-Portraits und Fitness-Selfies ab. Gemeinsames Merkmal: Tief verschachtelte JSON-Strukturen mit detaillierten Beschreibungen fuer Subject, Lighting, Camera und Environment.

## Empfohlenes Format

Tief verschachteltes JSON mit separaten Bloecken fuer `subject`, `environment`, `lighting`, `camera_settings` und `render_quality`. Die meisten Prompts nutzen 3-5 Verschachtelungsebenen. Besonders wichtig: Klare Trennung von Personen-Beschreibung (Haar, Haut, Ausdruck, Kleidung) und Szenen-Beschreibung (Location, Licht, Atmosphaere).

## Identity Lock Protokoll

Das Identity Lock Pattern kommt in fast allen Portrait-Prompts vor, die ein Referenzbild verwenden. Es stellt sicher, dass Gesichtszuege der hochgeladenen Person exakt erhalten bleiben:

```json
{
  "reference": {
    "face_identity": "uploaded reference image",
    "identity_lock": true,
    "face_preservation": "100% identical facial structure, proportions, skin texture, eye shape, lips, nose, brows, moles, freckles, and natural expression"
  }
}
```

Varianten:
- `"strict_identity_lock": true` -- Strenge Gesichtsbewahrung
- `"alter_face": false` -- Gesicht darf nicht veraendert werden
- `"use_reference_image": true` -- Referenzbild als Grundlage

Haeufig kombiniert mit `hard_constraints` wie:
```json
"hard_constraints": [
  "Face must match the uploaded reference with maximum similarity.",
  "Photorealistic anatomy, natural skin texture, no beauty filter."
]
```

---

## Best Practice Patterns

### Pattern 1: Studio Portrait (Klassisch)

Klassisches Studio-Setup mit kontrolliertem Licht, nahtlosem Hintergrund und detaillierter Beschreibung von Pose, Wardrobe und Lichtsetzung. Ideal fuer professionelle Portraitfotografie mit Multi-Panel-Layouts.

```json
{
  "realism_level": "Ultra-photorealistic",
  "texture_quality": "8k",
  "lighting_simulation": "Ray-traced studio lighting",
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
    }
  ]
}
```

**Kernmerkmale:**
- `global_assets` definiert Subject und Environment einmalig fuer alle Panels
- `panel_architecture` als Array fuer Multi-Shot-Layouts
- `lighting_rig` mit Key Light, Fill Light und Highlight-Beschreibung
- `visual_anchors` als Liste von Details, die der Generator betonen soll

---

### Pattern 2: Beauty Macro / Close-up

Extremes Close-up mit Fokus auf Hauttextur, Wassertropfen und Augendetails. Kombiniert einen Fliesstext-Prompt mit technischen Parametern und Negative Prompt.

```json
{
  "prompt": "Extreme wet close-up portrait, side profile of a young woman. Dark wet hair strands naturally glued to the skin. Fine droplets of water and thin sweat glistening realistically on face. Focus on bright natural green and hazel eyes with realistic reflection. Moist and shiny lips, soft natural skin texture. Soft lighting, cool color tones, light grey and white bokeh background. Hyper-realistic, 8k resolution, cinematic photography, raw style.",
  "negative_prompt": "excessive shine, oily skin, dry skin, heavy makeup, cartoon, illustration, 3d render, low quality, blurry, distorted eyes, bad anatomy, overexposed, high contrast",
  "parameters": {
    "aspect_ratio": "9:16",
    "steps": 30,
    "cfg_scale": 7.0,
    "style": "Photorealistic"
  }
}
```

**Kernmerkmale:**
- Kompakteres Format: Ein einzelner `prompt`-String statt tief verschachteltem JSON
- `negative_prompt` explizit angegeben -- wichtig fuer Hautqualitaet
- Technische `parameters` mit Steps und CFG Scale
- Fokus auf Mikro-Details: Wassertropfen, Poren, Reflexionen in den Augen

---

### Pattern 3: Lifestyle / Travel Portrait

Aufwendiges Location-Portrait mit Landmark im Hintergrund, cinematischer Lichtsetzung und Film-Look. Zeigt die volle Tiefe der JSON-Verschachtelung.

```json
{
  "scene_manifest": {
    "version": "3.1.0",
    "request_type": "photorealistic_generation",
    "compositional_settings": {
      "aspect_ratio": "3:4",
      "framing": "Medium shot",
      "camera_angle": "Eye-level",
      "subject_orientation": "Profile view facing left"
    }
  },
  "subject_entity": {
    "demographics": {
      "gender": "Female",
      "age_cohort": "Young Adult",
      "archetype": "Travel Influencer / Glamour"
    },
    "physical_attributes": {
      "hair": {
        "color_technique": "Honey-blonde balayage",
        "texture_descriptors": ["Long", "Wavy"],
        "current_state": "Being touched by hand"
      },
      "face": {
        "makeup_style": "Soft glam",
        "specific_features": ["Defined eyeliner", "Soft skin texture"],
        "expression_gaze": "Dreamy, looking away into distance"
      }
    },
    "styling_and_apparel": {
      "upper_garment": {
        "color": "Black",
        "type": "Sleeveless crop top",
        "cut": "Deep V-neckline",
        "fit": "Fitted chic"
      },
      "lower_garment": {
        "color": "Black",
        "type": "Mini skirt or dress (matching set)"
      },
      "adornments": {
        "wristwear": ["Silver bracelet", "Gold bangle"],
        "grooming": "Manicured nails"
      }
    },
    "pose_and_action": {
      "primary_posture": "Seated on ledge",
      "limb_placement": {
        "legs": "Crossed",
        "arms": "One hand raised running through hair"
      }
    }
  },
  "environmental_context": {
    "geo_location": {
      "landmark_name": "The Colosseum",
      "city": "Rome",
      "country": "Italy"
    },
    "scene_elements": {
      "foreground": "Ancient weathered stone ledge (subject seat)",
      "midground": "Illuminated ancient Roman arches",
      "background": "Deep twilight sky"
    },
    "atmospherics": {
      "time_of_day": "Blue Hour (Twilight)",
      "sky_condition": "Deep blue, clear evening",
      "mood_descriptors": ["Romantic", "Luxurious", "Cinematic", "Atmospheric"]
    }
  },
  "rendering_specifications": {
    "photographic_equipment": {
      "camera_body": "High-end DSLR",
      "lens_choice": "Portrait prime lens (50mm or 85mm)",
      "aperture_setting": "f/2.8 (Shallow depth of field)",
      "focus_point": "Sharp focus on subject eyes/face"
    },
    "lighting_design": {
      "scheme": "Mixed Cinematic Lighting",
      "sources": [
        {
          "type": "Key Light",
          "color": "Warm soft glow",
          "target": "Subject face and hair"
        },
        {
          "type": "Architectural Light",
          "color": "Warm golden tungsten",
          "target": "Ruins in background"
        },
        {
          "type": "Ambient Fill",
          "color": "Cool deep blue tones",
          "source": "Evening sky"
        }
      ]
    },
    "post_processing_style": {
      "aesthetic": "35mm film grain",
      "resolution": "8K",
      "texture_quality": "Highly detailed, photorealistic"
    }
  }
}
```

**Kernmerkmale:**
- `scene_manifest` mit Version und Request-Type -- quasi ein API-artiger Header
- `subject_entity` mit Demographics und Archetypes
- `environmental_context` mit echtem Geo-Location-Objekt
- Dreischichtiges Szenen-Setup: Foreground / Midground / Background
- `rendering_specifications` trennt Kamera-Equipment von Lighting und Post-Processing

---

### Pattern 4: Mirror Selfie

Authentischer Mirror-Selfie-Look mit Smartphone, Flash-Reflexion und Schlafzimmer-Setting. Betont die "ungestellte" Aesthetik.

```json
{
  "image_description": {
    "subject": {
      "gender": "female",
      "hair": {
        "color": "dark black",
        "style": "long, layered, voluminous waves",
        "texture": "glossy"
      },
      "face": {
        "expression": "sultry, neutral",
        "makeup": "Natural",
        "eye_color": "light hazel or green"
      },
      "skin_tone": "Fair"
    },
    "clothing": {
      "type": "dress",
      "pattern": "leopard print",
      "style": "backless, halter neck, bodycon/fitted",
      "fabric_texture": "smooth"
    },
    "accessories": {
      "jewelry": [
        "gold hoop earrings",
        "thin chain necklace with a cross pendant hanging down the back",
        "stack of gold and silver bangles/bracelets on wrist"
      ],
      "objects": "smartphone (iPhone style) held in right hand"
    },
    "pose": {
      "stance": "standing, angled profile showing back and side",
      "head_position": "turned over left shoulder facing the mirror",
      "action": "taking a mirror selfie"
    },
    "environment": {
      "location": "bedroom",
      "background_elements": [
        {
          "object": "bed",
          "details": "white linens, chunky beige knit throw blanket at the foot"
        },
        {
          "object": "furniture",
          "details": "wooden dresser with rattan/cane drawers, wooden bedside table"
        },
        {
          "object": "lighting_fixture",
          "details": "bedside lamp with warm yellow light"
        }
      ],
      "walls": "plain, neutral beige/cream color"
    },
    "lighting": {
      "source": "camera flash reflected in mirror",
      "effect": "bright starburst flare from flash, warm ambient glow from bedside lamp",
      "atmosphere": "dim, cozy, evening setting"
    },
    "technical_details": {
      "type": "mirror selfie",
      "perspective": "reflection",
      "focus": "sharp on subject, slightly softer background"
    }
  }
}
```

**Kernmerkmale:**
- `pose.action: "taking a mirror selfie"` -- explizite Selfie-Anweisung
- Flash-Reflexion als Lichtquelle (`"camera flash reflected in mirror"`)
- Background-Elements als Array mit detaillierten Objekt-Beschreibungen
- Kein `camera_settings`-Block noetig -- der Smartphone-Look kommt durch die Selfie-Perspektive

---

### Pattern 5: Night / Urban Portrait

Naechtliches Stadtportrait mit Neon-Beleuchtung, Bokeh und optionalem Camcorder-UI-Overlay. Zeigt wie cinematische Effekte und urbane Atmosphaere kombiniert werden.

```json
{
  "subject": {
    "gender": "female",
    "age": "young adult",
    "hair": {
      "color": "dark brown",
      "texture": "wet look",
      "style": "long, wavy, messy, loose strands framing face"
    },
    "eyes": {
      "color": "green/hazel",
      "makeup": "subtle winged eyeliner, natural eyeshadow"
    },
    "skin": {
      "tone": "light/fair",
      "texture": "smooth, dewy finish, high sheen on shoulder and cheekbones",
      "makeup": "soft contour, glossy lips"
    },
    "expression": "soft smile, direct eye contact, alluring"
  },
  "apparel": {
    "top": {
      "type": "crop top",
      "color": "black",
      "material": "ribbed fabric",
      "fit": "tight",
      "straps": "thin straps"
    }
  },
  "pose": {
    "action": "leaning forward",
    "arms": "resting on a railing",
    "angle": "3/4 portrait view"
  },
  "environment": {
    "setting": "city street at night",
    "background": "blurred urban cityscape, bokeh streetlights, car headlights, building lights",
    "atmosphere": "nightlife, candid"
  },
  "lighting": {
    "type": "flash photography style mixed with ambient street lighting",
    "highlights": "strong specular highlights on skin (shoulder, forehead, nose)",
    "shadows": "soft shadows defining facial features"
  },
  "camera_settings": {
    "shot_type": "medium close-up",
    "depth_of_field": "shallow",
    "focus": "sharp on face"
  },
  "camera_details": {
    "camera_model": "Canon EOS R5 Mirrorless Digital Camera",
    "lens": "Canon RF 85mm f/1.2L USM Lens",
    "aperture": "f/1.4",
    "iso": "1600",
    "shutter_speed": "1/100s",
    "focal_length": "85mm",
    "white_balance": "Auto (AWB) with slight tungsten warmth",
    "flash_type": "Direct on-camera flash with diffuser",
    "image_format": "RAW",
    "color_profile": "Adobe RGB"
  }
}
```

**Kernmerkmale:**
- Hohe ISO (1600) und offene Blende (f/1.4) fuer authentischen Nacht-Look
- "Wet look" Hair und "dewy finish" Skin fuer Nacht-Regen-Aesthetik
- Flash + Ambient Mix erzeugt den typischen Nightlife-Portrait-Look
- Konkrete Kamera- und Objektiv-Angaben (Canon EOS R5, RF 85mm) steigern den Realismus
- Bokeh-reicher Hintergrund durch Streetlights und Car Headlights

---

### Pattern 6: Fitness / Gym Selfie

Sportlicher Selfie-Look mit natuerlichem Gym-Licht, Smartphone-Kamera-Simulation und "sporty glow" Makeup.

```json
{
  "image_prompt": {
    "reference": {
      "face_identity": "uploaded reference image",
      "identity_lock": true,
      "face_preservation": "100% identical facial structure, proportions, skin texture, eye shape, lips, nose, brows, moles, freckles, and natural expression"
    },
    "subject": {
      "type": "young woman",
      "expression": "soft relaxed expression with slightly glossy lips",
      "gaze": "looking slightly past the camera with calm confidence",
      "pose": {
        "position": "close-up selfie angle from slightly above",
        "head": "subtle tilt",
        "posture": "casual and natural"
      }
    },
    "hair": {
      "color": "dark brown",
      "style": "pulled back into a low ponytail or tied-back style with clean hairline"
    },
    "makeup": {
      "style": "natural sporty glow",
      "details": [
        "dewy skin finish",
        "defined brows",
        "light mascara",
        "natural blush",
        "soft glossy pink lips"
      ]
    },
    "outfit": {
      "top": "loose white graphic t-shirt",
      "accessories": [
        "white over-ear headphones resting around the neck",
        "small stud earrings"
      ]
    },
    "environment": {
      "location": "modern gym interior",
      "background_elements": [
        "gym benches",
        "exercise machines",
        "wooden floor",
        "soft daylight coming through windows"
      ]
    },
    "lighting": {
      "type": "natural gym lighting",
      "characteristics": [
        "soft highlights on skin",
        "realistic shadows",
        "clean neutral tones"
      ]
    },
    "photography_style": {
      "style": "casual fitness selfie",
      "camera_look": "smartphone front-camera look",
      "depth_of_field": "shallow with background slightly blurred",
      "mood": "fresh, sporty, effortless"
    },
    "render_quality": {
      "realism": "highly photorealistic",
      "detail_level": "high",
      "skin_texture": "natural with visible pores and glow",
      "resolution": "high resolution",
      "color_grading": "clean neutral tones with warm skin balance"
    }
  }
}
```

**Kernmerkmale:**
- Volles Identity Lock Pattern fuer Gesichtsbewahrung
- `photography_style.camera_look: "smartphone front-camera look"` fuer Authentizitaet
- "Sporty glow" Makeup -- minimal aber definiert
- Natuerliches Gym-Licht statt Studio-Setup
- `render_quality` als separater Block mit Skin-Texture-Steuerung

---

## Mirror-Selfie Regeln

Mirror-Selfies haben besondere Anforderungen, die in den Prompts beachtet werden muessen:

1. **Perspektive**: Die Kamera zeigt das Spiegelbild -- `"perspective": "reflection"`. Alles ist spiegelverkehrt.
2. **Flash-Reflexion**: Der Kamera-Blitz erzeugt einen charakteristischen Lichtfleck im Spiegel (`"bright starburst flare from flash"`). Dieser Fleck ist Teil der Authentizitaet.
3. **Smartphone sichtbar**: Das Telefon muss in der Hand des Subjects sichtbar sein (`"objects": "smartphone held in hand"`).
4. **Pose**: Typisch ist "turned over shoulder facing the mirror" oder "body angled, head turned toward mirror".
5. **Hintergrund**: Der Raum hinter dem Subject ist sichtbar und sollte detailliert beschrieben werden (Moebel, Dekoration, Beleuchtung).
6. **Kein separater Camera-Block noetig**: Die Selfie-Perspektive ergibt sich aus der Szenen-Beschreibung.
7. **Activewear-Variante**: Fuer Gym/Fitness Mirror-Selfies zusaetzlich Pose auf Knien oder stehend, enge Sportkleidung, und `"aesthetic": "Influencer lifestyle, casual at-home aesthetic"`.

---

## Kategoriespezifische Tipps

- **Hauttextur ist entscheidend**: Die besten Portrait-Prompts betonen `"natural skin texture"`, `"visible pores"`, `"dewy finish"` -- nicht glattes Plastik-Skin.
- **Augen-Details**: Reflexionen in den Augen (`"realistic reflection"`), Wimpern-Definition und Blickrichtung erhoehen den Realismus massiv.
- **Haar-Physik**: Einzelne Straehnen (`"individual strands defined"`), Baby Hairs und Wind-Effekte machen den Unterschied.
- **Beleuchtung benennen**: Nicht nur "good lighting" -- sondern Key Light Position, Fill Light, und Highlight-Bereiche explizit angeben.
- **Kamera-Spezifikationen**: Konkrete Objektiv-Angaben (85mm f/1.2, 50mm f/1.4) und ISO-Werte erhoehen die Prompt-Qualitaet deutlich.
- **Negative Prompts nutzen**: Besonders bei Close-ups wichtig -- `"cartoon"`, `"illustration"`, `"plastic skin"`, `"beauty filter"` explizit ausschliessen.
- **Aspect Ratio**: Portraits meist 9:16 (vertikal) oder 3:4. Studio-Panels koennen 1:1 sein.

---

## Empfohlene Negative Prompts

Fuer Portrait Photography besonders wirksame Negative Prompts:

```json
{
  "negative_prompt": [
    "cartoon",
    "illustration",
    "anime",
    "3d render",
    "cgi",
    "plastic skin",
    "beauty filter",
    "over-smoothing",
    "face morph",
    "identity drift",
    "bad anatomy",
    "deformed hands",
    "extra fingers",
    "missing limbs",
    "bad proportions",
    "blurred face",
    "distorted eyes",
    "low quality",
    "pixelated",
    "blurry",
    "watermark",
    "text",
    "logo",
    "overexposed",
    "high contrast"
  ]
}
```

**Tipp**: Bei Beauty-Macro-Shots zusaetzlich `"oily skin"`, `"dry skin"`, `"heavy makeup"` ausschliessen. Bei Night-Portraits `"underexposed"` und `"noise artifacts"` hinzufuegen.
