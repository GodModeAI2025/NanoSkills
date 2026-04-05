# Food & Culinary - Prompt-Patterns

> Staerke dieser Kategorie: Cinematic Food Photography, dynamische Splash-Effekte, Exploded-View-Rezeptdarstellungen, kreative Food-Art-Konzepte. Ideal fuer Restaurant-Marketing, Social-Media-Ads und kulinarische Storytelling-Formate.

## Empfohlenes Format
Hybrid (JSON fuer komplexe Serien mit Varianten, Fliesstext fuer einzelne Hero-Shots)

## Best Practice Patterns

### Pattern 1: Cinematic Food Production Manifest (JSON-Varianten-System)
Dieses Pattern definiert eine komplette Food-Foto-Serie mit Film-Emulation und physikalischen Effekten (Schwerelosigkeit). Besonders stark: Die Aufteilung in technical_stack, artistic_direction und variant_registry fuer verschiedene Geschmacksrichtungen.

```json
{
  "production_manifest": {
    "metadata": {
      "series_id": "CIN-FOOD-2025",
      "aspect_ratio": "9:16",
      "resolution_target": "8k_uhd"
    },
    "technical_stack": {
      "hardware": {
        "camera": "ARRI Alexa 65",
        "lens_profile": "Large format cinematic prime"
      },
      "film_emulation": {
        "stock": "Kodak Portra 400",
        "characteristics": ["Fine grain", "Natural skin tones", "Warm highlights"]
      },
      "lighting_rig": {
        "style": "Cinematic soft glow",
        "atmosphere": "Timeless indoor",
        "diffusion": "High"
      }
    },
    "artistic_direction": {
      "composition_rule": "Graphic centered symmetry",
      "physics_engine": "Suspended animation / Zero gravity",
      "background_specification": "Flat off-white / Studio bone"
    },
    "variant_registry": [
      {
        "id": "VAR-001",
        "flavor_profile": "Dark Chocolate Chip & Oat",
        "tonal_emotion": "Playful, cheeky yet chic",
        "ingredients": {
          "primary_solids": ["Dark chocolate chip cookies"],
          "fluid_fx": ["Oat milk splash"],
          "debris": ["Cookie crumbs"]
        }
      },
      {
        "id": "VAR-002",
        "flavor_profile": "Pistachio Macaron",
        "tonal_emotion": "Refined, playful chic",
        "ingredients": {
          "primary_solids": ["Pistachio macarons"],
          "fluid_fx": ["Cream filling swirls"],
          "debris": ["Crushed pistachio nuts"]
        }
      },
      {
        "id": "VAR-003",
        "flavor_profile": "Strawberry Shortcake",
        "tonal_emotion": "Sweet, playful yet chic",
        "ingredients": {
          "primary_solids": ["Fresh strawberry slices"],
          "fluid_fx": ["Whipped cream swirls"],
          "debris": ["Shortcake biscuit crumbs"]
        }
      }
    ]
  }
}
```

### Pattern 2: Dynamic Hero Shot mit Sauce-Varianten (JSON-Serie)
Dieses Pattern erzeugt dramatische Food-Hero-Shots mit dynamischen Saucen-Effekten. Jede Variante hat ein eigenes Thema mit spezifischer Sauce, Akzenten und Hintergrundfarbe. Besonders wertvoll: Die fertigen full_string Prompts.

```json
{
  "food_photography_series": {
    "subject": "Fried Chicken Thigh",
    "technical_specs": {
      "style": "Hyper-realistic hero shot",
      "aspect_ratio": "3:4",
      "lighting": "Cinematic / Studio"
    },
    "variations": [
      {
        "theme": "Tartar Refresh",
        "sauce": "Thick tartar sauce",
        "accents": ["capers", "dill", "chopped pickles"],
        "background": "Bright lemon-yellow",
        "prompt": "Hyper-realistic hero shot of a fried chicken thigh in midair with thick tartar sauce bursting around it, flecks of capers, dill, and chopped pickles frozen in motion. The sauce flows like creamy waves, dancing around the crispy surface. Bright lemon-yellow background with moody studio backlight creates a gourmet, refreshing tone ultra-detailed commercial look, --ar 3:4"
      },
      {
        "theme": "Smoked Cheese Indulgence",
        "sauce": "Molten smoked cheese fondue",
        "accents": ["golden crouton crumble"],
        "background": "Creamy yellow with taupe haze",
        "prompt": "Hyper-realistic hero shot of a crisp fried chicken thigh surrounded by a molten splash of smoked cheese fondue mid-air, with bits of golden crouton crumble suspended in orbit. Deep lighting creates dimensional drama on the crispy crust. The backdrop blends creamy yellow with taupe haze indulgent cheese-forward visual, --ar 3:4"
      },
      {
        "theme": "Miso Umami",
        "sauce": "Miso butter glaze and umami cream",
        "accents": ["toasted seaweed powder", "sesame seeds"],
        "background": "Muted beige",
        "prompt": "Hyper-realistic hero shot of a rich fried chicken thigh hovering mid-air, glazed with miso butter and surrounded by a dynamic splash of umami cream, flecked with toasted seaweed powder and sesame seeds. Dramatic soft shadows sculpt the skin texture. Muted beige background, clean and warm umami-focused food ad, --ar 3:4"
      }
    ]
  }
}
```

### Pattern 3: Exploded-View Ingredient Breakdown (Fliesstext)
Dieses Pattern zerlegt ein Gericht in seine Einzelteile mit Infografik-Annotationen. Besonders stark fuer Menu-Design, Marketing-Material und Food-Education-Content.

```
Exploded view of the same [dish], presented as a clean, commercial recipe-style breakdown.
Exactly five ingredients, separated and arranged vertically from top to bottom, evenly spaced and perfectly aligned.

Ingredient order (top to bottom):

Fresh tomato salsa -- 40 g

Shredded cheddar cheese -- 30 g

Grilled chicken pieces -- 80 g

Crisp lettuce -- 25 g

Soft wheat taco tortilla -- 60 g (bottom base)

Add clear infographic-style annotations for each ingredient.
Each annotation includes the ingredient name and its exact weight in grams, written exactly as listed above.

Annotation design guidelines:
- Clean sans-serif font, medium weight
- Text placed inside minimal frames or boxes
- Thin, precise connector lines pointing directly to each ingredient
- High readability, no overlap, no decorative excess
- Structured vertical layout, like a modern recipe card

Background is light, neutral, and optimized for text clarity and visual cleanliness.
Overall style is minimal, instructional, and commercial, suitable for marketing, explainer visuals, and product breakdowns.
```

### Pattern 4: Culinary Atlas -- Globale Rezept-Exploration (Instruktions-Prompt)
Dieses Pattern erstellt eine visuelle "Kulinarische Weltkarte" mit historischen Skizzen und 3D-Pop-up-Dioramen. Besonders kreativ: Die Kombination aus 2D-Vintage-Illustration und 3D-Miniatur-Szenen.

```
<instruction>
Inputs: Ingredients = [User Choice, e.g., Chicken, Bacon]

Step 1: Global Analysis
Analyze the ingredients.
Select 4 Distinct Countries with a famous dish using these ingredients  

Goal: A "Culinary Atlas" Grid showing 4 different cultural variations of the ingredients.

Layout Rule:
Output Format: A 2x2 Grid.
Content per Panel: Each of the 4 panels must show a Single Open Book Spread for that specific country.

Inside Each Panel (The Book Spread Rule):
Left Page (The History): 2D Vintage Sepia Sketches. A visual timeline or illustrated recipe of the dish (e.g., "1850 -> 1920 -> Today"). Flat, ink-drawn style.
Right Page (The Reality): 3D Pop-up Diorama. The finished, steaming meal emerges physically from the page. A tiny miniature chef from that country is standing on the page next to the massive food.
Consistency: All 4 books should look like part of the same series, but with different cultural contents.

Lighting: Cinematic top-down lighting, highlighting the depth difference between the flat left page and the 3D right page.
Output: 2x2 Grid, High Definition, Macro Detail.
</instruction>
```

## Kategoriespezifische Tipps
- "Suspended animation / Zero gravity" erzeugt die beliebtesten Food-Shots mit schwebenden Zutaten
- Splash-Effekte immer als "frozen in motion" beschreiben fuer scharfe Details
- Warme Hintergrundfarben (Lemon-Yellow, Amber, Warm Beige) verstaerken den Appetit-Effekt
- Film-Emulation (Kodak Portra 400) gibt Food-Fotos einen authentischen, warmen Look
- Exploded-View-Formate funktionieren hervorragend fuer Ingredient-Breakdowns und Menu-Design
- "Cinematic soft glow" + "High diffusion" ist die Standard-Beleuchtung fuer Premium-Food-Fotografie
- Aspect Ratios: 3:4 fuer Food-Editorial, 9:16 fuer Social-Media, 1:1 fuer Restaurant-Menus

## Empfohlene Negative Prompts
```
cartoon, low quality, blurry, flat lighting, amateur, unappetizing colors, cold blue tones, plastic-looking food, dry textures, oversaturated, watermark, signature, ugly plating, messy composition, unrealistic food textures, burnt edges, undercooked appearance
```
