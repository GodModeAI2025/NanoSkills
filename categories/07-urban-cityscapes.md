# Urban Cityscapes - Prompt-Patterns

> Staerken: Stadtlandschaften mit cineastischer Beleuchtung, 3D-Billboard-Illusionen, Zeitreise-Splits, illustrative Stadtszenen und Landmark-Aerial-Fotografie. Mischung aus JSON und Fliesstext-Prompts je nach Komplexitaet.

## Empfohlenes Format
Hybrid (JSON fuer komplexe Szenen mit vielen Parametern, Fliesstext fuer Template-basierte Prompts mit Platzhaltern)

## Best Practice Patterns

### Pattern 1: Cozy Storybook Stadtszenen-Illustration
Umfassendes Design-System als JSON fuer handgezeichnete Illustrationen im Kinderbuch-Stil. Definiert Medium, Farbtheorie, Linienarbeit und Atmosphaere als verschachtelte Parameter mit zwei Prompt-Varianten (Buntstift und Aquarell-Mix).

```json
{
  "design_system": {
    "visual_parameters": {
      "medium": {
        "primary": "Colored Pencil",
        "secondary": "Watercolor Wash (Variation only)",
        "application": "Hand-drawn",
        "texture": {
          "type": "Visible pencil strokes",
          "quality": "Slightly rough outlines",
          "finish": "Non-realistic / No photo texture"
        }
      },
      "line_work": {
        "style": "Clean line art",
        "weight": "Slightly rough/organic",
        "clarity": "High"
      },
      "color_theory": {
        "base_tone": "Warm and friendly",
        "palette_type": "Vibrant Pastel",
        "adjustments": {
          "brightness": "Increased / High-key",
          "saturation": "Enhanced but natural",
          "contrast": "Soft"
        }
      },
      "lighting_and_shading": {
        "shadows": "Minimal",
        "highlights": "Soft",
        "rendering": "Flat yet detailed",
        "gradients": "Subtle watercolor layers (Variation only)"
      }
    },
    "subject_geometry": {
      "anatomy": {
        "proportions": "Semi-cartoon realistic",
        "scale": "Storybook style"
      },
      "facial_features": {
        "eyes": "Dot style",
        "mouth": "Small smile",
        "complexity": "Simple / Minimalist"
      }
    },
    "atmosphere": {
      "mood": ["Cozy", "Cheerful", "Warm", "Friendly"],
      "genre_tags": ["Children's Book", "Lifestyle Sketch", "Storybook Illustration"]
    }
  },
  "generation_configs": {
    "negative_prompt_tokens": [
      "realism", "photorealistic", "photo texture",
      "dark colors", "complex shading", "3d render"
    ],
    "prompt_variations": [
      {
        "variant_name": "Textured Colored Pencil",
        "full_text": "Illustration style: hand-drawn colored pencil illustration, clean line art with slightly rough pencil outlines, soft pastel coloring with increased brightness, lighter and more vivid color tones, enhanced saturation while staying natural, visible pencil strokes and gentle shading texture, warm and friendly tone, semi-cartoon realistic proportions, simple facial features with dot eyes and small smiles, flat yet detailed coloring, minimal shadows, soft highlights, storybook illustration feel, cozy and cheerful atmosphere, vibrant yet soft color palette, children-book / lifestyle sketch style, high clarity, no realism, no photo texture"
      },
      {
        "variant_name": "Mixed Media Watercolor",
        "full_text": "Hand-drawn colored pencil illustration with clean line art and slightly rough pencil outlines, combined with soft watercolor wash textures. Bright pastel colors, lighter and more vivid tones with natural saturation. Visible pencil strokes layered with subtle watercolor gradients. Warm and friendly tone, semi-cartoon realistic proportions. Simple facial features with dot eyes and small smiles. Flat yet detailed coloring, minimal shadows, soft highlights. Storybook illustration feel, cozy and cheerful atmosphere, children-book style, high clarity, no realism, no photo texture."
      }
    ]
  }
}
```

### Pattern 2: Landmark Aerial-Fotografie (Template mit Platzhaltern)
Hochdetailliertes Template fuer Drohnen-Luftaufnahmen von Landmarks. Nutzt Platzhalter-Variablen fuer flexible Anwendung auf beliebige Wahrzeichen. Besonderer Fokus auf physikalisch korrekte Beleuchtung und realistische Drohnen-Perspektiven.

```json
{
  "customInputs": {
    "landmark": "{INSERT_LANDMARK_NAME}",
    "aspectRatio": "{INSERT_ASPECT_RATIO}",
    "timeOfDay": "{INSERT_TIME_OF_DAY}",
    "weather": "{INSERT_WEATHER_CONDITION}"
  },
  "promptDetails": {
    "description": "A completely real, ultra high resolution aerial photograph of {INSERT_LANDMARK_NAME} captured exactly as it exists today. The image must look exactly like a true professional aerial photograph. All lighting, geography, environment, structures and materials must remain fully accurate to real life.",
    "defaultLogic": {
      "aspectRatio": "If empty, default to 3:2.",
      "timeOfDay": "If empty, default to golden hour daytime.",
      "weather": "If empty, default to a perfect golden hour sunset atmosphere with clear skies, warm tones and maximum natural visibility."
    },
    "angleAndComposition": "The camera angle must be a physically real, legally flyable, aesthetically optimal oblique aerial angle that emphasizes the landmark as the primary subject. Use real world framing principles such as rule of thirds, true horizon placement, natural leading lines and authentic depth cues.",
    "realisticSunPhysics": "Sun position must follow real-world solar physics. Golden hour sunlight must have a real azimuth between 15 and 35 degrees above the horizon. Sky gradients must follow atmospheric Rayleigh scattering rather than artistic effects.",
    "realisticDroneAltitude": "The drone altitude must stay within realistic flight limits between 30 meters and 150 meters. The horizon line, perspective compression, and foreground scale relationships must reflect a real, physically achievable drone altitude.",
    "camera": {
      "equipment": "Professional cinema drone with full frame 8K camera.",
      "lens": "24mm rectilinear wide-angle lens with zero distortion.",
      "settings": "8K RAW-equivalent clarity, native ISO for clean shadows and balanced exposure."
    },
    "stylization": "Zero stylization. Only real-life photographic tonality. Pure documentary-level realism."
  },
  "negativePrompt": "hallucinated architecture, invented buildings, fictional modifications, impossible angles, unrealistic lighting, incorrect shadow direction, surreal clouds, neon skies, artificial bloom, painterly textures, CGI artifacts, false reflections, oversharpened edges, warped geometry, fantasy weather"
}
```

### Pattern 3: 3D-Billboard-Illusion in der Stadt
Fliesstext-Template fuer die Erstellung von gigantischen 3D-Displays, die aus Gebaeudefassaden herauszubrechen scheinen. Nutzt ein modulares Scene-Description-System fuer flexible Inhalte.

```
An enormous L-shaped glasses-free 3D LED screen situated prominently at a bustling urban intersection, designed in an iconic architectural style reminiscent of Shinjuku in Tokyo or Taikoo Li in Chengdu. The screen displays a captivating glasses-free 3D animation featuring [scene description]. The characters and objects possess striking depth and appear to break through the screen's boundaries, extending outward or floating vividly in mid-air. Under realistic daylight conditions, these elements cast lifelike shadows onto the screen's surface and surrounding buildings. Rich in intricate detail and vibrant colors, the animation seamlessly integrates with the urban setting and the bright sky overhead.

----
scene description:
[An adorable giant kitten playfully paws at passing pedestrians, its fluffy paws and curious face extending realistically into the space around the screen.]
```

### Pattern 4: Zeitreise-Split-Screen (Zwei-Epochen-Verschmelzung)
Template fuer cineastische Split-Screens, die historische und moderne Versionen derselben Szene nahtlos verschmelzen. Stark parametrierbar durch Szene, Epoche-A und Epoche-B Platzhalter.

```
A horizontal split-screen cinematic shot of {Scene}, seamlessly blending two different eras: {Era_A} on the left and {Era_B} on the right (default: about 100 years ago vs. present day).

On the left side ({Era_A}): show era-appropriate architecture, interior or environment design, materials, vehicles, and props that clearly belong to that historical period. People wear authentic clothing from {Era_A}, including hairstyles, accessories, and typical items in their hands.

On the right side ({Era_B}): show the same {Scene} in the modern era, with updated architecture or renovated structures, contemporary materials (glass, steel, LED screens, modern furniture), modern vehicles or equipment, and current technology (smartphones, laptops, cameras).

In the center: the two eras merge and overlap organically, without a hard dividing line. Elements from {Era_A} and {Era_B} visually interact: people from different times look at each other, walk through each other's space, or seem surprised by the other era's technology. Architecture and environment smoothly morph from old to new.

Make sure the scene is not just a simple left/right comparison but a dynamic time-travel interaction where buildings, clothing, props, and human gestures clearly emphasize the contrast and fusion between the two eras. Photorealistic, 8k resolution, cinematic lighting, wide angle, highly detailed textures, rich sense of time-travel storytelling.

---
SCENE: Times Square, New York
Era Comparison: 1920s and present day
Aspect Ratio: 4:3
```

## Kategoriespezifische Tipps
- Fuer Landmark-Aufnahmen immer physikalisch korrekte Lichtverhaeltnisse angeben (Sonnenposition, Schattenwurf)
- 3D-Billboard-Szenen leben von der Interaktion zwischen digitalem Content und realen Passanten
- Split-Screen-Zeitreisen funktionieren am besten mit einer organischen Uebergangszone in der Mitte
- Stadtszenen brauchen "crowd" Details: natuerliche Bewegung, unterschiedliche Kleidung, candid poses
- Bei illustrativen Styles explizit "no realism, no photo texture" im Negative Prompt angeben

## Empfohlene Negative Prompts
```
cartoon (bei Foto-Stil), anime, illustration (bei Foto-Stil), cgi look, low quality, blur, distorted buildings, fake lighting, over-saturated colors, hallucinated architecture, invented buildings, warped geometry, realism (bei Illustrations-Stil), photorealistic (bei Illustrations-Stil)
```
