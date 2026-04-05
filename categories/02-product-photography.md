# Product Photography - Prompt-Patterns

> Staerke dieser Kategorie: Hyper-realistische Produktinszenierung, cinematic Beleuchtung, dynamische Splashes und Effekte, Luxury-Aesthetik. Ideal fuer Getraenke, Kosmetik, Sneaker, Parfuem und Tech-Produkte.

## Empfohlenes Format
JSON (detaillierte Produktspezifikationen mit Lighting-Design, Kamera-Einstellungen und Material-Definitionen)

## Best Practice Patterns

### Pattern 1: Cinematic Beverage Photography (JSON-Manifest)
Dieses Pattern erzeugt hyper-realistische Getraenke-Produktfotos mit detaillierten Kamera- und Licht-Spezifikationen. Besonders stark: Die Aufteilung in primary_subject, dynamic_environment und cinematography_specs.

```json
{
  "image_generation_manifest": {
    "meta_directives": {
      "output_format": {
        "aspect_ratio": "9:16 (Vertical)",
        "resolution": "4K",
        "aesthetic": "Hyper-realistic cinematic product photography"
      }
    },
    "primary_subject": {
      "product_identity": {
        "brand": "[Brand Name]",
        "flavor": "[Flavor]",
        "container": "Classic 330 ml aluminum can",
        "finish": "Matte-finish aluminum"
      },
      "positional_state": {
        "physics": "Suspended in mid-air, weightless, no supports.",
        "orientation": "Logo centered and sharp."
      },
      "condition_details": {
        "temperature": "Ice-cold",
        "surface_effects": {
          "condensation": "Dense coverage of ultra-fine droplets, organic streaks, and crystal-clear refractions.",
          "atmosphere": "Subtle chill misting and light diffusion around the edges suggesting weight."
        }
      }
    },
    "dynamic_environment": {
      "foreground_activity": {
        "organic_elements": "Fine plant hairs and upward-stretching vines.",
        "moisture_dynamics": "Moisture droplets beading and dripping from fine plant hairs mid-air.",
        "light_dynamics": [
          "Faint ember-like pulses within some vines, alive with warmth.",
          "Vines glow subtly like lava-veined roots due to rim lighting."
        ]
      },
      "background_context": {
        "scenery": "Blurred silhouette of an overgrown infernal forest or deep alien undergrowth.",
        "atmospheric_conditions": "Obscured in fog and cinematic haze.",
        "mood_indicators": "Pulses with heat and shadow, suggesting tension and drama."
      }
    },
    "cinematography_specs": {
      "optical_configuration": {
        "lens": "100 mm Macro",
        "aperture": "f/8",
        "depth_of_field": "Shallow"
      },
      "focus_map": {
        "sharp_plane": ["Logo", "Can Condensation", "Closest Vine Textures"],
        "blur_plane": ["Background melting into smooth atmospheric bokeh"]
      },
      "composition_rules": {
        "framing": "Frontal cinematic close-up with slight upward angle (Heroic Framing).",
        "layout": "Negative space below the can with vines stretching upward.",
        "intent": "Emphasize scale and impact without overpowering the subject."
      }
    },
    "lighting_design": {
      "scheme": "Dual-tone rim setup",
      "sources": {
        "key_left": {
          "color_temp": "Cool white (~5600 K)",
          "purpose": "Accentuate metallic highlights and water beads."
        },
        "rim_right": {
          "color_tone": "Deep red-orange",
          "purpose": "Create lava-veined root glow effect on vines."
        }
      }
    }
  }
}
```

### Pattern 2: Beauty Product Editorial (JSON mit Negative Prompts)
Dieses Pattern ist optimiert fuer Kosmetik-Produktfotografie mit extremer Detailtreue. Besonders wertvoll: Die integration von negative_prompt und quality_rules direkt im JSON.

```json
{
  "generation_request": {
    "meta_data": {
      "task_type": "photorealistic_product_beauty_macro",
      "priority": "high"
    },
    "output_settings": {
      "aspect_ratio": "3:4",
      "orientation": "portrait",
      "resolution": "ultra_high_res",
      "render_style": "photorealistic_editorial_beauty_macro",
      "sharpness": "high",
      "film_grain": "none_or_very_subtle"
    },
    "creative_prompt": {
      "scene_summary": "Ultra photoreal editorial beauty macro shot. A woman holds a nail polish bottle extremely close to the camera with dramatic perspective. The bottle is the main focus (tack sharp), while the face is softly out of focus behind it. White seamless background. Keep the same composition and hand-to-camera product framing as the reference image.",
      "environment": {
        "setting": "studio",
        "background": "pure white seamless backdrop",
        "lighting": "clean high-key studio lighting, soft shadows, crisp specular highlights on glass and nails"
      },
      "camera": {
        "type": "beauty macro / close-up product shot",
        "lens_look": "wide-close macro perspective (24-35mm equivalent feel), dramatic foreshortening",
        "focus": "product label and bottle edges tack sharp; face slightly soft bokeh",
        "aperture": "f2.0_to_f2.8",
        "do_not_crop": "keep full bottle visible and readable"
      },
      "product_design": {
        "object": "nail_polish_bottle",
        "bottle_material": "clear_glass_with_realistic_refraction",
        "polish_color": "vivid_orange",
        "label_design": {
          "base": "clean_modern",
          "brand_text": "[BRAND NAME] printed clearly on the bottle label",
          "print_rules": "text must be crisp, aligned, not warped, no gibberish letters"
        }
      },
      "quality_rules": [
        "ultra realistic skin texture (no plastic smoothing)",
        "natural eye catchlights",
        "no extra people",
        "no extra objects",
        "no watermark, no UI",
        "product label must be readable and correct",
        "true-to-life glass highlights and reflections",
        "high-end magazine beauty advertising look"
      ]
    },
    "negative_prompt": [
      "text outside the product label",
      "watermark",
      "logo errors",
      "misspelled words",
      "gibberish typography",
      "extra people",
      "extra hands",
      "extra fingers",
      "warped hands",
      "deformed nails",
      "blurred product label",
      "low resolution",
      "plastic skin",
      "over smoothing",
      "face drift",
      "identity change",
      "cartoon",
      "cgi"
    ]
  }
}
```

### Pattern 3: Beverage Hero Shot mit Splash (JSON mit Positive/Negative)
Dieses Pattern erzeugt dramatische Getraenke-Shots mit dynamischen Splash-Effekten. Kompaktes Format mit klaren positiven und negativen Anweisungen.

```json
{
  "prompt": {
    "positive": "Ultra-realistic luxury beverage product photography of a sleek aluminum can, centered in the frame. The can is deep midnight purple, featuring elegant illustrations of grape clusters and green leaves, and is heavily covered in fresh, cold condensation droplets. Prominently labeled '[Product Name]' in premium typography. A dramatic, symmetrical crown-shaped splash of vivid purple juice erupts violently upward and outward from immediately behind the can, catching the light. Studio lighting, high detail, 8k resolution, cinematic, macro lens focus on the can and droplets.",
    "negative": "cartoon, low quality, blurry, flat lighting, amateur, distorted text, ugly splash, asymmetrical, dry can, plastic looking liquid, watermark, signature, out of frame, cropped",
    "style_preset": "photographic",
    "aspect_ratio": "2:3"
  },
  "parameters": {
    "guidance_scale": 7.5,
    "steps": 30,
    "sampler": "DPM++ 2M Karras"
  }
}
```

### Pattern 4: Transparent Material Hyperrealism (JSON-Style-System)
Dieses Pattern erzeugt futuristische transparente Produktvisualisierungen. Besonders stark: Die detaillierte Material- und Beleuchtungsdefinition fuer Glas/Polymer-Effekte.

```json
{
  "subject": "[Your Product]",
  "target_style": {
    "style_name": "ultra-modern transparent black hyperrealism",
    "visual_language": [
      "sleek",
      "futuristic",
      "minimalistic",
      "floating design",
      "high-gloss transparency"
    ],
    "material_appearance": {
      "base_material": "transparent black glass or polymer",
      "texture_quality": "smooth and curved",
      "finish": "high-gloss with partial internal reflections"
    },
    "lighting_style": {
      "source_type": "rim light and directional top light",
      "intensity": "high",
      "shadows": "soft and diffuse glow underneath",
      "highlight_behavior": "sharp specular highlights and reflections across transparent surfaces"
    },
    "color_palette": {
      "dominant_colors": ["#000000", "#0d0d0d", "#1a1a1a"],
      "accent_colors": ["#ffffff", "#333333"],
      "contrast_level": "very high",
      "overall_tone": "dark, glossy, and luminous."
    },
    "rendering_style": {
      "dimensionality": "3D hyperrealistic",
      "resolution_quality": "ultra high",
      "depth_effects": "floating volumetric space with layered reflections"
    }
  },
  "output_settings": {
    "aspect_ratio": "1:1",
    "background_handling": "pure dark void",
    "object_focus": "centered floating form with emphasis on transparency and lighting"
  }
}
```

## Kategoriespezifische Tipps
- Condensation/Kondensation ist DAS Schluessel-Detail fuer Getraenke-Fotografie -- immer detailliert beschreiben
- "Heroic Framing" (leichter Aufwaertswinkel) verstaerkt die Produktwirkung
- Dual-tone Rim Lighting erzeugt professionelle Tiefe und Materialitaet
- Fuer Beauty-Produkte: immer "quality_rules" und "negative_prompt" mitgeben
- Lesbarer Text auf Produkten erfordert explizite Anweisungen: "crisp, aligned, not warped, no gibberish"
- Aspect Ratios: 9:16 fuer Social Media, 3:4 fuer Editorial, 1:1 fuer E-Commerce
- Kamera-Spezifikationen (Lens, Aperture, ISO) erhoehen die Realismus-Qualitaet deutlich

## Empfohlene Negative Prompts
```
cartoon, low quality, blurry, flat lighting, amateur, distorted text, ugly splash, asymmetrical, watermark, signature, out of frame, cropped, plastic skin, over smoothing, deformed hands, extra fingers, gibberish typography, logo errors, misspelled words, cgi look
```
