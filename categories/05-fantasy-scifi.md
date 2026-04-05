# Fantasy & Sci-Fi - Prompt-Patterns

> Staerken: Cyberpunk-Portraits, AR-Visualisierungen, Ghibli-inspirierte Fantasy-Szenen, Sci-Fi-Charakterdesign mit cineastischer Beleuchtung. JSON-Struktur dominiert fuer praezise Kontrolle ueber Licht, Kamera und Atmosphaere.

## Empfohlenes Format
JSON (strukturiert mit verschachtelten Objekten fuer Subject, Lighting, Camera, Environment)

## Best Practice Patterns

### Pattern 1: Cyberpunk-Portrait mit cineastischer Beleuchtung
Extrem detailliertes JSON-Schema fuer Neon-beleuchtete Sci-Fi-Portraits. Trennt Subject, Lighting, Camera und Environment in eigene Bloecke fuer maximale Kontrolle ueber die Cyberpunk-Aesthetik.

```json
{
  "Objective": "Generate an ultra-realistic cinematic close-up side-profile portrait with a futuristic cyberpunk atmosphere, deep emotional tension, and dramatic lighting.",

  "Subject": {
    "Gender": "Male",
    "Age_Group": "Young adult",
    "Appearance": {
      "Facial_Structure": {
        "Jawline": "Sharp, sculpted, highly defined",
        "Skin": "Hyper-realistic skin texture with visible pores, subtle imperfections, natural highlights"
      },
      "Expression": "Focused, intense, emotionally charged gaze"
    }
  },

  "Lighting": {
    "Style": "Cyberpunk cinematic lighting",
    "Key_Lights": [
      "Neon rim light from behind",
      "Soft diffused key light on face"
    ],
    "Colors": ["Electric blue", "Neon magenta", "Purple glow"],
    "Contrast": "High contrast with deep shadows and glowing highlights"
  },

  "Camera": {
    "Shot_Type": "Extreme close-up side profile",
    "Lens": "85mm cinematic portrait lens",
    "Depth_of_Field": "Shallow DOF with soft background bokeh",
    "Focus": "Eyes and jawline in razor-sharp focus"
  },

  "Environment": {
    "Background": "Abstract futuristic city lights, blurred neon signs, cyberpunk ambience",
    "Mood": "Dark, intense, futuristic, emotionally powerful"
  },

  "Quality": {
    "Resolution": "8K",
    "Rendering": "Ultra-detailed, photorealistic, cinematic color grading",
    "Style": "High-end movie still, cyberpunk noir"
  }
}
```

### Pattern 2: Augmented Reality im urbanen Setting
Verbindet physische Realitaet mit digitalen AR-Elementen. Besonders stark fuer Tech-Visualisierungen, bei denen holographische Interfaces in reale Umgebungen eingebettet werden.

```json
{
  "A hyper-realistic, cinematic 8k image of a man standing in a bustling street market at night. He is wearing a plain grey t-shirt, green cargo pants, and white sneakers, holding a smartphone. The scene is overlaid with a detailed Augmented Reality (AR) visualization: numerous floating, translucent frosted-glass music player interface cards orbiting the subject in 3D space. The cards feature colorful album artwork, progress bars, and playback controls with a soft, glowing border luminescence (bloom effect). The composition uses depth of field, with some cards blurred in the foreground and others sharp near the subject. The background features authentic street elements: green and yellow auto-rickshaws, shop signs, and warm ambient street lighting contrasting with the cool blue-white glow of the AR interface.",
  "negative_prompt": "coat, blazer, suit, formal wear, cartoon, illustration, low quality, blurry, distorted, bad anatomy, extra limbs, text watermark",
  "subject_attributes": {
    "clothing": "grey t-shirt, green cargo pants, white sneakers",
    "pose": "standing, holding phone"
  },
  "environment": {
    "location": "street market",
    "time": "night",
    "details": "auto-rickshaws, crowds, shop lights"
  },
  "style": "Augmented Reality, Cyberpunk, Cinematic, Photorealistic"
}
```

### Pattern 3: Fantasy-Kreatur trifft Realismus (Ghibli-Stil)
Photorealistisches Rendering einer Fantasy-Szene mit detaillierter JSON-Struktur fuer Subjekte, Umgebung und Lichtstimmung. Ideal fuer Szenen, die reale Personen mit fiktiven Kreaturen kombinieren.

```json
{
  "image_generation_prompt": {
    "full_text": "An ultra-realistic 8K UHD photograph of a rainy night scene at a rural Japanese bus stop. A person is standing, holding a small red umbrella, wearing a red jumpsuit, blue boots, and a yellow t-shirt, looking to the side with an expression of apprehension and curiosity. Beside him, a gigantic, realistic Totoro creature, with wet fur and a leaf on its head, waits in the rain. The setting includes an aged bus stop sign, dense wet forest trees in the background, and the lighting comes from a dim lamppost and the moon, with realistic rain reflections on the wet asphalt. Wide shot. The face must be sharp and expressive.",
    "technical_specs": {
      "medium": "Photograph",
      "resolution": "8K UHD",
      "style": "Ultra-realistic",
      "composition": "Wide shot",
      "focus": "Sharp and expressive face"
    },
    "lighting": {
      "sources": ["Dim lamppost", "Moon"],
      "effects": ["Realistic rain reflections on wet asphalt"]
    },
    "environment": {
      "location": "Rural Japanese bus stop",
      "weather": "Rainy night",
      "background": "Dense wet forest trees",
      "props": ["Aged bus stop sign"]
    },
    "subjects": [
      {
        "type": "Human",
        "build": "Normal",
        "attire": {
          "clothing": "Red jumpsuit, yellow t-shirt",
          "footwear": "Blue boots",
          "accessories": "Small red umbrella"
        },
        "pose": "Standing, looking to the side",
        "expression": "Apprehension and curiosity"
      },
      {
        "type": "Creature",
        "identity": "Gigantic realistic Totoro",
        "details": ["Wet fur", "Leaf on head"],
        "action": "Waiting in the rain"
      }
    ]
  }
}
```

### Pattern 4: Sci-Fi Film-Still mit Rollenspiel-Kontext
Nutzt einen "Role"-Ansatz, bei dem der Prompt als Briefing fuer einen Filmfotografen formuliert wird. Extrem detailliert bei Wardrobe, Lighting und Camera-Specs fuer authentische Sci-Fi-Film-Aesthetik.

```
Role: You are a world-class unit still photographer for high-budget sci-fi films. Your task is to generate a photorealistic cinematic portrait in the visual tone of gritty military sci-fi.

AESTHETIC REQUIREMENTS:
Produce a photorealistic film still with:
- tangible textures (heavy canvas, scratched plastic, grease stains, industrial metal)
- cinematic lighting and organic film grain
- grounded, war-movie atmosphere

STYLE TARGET - THE REBELLION:
Match the gritty, desaturated, boots-on-the-ground military sci-fi aesthetic.
Palette: Industrial greys, dirty orange, olive drab, cold hangar lighting.
Vibe: Determined, weary, functional, ready for combat.

SCENE SETTING:
A cinematic medium shot in a busy Rebel Hangar.
Background: Blurred mechanics, astromech droids, and parts of an X-Wing fighter.
Action: The subject stands holding a rebel pilot helmet under one arm.

WARDROBE (X-Wing Pilot):
Authentic flight gear that serves as a support system, not a costume.
Flight Suit: Iconic orange flight suit made heavy, fire-resistant cotton canvas. It must look worn, stained with grease, and faded.
Vest: A white flak vest with a detailed life-support box on the chest (weathered plastic buttons, thick webbing straps).
Details: Hoses connecting the suit, heavy black gloves, leg flares.

LIGHTING: Industrial hangar lighting.
Mixed color temperatures: Cool fluorescent overhead lights combined with warm practical lights from machinery.
Soft, diffuse light on the face, emphasizing grit and texture.

CAMERA & TEXTURE:
Arri Alexa 65/70s Hybrid aesthetic.
Fine film grain.
Focus on the weave of the canvas suit and the scratches on the helmet.
```

## Kategoriespezifische Tipps
- Cyberpunk-Szenen profitieren von expliziten Farbangaben fuer Neon-Lichter (Electric Blue, Magenta, Purple)
- AR-Visualisierungen benoetigen den "bloom effect" und "frosted-glass" Beschreibungen fuer glaubwuerdige holographische Elemente
- Fantasy-Kreaturen wirken realistischer mit physischen Details wie "wet fur", "visible pores", "rain reflections"
- Sci-Fi-Film-Stills gewinnen durch Weathering-Details: "grease stains", "scratched plastic", "faded fabric"
- Shallow Depth of Field trennt Subjekt von futuristischem Hintergrund

## Empfohlene Negative Prompts
```
cartoon, illustration, low quality, blurry, distorted, bad anatomy, extra limbs, text watermark, coat, blazer, formal wear, anime style, oversaturated neon color, plastic look, CGI artifacts
```
