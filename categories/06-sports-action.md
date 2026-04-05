# Sports & Action - Prompt-Patterns

> Staerken: Authentische Fitness-Fotografie, Sport-Action-Szenen, Selfie-Aesthetik mit kontextgerechten Details. JSON-Struktur mit besonderem Fokus auf realistische Unvollkommenheiten, kontextgerechte Accessoires und natuerliche Smartphone-Fotografie.

## Empfohlenes Format
JSON (tief verschachtelt mit Subject, Accessories, Photography, Background als Hauptbloecke)

## Best Practice Patterns

### Pattern 1: Fitness/Gym-Szene mit Lifestyle-Authentizitaet
Umfassendes JSON-Template fuer Gym-Content. Besonderer Fokus auf kontextgerechte Details: Schweiss, zerzauste Haare, minimales Makeup. Demonstriert die "Action-based Description"-Methode statt statischer Posen.

```json
{
  "subject": {
    "description": "A young woman sitting on yoga mat, wiping sweat with towel, holding water bottle",
    "mirror_rules": "N/A - direct gym photo",
    "age": "late 20s",
    "expression": "accomplished, slight breathlessness, confident smile",
    "hair": {
      "color": "blonde with highlights",
      "style": "high ponytail, slightly messy with flyaways from workout"
    },
    "clothing": {
      "top": {
        "type": "sports bra",
        "color": "dusty rose pink",
        "details": "medium support, strappy back detail, moisture visible from sweat"
      },
      "bottom": {
        "type": "high-waisted leggings",
        "color": "black with mesh panels",
        "details": "ankle length, mesh cutouts on calves, compression fit"
      }
    },
    "face": {
      "preserve_original": true,
      "makeup": "minimal, dewy from workout, natural flushed cheeks, no eye makeup"
    }
  },
  "accessories": {
    "headwear": {
      "type": "none",
      "details": "hair pulled back in scrunchie"
    },
    "jewelry": {
      "earrings": "small diamond studs",
      "necklace": "none",
      "wrist": "rose gold fitness tracker, black hair ties on wrist",
      "rings": "none"
    },
    "device": {
      "type": "smartphone",
      "details": "propped against dumbbell, recording workout selfie"
    },
    "prop": {
      "type": "insulated water bottle",
      "details": "matte black 32oz bottle with motivational quote sticker, condensation visible"
    }
  },
  "photography": {
    "camera_style": "gym selfie aesthetic, smartphone front camera",
    "angle": "slightly above eye level, sitting position",
    "shot_type": "full upper body and crossed legs, centered composition",
    "aspect_ratio": "9:16 vertical",
    "texture": "crisp detail, bright gym lighting, energetic feel"
  },
  "background": {
    "setting": "modern gym studio",
    "wall_color": "light gray with motivational mural",
    "elements": [
      "purple yoga mat laid out",
      "set of dumbbells scattered nearby",
      "white towel draped over shoulder",
      "blurred gym equipment in background",
      "large mirror reflecting back wall",
      "resistance bands coiled on floor"
    ],
    "atmosphere": "energetic, accomplished, health-focused",
    "lighting": "bright overhead LED gym lighting, even coverage"
  }
}
```

### Pattern 2: Miniatur-Sport-Szene auf Smartphone
Kreatives Konzept-Prompt fuer eine Miniatur-Sportszene, die aus einem Smartphone herausbricht. Zeigt wie man hyper-realistische Konzeptbilder mit detaillierten Material- und Rendering-Spezifikationen erstellt.

```json
{
  "type": "image_generation",
  "style": "hyper_realistic",
  "quality": "8K DSLR",
  "aspect_ratio": "4:5",
  "camera": {
    "angle": "slightly tilted cinematic perspective",
    "lens": "50mm DSLR",
    "depth_of_field": "shallow",
    "focus": "smartphone and football action"
  },
  "scene": {
    "setting": "smartphone placed on a wooden table",
    "concept": "phone screen transformed into a miniature football stadium",
    "environment": "indoor, soft daylight coming from the side",
    "atmosphere": "cinematic, immersive, realistic"
  },
  "details": {
    "screen": "weathered green football pitch with visible wear, dirt patches, and grass texture",
    "players": "miniature football players actively playing a match with dynamic poses",
    "lighting": "soft diffused daylight with subtle lens flares and realistic reflections",
    "realism_effects": [
      "fingerprints on screen",
      "light scratches on phone body",
      "natural smudges",
      "micro dust particles"
    ]
  },
  "materials": {
    "phone": "metallic frame with realistic reflections",
    "table": "textured wooden surface with warm tones"
  },
  "mood": "high-end cinematic, dramatic, premium advertising look",
  "rendering": {
    "sharpness": "ultra sharp",
    "texture_detail": "extreme",
    "lighting_quality": "studio grade",
    "photorealism": true
  }
}
```

### Pattern 3: Motorsport/Racing-Szene mit Editorial-Aesthetik
Detailliertes JSON fuer professionelle Sport-Portraitfotografie im Motorsport-Kontext. Zeigt wie man cineastische Action-Szenen mit Fashion-Editorial-Qualitaet kombiniert.

```json
{
  "type": "image_generation_prompt",
  "style": "hyper-realistic, cinematic motorsport photography",
  "subject": {
    "pose": {
      "stance": "standing confidently on the race grid",
      "posture": "upright, professional, composed",
      "hands": "holding a Formula 1 helmet in one hand"
    },
    "expression": "focused, confident, calm",
    "appearance": {
      "wardrobe": {
        "outfit": "official Formula 1 driver racing suit, red with sponsor details"
      },
      "accessories": [
        "F1 helmet held at the side"
      ]
    }
  },
  "environment": {
    "location": "Formula 1 race grid",
    "elements": [
      "Formula 1 car positioned beside the subject",
      "asphalt track markings",
      "pit lane and grid details",
      "subtle background crew and equipment (softly blurred)"
    ]
  },
  "lighting": {
    "type": "natural daylight",
    "quality": "bright and cinematic",
    "effects": [
      "realistic highlights on racing suit and helmet",
      "natural shadows on the ground",
      "reflections on the car body"
    ]
  },
  "camera": {
    "framing": "full-body shot",
    "angle": "eye-level to slightly low angle",
    "lens_look": "85mm motorsport editorial style",
    "depth_of_field": "moderate, subject in sharp focus with softly blurred background"
  },
  "color_grading": {
    "palette": ["Ferrari red", "black", "white", "metallic highlights"],
    "contrast": "balanced and dynamic",
    "saturation": "rich but realistic"
  },
  "mood": {
    "atmosphere": "powerful, professional, high-performance",
    "tone": "elite motorsport confidence"
  },
  "quality": {
    "resolution": "8K",
    "realism": "ultra-photorealistic",
    "detail_level": "high detail in fabric, helmet texture, car paint, and asphalt"
  }
}
```

### Pattern 4: Multi-Panel Workout Grid
Template fuer mehrteilige Fitness-Collagen. Demonstriert wie man konsistente Subjekte ueber mehrere Panels hinweg erzeugt, mit unterschiedlichen Posen und Uebungen in einem einzigen Prompt.

```json
{
  "scene": {
    "layout": "1x3_grid",
    "aspect_ratio": "3:2",
    "background": "modern_fitness_gym_with_neutral_lighting",
    "style": "hyper_realistic_photography"
  },
  "subject": {
    "description": "the same athletic woman from the reference image",
    "appearance_consistency": true,
    "outfit": "black_sports_bra_and_black_gym_leggings",
    "physique": "fit_toned_and_athletic"
  },
  "frames": [
    {
      "index": 1,
      "title": "Mirror Selfie",
      "action": "woman turning slightly, showing her back in a gym mirror",
      "pose": "one hand holding smartphone, other hand on hip",
      "expression": "neutral_confident",
      "camera": "mirror reflection view, front camera angle",
      "details": ["defined back muscles", "clean gym mirror", "sharp focus"]
    },
    {
      "index": 2,
      "title": "Squat",
      "action": "woman performing a proper squat",
      "pose": "feet shoulder width apart, hips lowered, back straight",
      "expression": "focused",
      "camera": "side angle to show form",
      "details": ["muscle engagement visible", "dynamic tension", "realistic shadows"]
    },
    {
      "index": 3,
      "title": "Cable Cross",
      "action": "woman doing cable crossover exercise",
      "pose": "arms extended forward, slight forward lean",
      "expression": "determined",
      "camera": "front three-quarter view",
      "details": ["defined shoulders and chest activation", "cable tension visible", "high clarity"]
    }
  ],
  "visual_style": {
    "sharpness": "ultra_high",
    "skin_tones": "natural",
    "color_grade": "clean_modern_fitness_palette",
    "depth_of_field": "medium_shallow_to_emphasize_subject"
  }
}
```

## Kategoriespezifische Tipps
- Immer aktionsbasierte Beschreibungen verwenden ("wiping sweat", "holding racket") statt statischer Posen ("standing confidently")
- Authentische Unvollkommenheiten einbauen: "flyaways from workout", "moisture visible from sweat", "natural flushed cheeks"
- Accessoires muessen zum Kontext passen: Fitness-Tracker im Gym, KEINE Luxus-Schmuckstuecke
- Bei Mirror-Selfies immer `mirror_rules` angeben fuer korrekte Textdarstellung
- Einfache Kamera-Sprache nutzen: "smartphone front camera" statt "f/1.8 aperture, 3200K"
- Background-Elemente als Arrays strukturieren fuer mehr Kontrolle
- Bei Multi-Panel-Layouts `appearance_consistency: true` setzen

## Empfohlene Negative Prompts
```
Indoor (when outdoor needed), night (when daylight), blurry, out of focus, multiple subjects (when single), cartoon, illustration, low quality, distorted, bad anatomy, extra limbs, oversized accessories, formal wear in gym setting
```
