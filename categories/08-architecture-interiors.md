# Architecture & Interiors - Prompt-Patterns

> Staerken: Interior-Design-Transformationen, Travel-Itinerary-Illustrationen, architektonische Grid-Vergleiche, dystopische Architektur-Konzepte und Droste-Effekt-Kunstwerke. Mischung aus kurzen direktiven Prompts und komplexen Template-Systemen.

## Empfohlenes Format
Hybrid (kurze direktive Prompts fuer Raumtransformationen, strukturierte Templates fuer Travel-Illustrationen und Architektur-Grids)

## Best Practice Patterns

### Pattern 1: Travel-Journal Illustration (Template-System)
Vollstaendiges Prompt-System fuer kindlich-verspielte Reise-Illustrationen im Buntstift-Stil. Nutzt Platzhalter fuer Stadt, Tagesanzahl und Sprache. Generiert automatisch Routen mit Sehenswuerdigkeiten, lokalen Speisen und dekorativen Elementen.

```
Please create a vibrant, child-like crayon-style vertical (9:16) illustration titled "{City Name} Travel Journal."
The artwork should look as if it were drawn by a curious child using colorful crayons, featuring a soft, warm light-toned background (such as pale yellow), combined with bright reds, blues, greens, and other cheerful colors to create a cozy, playful travel atmosphere.

I. Main Scene: Travel-Journal Style Route Map

In the center of the illustration, draw a winding, zigzagging travel route with arrows and dotted lines connecting multiple locations.
The route should automatically generate recommended attractions based on {Number of Days}:

Example structure (auto-filled with {City Name}-related content):
- "Stop 1: {Attraction 1 + short fun description}"
- "Stop 2: {Attraction 2 + short fun description}"
- "Stop 3: {Attraction 3 + short fun description}"
- "Final Stop: {Local signature food or souvenir + warm closing remark}"

Rules:
- If no number of days is provided, default to a 1-day highlight itinerary.

II. Surrounding Playful Elements (Auto-adapt to the City)

Add many cute doodles and child-like decorative elements around the route:
1. Adorable travel characters (a child holding a local snack, a little adventurer with a backpack)
2. Q-style hand-drawn iconic landmarks
3. Funny signboards ("Don't get lost!", "Crowds ahead!", "Yummy food this way!")
4. Sticker-style short phrases ("{City Name} travel memories unlocked!")
5. Cute icons of local foods
6. Childlike exclamations ("I didn't know {City Name} was so fun!")

III. Overall Art Style Requirements
- Crayon / children's hand-drawn travel diary style
- Bright, warm, colorful palette
- Cozy but full and lively composition
- Emphasize the joy of exploring
- All text should be in a cute handwritten font
- Make the entire page feel like a young child's fun travel-journal entry

---
Input: {City Name} {Number of Days}-Day Trip, {Language}
```

### Pattern 2: Architektonischer Grid-Vergleich (16 Styles, ein Raum)
Kompakter Prompt fuer die Erzeugung eines 4x4-Grids, das denselben Raum in 16 verschiedenen Interior-Design-Stilen zeigt. Nutzt Depth-Map-Referenz fuer konsistente Raumgeometrie.

```
Professional architectural photography 4x4 grid showcasing identical room layout transformed through 16 distinct interior design styles. All furniture placement, room geometry, and spatial composition must exactly match the provided depth map reference. Camera: consistent 3/4 angle, 24mm tilt-shift lens, f/8, tripod-mounted. Only materials, colors, textures, and decorative elements change - never position or scale of objects.

CRITICAL CONSTRAINT: Furniture placement, room dimensions, window/door positions, and all object locations must remain pixel-perfect identical to the reference depth map across all 16 frames. The silhouette and spatial arrangement cannot change.
```

### Pattern 3: Dystopische Mega-Architektur (Objekt-zu-Gebaeude-Transformation)
Mehrstufiger Prompt fuer die Transformation eines Alltagsgegenstands in ein dystopisches Firmenhauptquartier. Erzeugt ein 2x2-Grid mit Blueprints, Strassenansicht und Innenraum.

```
Step 1: Take a mundane office object as starting point.

Step 2: Scale this object up by 5000%. It is now the headquarters for a villainous mega-corporation in a Brutalist concrete future. Analyze the geometry to create habitable floors.

Step 3 Output: 2x2 Grid.
Grid 1 & 2: Blueprints of the "Object turned into Tower" showing elevator shafts and executive suites.
Grid 3: Eye-level street view looking up at the concrete mega-structure in rain and fog. Tiny people for scale. Neon cyberpunk signs attached to the exterior.
Grid 4: Interior shot of the lobby, retaining the plastic curves of the original object but rendered in cold concrete and glass.
```

### Pattern 4: Einfache Raumtransformation
Minimalistischer Prompt-Ansatz: Ein leerer Raum wird durch eine einfache Anweisung moebliert. Demonstriert, dass Nano Banana Pro auch mit kurzen, direktiven Prompts starke Ergebnisse liefert.

```
Show me how this room would look with furniture in it
```

Ergaenzend fuer spezifischere Ergebnisse:
```
A shorthand prompt for recursive images: "Droste effect without photography or people"
```

## Kategoriespezifische Tipps
- Fuer Interior-Design: Mit einem Foto eines leeren Raums starten, dann per Prompt moeblieren lassen
- Grid-Vergleiche benoetigen eine Depth-Map-Referenz fuer konsistente Raumgeometrie
- Travel-Illustrationen funktionieren am besten im 9:16 Hochformat
- Dystopische Architektur profitiert von Kontrasten: "cold concrete and glass" vs. "plastic curves"
- Der Droste-Effekt ("Bild im Bild") eignet sich besonders fuer Kunst-Studio- und Galerie-Szenen
- Einfache Prompts reichen oft aus - Nano Banana Pro versteht Kontext aus Referenzbildern

## Empfohlene Negative Prompts
```
blurry, low detail, washed out, cartoon (bei Foto-Stil), anime, game UI, infographic style, text, captions, watermarks, logos, interface elements, distorted perspective, warped buildings, oversaturated neon color, plastic look
```
