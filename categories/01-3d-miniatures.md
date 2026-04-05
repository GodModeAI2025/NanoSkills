# 3D Miniatures & Dioramas - Prompt-Patterns

> Staerke dieser Kategorie: Tilt-Shift-Fotografie, Miniatur-Welten mit uebergrossen Produkten, Konstruktions-Szenarien mit winzigen Arbeitern, isometrische Stadtszenen. Ideal fuer Brand-Marketing, Storytelling und surreale Produktinszenierung.

## Empfohlenes Format
JSON (strukturierte Szenen-Definitionen mit Subject, Environment, Style, Parameters)

## Best Practice Patterns

### Pattern 1: Chibi-Style Concept Store (Fliesstext-Template)
Dieses Pattern verwandelt jede Marke in einen charmanten Miniatur-Laden. Es nutzt Cinema 4D Aesthetik mit Blind-Box-Toy-Stil. Besonders stark: Die Verbindung von Markenidentitaet mit architektonischem Design.

```
{Brand Name}

--- Prompt ---

3D chibi-style miniature concept store of {Brand Name}, creatively designed with an exterior inspired by the brand's most iconic product or packaging (such as a giant {brand's core product, e.g., chicken bucket/hamburger/donut/roast duck}). The store features two floors with large glass windows clearly showcasing the cozy and finely decorated interior: {brand's primary color}-themed decor, warm lighting, and busy staff dressed in outfits matching the brand. Adorable tiny figures stroll or sit along the street, surrounded by benches, street lamps, and potted plants, creating a charming urban scene. Rendered in a miniature cityscape style using Cinema 4D, with a blind-box toy aesthetic, rich in details and realism, and bathed in soft lighting that evokes a relaxing afternoon atmosphere. --ar 2:3

Brand name: Starbucks
```

### Pattern 2: Miniature Construction Crew (JSON-Multi-Szenen)
Dieses Pattern inszeniert uebergrosse Produkte als Baustellen mit winzigen Arbeitern. Die JSON-Struktur erlaubt mehrere Varianten in einem Prompt. Besonders effektiv: Die Kombination aus Tilt-Shift-Fotografie und surrealer Groessenverschiebung.

```json
{
  "midjourney_prompts": [
    {
      "id": 1,
      "title": "Sculpting the Drumstick",
      "content": {
        "core_scene": "A surreal, hyper-realistic scene featuring miniature construction workers sculpting a giant crispy drumstick using tiny tools and ladders.",
        "details": "The drumstick rests on a branded box with a company logo.",
        "lighting_and_tone": "Warm studio lighting, playful and imaginative tone."
      },
      "parameters": {
        "aspect_ratio": "51:91",
        "stylize": 150
      },
      "full_string": "A surreal, hyper-realistic scene featuring miniature construction workers sculpting a giant [crispy drumstick] using tiny tools and ladders. the [drumstick] rests on a branded box with a company logo. warm studio lighting, playful and imaginative tone. --ar 51:91 --stylize 150"
    },
    {
      "id": 2,
      "title": "Fries Construction Site",
      "content": {
        "core_scene": "A surreal, hyper-realistic scene of miniature workers operating tiny forklifts and conveyor belts to pile up giant fries in a branded red carton.",
        "details": "Some workers spray golden shine on the fries, others climb ladders to arrange them neatly.",
        "lighting_and_tone": "Cinematic warm studio lighting, playful food art vibe."
      },
      "parameters": {
        "aspect_ratio": "51:91",
        "stylize": 150
      },
      "full_string": "A surreal, hyper-realistic scene of miniature workers operating tiny forklifts and conveyor belts to pile up giant fries in a branded red carton. Some workers spray golden shine on the fries, others climb ladders to arrange them neatly. Cinematic warm studio lighting, playful food art vibe. --ar 51:91 --stylize 150"
    }
  ]
}
```

### Pattern 3: Isometrische Miniatur-Stadt (Fliesstext)
Dieses Pattern erzeugt detaillierte 3D-Cartoon-Staedte mit Wetter-Integration und typografischen Elementen. Besonders nuetzlich fuer Social-Media-Content und Reise-Themen.

```
Present a clear, 45° top-down isometric miniature 3D cartoon scene of [CITY], featuring its most iconic landmarks and architectural elements. Use soft, refined textures with realistic PBR materials and gentle, lifelike lighting and shadows. Integrate the current weather conditions directly into the city environment to create an immersive atmospheric mood.
Use a clean, minimalistic composition with a soft, solid-colored background.

At the top-center, place the title "[CITY]" in large bold text, a prominent weather icon beneath it, then the date (small text) and temperature (medium text).
All text must be centered with consistent spacing, and may subtly overlap the tops of the buildings.
Square 1080x1080 dimension.
```

### Pattern 4: Sneaker-Monument Engineering (JSON-Szenen-System)
Dieses Pattern behandelt Sneaker als architektonische Monumente mit detaillierten Szenen-Definitionen. Besonders stark: Die Aufteilung in global_style_profile und individuelle Szenen mit technischen Parametern.

```json
{
  "project_title": "Miniature Engineering: The Sneaker Colossus Series",
  "global_style_profile": {
    "aesthetic": "Hyper-realistic, cinematic commercial, macro photography",
    "rendering_engine": "Octane Render / Unreal Engine 5.4",
    "color_grading": "High-contrast, professional studio finish"
  },
  "prompts": [
    {
      "scene_id": "monument_blackout",
      "concept": "The sneaker as a sacred architectural monument.",
      "visual_description": {
        "subject": "A massive, towering sneaker standing vertically like a skyscraper.",
        "characters": "Dozens of tiny engineers and designers in high-visibility gear, utilizing intricate industrial scaffolding to access the upper collars.",
        "actions": "Workers using miniature spray-paint rigs on the panels, laser-leveling the swoosh, and using heavy-duty sewing machinery on the leather seams.",
        "environment": "Void-like black studio background to emphasize the scale and texture of the sneaker.",
        "lighting": "Dramatic rim lighting, cinematic shadows, and sharp studio spotlights highlighting the premium leather grain."
      },
      "technical_parameters": {
        "aspect_ratio": "2:3",
        "stylize": 250,
        "detail_level": "Ultra-detailed textures, 8k resolution, creative surrealism"
      }
    },
    {
      "scene_id": "warehouse_sole_maintenance",
      "concept": "Industrial-scale cleaning of a pristine classic.",
      "visual_description": {
        "subject": "A colossal, pristine white sneaker occupying a warehouse floor.",
        "characters": "Miniature maintenance crew in orange safety vests; a team is pressure-washing the tread of the sole while another group uses toothbrush-sized tools to scrub the stitching.",
        "environment": "Smooth warehouse floor with atmospheric haze and wide industrial windows.",
        "lighting": "Side-lit by soft daylight, creating realistic volume and highlighting the leather texture."
      },
      "technical_parameters": {
        "aspect_ratio": "9:16",
        "resolution": "4K Realism",
        "mood": "Cinematic commercial tone, crisp and clean"
      }
    }
  ]
}
```

## Kategoriespezifische Tipps
- Tilt-Shift-Effekte verstaerken den Miniatur-Eindruck enorm -- immer "shallow depth of field" und "tilt-shift" erwaehnen
- Miniatur-Arbeiter in Sicherheitswesten (orange, pink, gelb) erhoehen die visuelle Lesbarkeit der Szene
- Cinema 4D und Octane Render als Rendering-Engine erwaehnen fuer konsistente 3D-Aesthetik
- "Blind-box toy aesthetic" erzeugt den charakteristischen Chibi-Miniatur-Look
- Aspect Ratios: 2:3 oder 51:91 (vertikal) funktionieren am besten fuer Miniatur-Szenen
- Warm studio lighting + cinematic shadows sind die Standard-Beleuchtung fuer diese Kategorie

## Empfohlene Negative Prompts
```
blurry, low quality, flat lighting, 2D, cartoon style, unrealistic proportions, oversaturated, noisy, pixelated, amateur rendering, inconsistent scale between miniature figures
```
