# Resources Design – S01 World Asset Kit (Prompts)

Purpose: Generate a cohesive asset library for Season 1 that feels rich and distinct while keeping species differences subtle. S01 shows only interiors and mid‑city vistas inside the Golden City; the floating nature is hidden until the season finale.

## Global Generation Settings

- Style: realistic‑anime, vibrant yet cinematic, soft volumetric light, shallow depth of field, clean linework,
- Resolution: 3840×2160 masters (deliver 1080p/9:16 crops)
- Models: SDXL (stills), ControlNet Depth + OpenPose as needed; img2video for motion
- Negative (global): lowres, blurry, overexposed, text, watermark, logo, extra fingers/limbs, fused limbs, grotesque anatomy, plastic 3D toy look, oversaturated, lens dirt
- Color grade intent: filmic contrast, warm highlights, slightly teal shadows
- Naming: `assets/s01/{category}/{location|species}/{variant}_{time}.png`

### Global Variables (use in prompts)

- GLOBAL_MODEL: SDXL
- GLOBAL_SAMPLER: DPM++ 2M
- GLOBAL_RES_4K: 3840x2160
- GLOBAL_STEPS_DEFAULT: 34
- GLOBAL_CFG_DEFAULT: 6.5
- GLOBAL_STYLE: realistic anime, vibrant yet cinematic, soft volumetric light, shallow depth of field, clean linework, filmic contrast, warm highlights, slightly teal shadows,
- GLOBAL_NEGATIVE: lowres, blurry, overexposed, text, watermark, logo, extra fingers, extra limbs, fused limbs, mangled hands, grotesque anatomy, plastic 3D toy look, oversaturated, lens dirt

- GLOBAL_STYLE_BOOST: award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary,
- GLOBAL_COLOR_SCRIPT: warm gold highlights vs cool teal shadows; saturated accent colors keyed to ot: amber (Ayala), indigo (Inbar), teal (Matar)
- GLOBAL_HQ_UPSCALE: hires_fix=1.7, denoise=0.28 (optional)
- GLOBAL_DETAILING: optional ControlNet Tile for micro‑detail (weight 0.5–0.7)
- GLOBAL_MOON_SYSTEM: A faint, colossal sci-fi man-made moon-like skeleton-structure in orbit, partially obscured by clouds. Alongside it, a natural celestial moon with a rust-red glow, warmer in tone. Both cast layered, distinct shadows at night, with faint translucence in the day sky.

## S01 Visual Reveal Policy (Mandatory)

- Do not show the city’s physical edge, underside, or skies that imply floating.
- Frame mid‑city vistas with occlusion (towers, arcades, rising streets).
- Use haze, architectural foregrounds, and tight horizons to avoid reveals.
- Signage must be abstract/no readable text.

## Species Subtlety Guide (S01)

- Enosh: luminous eyes (color shifts), iridescent skin, refined attire.
- Sylvari: faint leaf‑fiber hair textures; subtle bark‑grain on temples; earth‑tone attire with natural weaves.
- Aquarii: soft bioluminescent freckles; faint gill lines at neck; fabrics with liquid sheen; cool palette.
- Ferox: slightly longer canines; athletic posture; warmer undertones; leather/mesh accents; minimal overt animal traits.
- Mechani: fine sub‑dermal circuit filigree; small interface ports; matte technical fabrics.
- Umbra: shadow‑blending garments, high contrast lighting on features; reflective eyes in low light.

Seeds: fix per species for background extras; main heroes use episode‑specific seeds. Example: Enosh=1201, Sylvari=1202, Aquarii=1203, Ferox=1204, Mechani=1205, Umbra=1206.

---

## The Golden City – S01‑Safe Plates

All prompts include: realistic anime, high detail, no readable text, no horizon or edges implying floating.

Note: The descriptive briefs above are for planning. Use the self‑contained prompts in "Per‑Asset Generation Details" below directly, or insert the variables (GLOBAL\_\*) into your tool if supported.

1. Civic Core Plaza (Day)

- Prompt: elegant civic plaza with tiered stone, shallow reflecting pool, slender light pylons, planted trees in geometric planters, mid‑rise towers enclosing the view; warm daylight, people silhouettes; clean surveillance nodes subtly visible
- Negative: (global)

2. Civic Core Plaza (Night)

- Prompt: same plaza at night, soft amber path lights, cool blue uplights on architecture, reflections on wet stone, sparse crowd silhouettes

3. Market Arcade (Day)

- Prompt: covered market arcade with fabric awnings, vendor stalls, crates, overhead beams, skylight slats casting stripes of light; mixed‑species pedestrians; mid‑distance occlusion

4. Residential Terraces (Afternoon)

- Prompt: stacked terraces with small balconies, potted plants, laundry lines, narrow passages; warm afternoon light; neighbors at windows (silhouettes)

5. Transport Hub Concourse (Interior)

- Prompt: wide interior concourse with turnstiles, platforms suggested by edge lighting, clean signage without text, surveillance domes; clinical lighting; controlled crowd

6. Industrial Belt – Service Road (Dusk)

- Prompt: service road between warehouses, utility conduits, maintenance doors, safety beacons, dusk haze; limited sky wedge; forklifts parked

7. Abandoned Factory – Loading Dock (Night)

- Prompt: sealed loading doors, broken windows, puddled concrete with moon reflections, crate stacks, minimal security fixtures

8. Administrative Lobby (Enosh) (Day)

- Prompt: refined lobby with polished stone, abstract reliefs, elegant guard post, translucent partitions, controlled warmth, mid‑shot composition

---

## Mini‑Habitats (Urbanized Species Districts)

1. Sylvari Atrium Courtyard (Day/Night)

- Prompt: indoor‑outdoor courtyard ringed by living walls, hanging planters, timber/stone textures, softly dappled light; communal seating; subtle leaf motifs; Sylvari citizens present

2. Aquarii Canal Walk (Day/Night)

- Prompt: narrow canal with glass‑lined water channels, low bridges, moisture on stone, teal lighting cues; Aquarii citizens with subtle gill lines and luminescent freckles

3. Ferox Market Alley (Afternoon/Night)

- Prompt: muscular architecture, leather/mesh awnings, grit on pavement, robust fixtures; Ferox citizens with athletic posture and warm undertones

4. Mechani Service Tunnel & Workshop (Low‑light)

- Prompt: maintenance tunnel with cable trays, access panels, tool benches; cool LEDs; Mechani with sub‑dermal circuit filigree

5. Umbra Shadow Arcade (Night)

- Prompt: vaulted arcade with deep shadows, patterned light leaks, reflective eyes in darkness, information kiosks with dim UI glow; Umbra citizens blending into shade

---

## Street‑Level Props & Set Dressing

1. Surveillance Camera Node

- Prompt: sleek minimal camera pod with blue status LED, mounted on slender pole or soffit; futuristic but discreet

2. Micro‑Drone (Patrol)

- Prompt: palm‑sized quad with smooth shell, faint blue light band, near‑silent design; neutral background

3. Wayfinding Pylon (No Text)

- Prompt: monolithic signage totem with abstract icons, edge lighting, matte metal + glass

4. Vendor Crates & Stalls

- Prompt: stack of wooden/composite crates, fabric awnings, wire baskets, produce/goods without readable labels

5. Light Poles & Benches Set

- Prompt: cohesive urban furniture kit: slender light poles, benches with wood/metal hybrid, planter variations

6. Access Terminals (Hand‑held and Wall)

- Prompt: small screen devices with abstract UI, no legible glyphs; cool blue accents

---

## Background Citizens (Extras)

Guidelines: mid‑distance, subtle species markers, neutral fashion variations; avoid hero‑level detail. Generate trios for variety.

- Enosh Civilians (3 variants)

  - Prompt: stylish humanoid civilians with luminous eyes, refined attire, subtle iridescent skin; walking/standing groups; realistic anime

- Sylvari Civilians (3 variants)

  - Prompt: civilians with faint leaf‑fiber hair textures, soft bark‑grain at temples, earth‑tone garments with natural weaves

- Aquarii Civilians (3 variants)

  - Prompt: civilians with faint neck gill lines and soft bioluminescent freckles, cool palette garments with liquid sheen

- Ferox Civilians (3 variants)

  - Prompt: civilians with slightly longer canines, athletic posture, warmer undertones; leather/mesh accents; restrained animal hints

- Mechani Civilians (3 variants)

  - Prompt: civilians with fine sub‑dermal circuit filigree, matte technical fabrics, small interface ports near wrist/neck

- Umbra Civilians (3 variants)
  - Prompt: civilians in shadow‑blending garments, reflective eyes in low light; high contrast lighting

---

## Enforcers & Security

- Enforcer (Sheol’s forces) – Patrol Pair

  - Prompt: imposing armored uniforms with sharp silhouettes, muted insignia (no readable text), tactical gear, cold lighting; realistic anime

- Security Checkpoint (Compact)
  - Prompt: waist‑high barrier, scanner arch, camera pods, abstract UI screens, clean industrial design

---

## UI/HUD & Motifs (Non‑linguistic)

- Waveform Monitor Panel

  - Prompt: dark panel with audio waveform line, small red REC dot, subtle cool grid

- Ot Motif Textures (Neutral)
  - Prompt: abstract, non‑readable glyph motifs inspired by ancient scripts; embossed/engraved textures; no legible letters

---

## Lighting Variants

For each location, produce: Day, Golden Hour/Dusk, Night. Maintain consistent key direction and practical sources for continuity.

---

## ControlNet & Consistency Notes

- Depth maps from base plates ensure layout coherence across time of day.
- OpenPose for simple crowd/figure arrangements; keep poses readable and calm.
- Fix seeds per location and per species background set to stabilize look.
- Keep signage non‑linguistic; avoid vistas that betray the floating city until S01 finale.

---

## Per‑Asset Generation Details (Self‑contained)

Use these directly in the generator. Each includes model/settings, seed, negatives, and references (if any).

### Golden City – Plates

1. Civic Core Plaza (Day)

- Prompt: realistic anime, elegant civic plaza with tiered calcite stone pavers and brass inlay tracery (non‑linguistic), shallow reflecting pool with geometric ripple pattern, slender light pylons casting halo glow, planted trees in geometric planters, mid‑rise towers enclosing the view; warm daylight; subtle surveillance nodes; atmospheric haze; no readable text; no horizon or edges implying floating; award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary, A faint, colossal sci-fi man-made moon-like skeleton-structure in orbit, partially obscured by clouds. Alongside it, a natural celestial moon with a rust-red glow, warmer in tone. Both cast layered, distinct shadows at night, with faint translucence in the day sky.
- Negative: lowres, blurry, text, watermark, logo, oversaturated, lens dirt
- Settings: model=SDXL, size=3840x2160, sampler=DPM++ 2M, steps=36, cfg=6.5, seed=610101, ${GLOBAL_HQ_UPSCALE}
- ControlNet: none
- References: none

2. Civic Core Plaza (Night)

- Prompt: realistic anime, same plaza at night with soft amber path lights, cool blue uplights washing ribbed facades, reflections on wet calcite stone, sparse crowd silhouettes, prismatic glass accents catching dual moonlight; atmospheric mist; no readable text; occluded horizons; award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary, A faint, colossal sci-fi man-made moon-like skeleton-structure in orbit, partially obscured by clouds. Alongside it, a natural celestial moon with a rust-red glow, warmer in tone. Both cast layered, distinct shadows at night, with faint translucence in the day sky.
- Negative: (same as above)
- Settings: model=SDXL, 3840x2160, DPM++ 2M, steps=34, cfg=6.5, seed=610102
- ControlNet: Depth (optional from Day plate), weight=0.6
- References: assets/s01/city/civic_core_plaza_day.png (optional depth)

3. Market Arcade (Day)

- Prompt: realistic anime, covered market arcade with woven fabric awnings (species motifs: leaf lattices, water‑wave jacquards, leather mesh), vendor stalls and stacked crates, overhead timber/metal beams, skylight slats casting dramatic stripes of light; pedestrians showing subtle species traits (luminous eyes, leaf-fiber hair, gill lines, longer canines, circuit filigree, shadow-blending garments); hanging lanterns; mid‑distance occlusion; no readable signage; warm gold highlights; award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary, A faint, colossal sci-fi man-made moon-like skeleton-structure in orbit, partially obscured by clouds. Alongside it, a natural celestial moon with a rust-red glow, warmer in tone. Both cast layered, distinct shadows at night, with faint translucence in the day sky.
- Negative: (global)
- Settings: SDXL, 3840x2160, DPM++ 2M, steps=36, cfg=6.5, seed=610103, ${GLOBAL_HQ_UPSCALE}
- ControlNet: none
- References: none

4. Residential Terraces (Afternoon)

- Prompt: realistic anime, stacked terraces with cantilevered planters of exotic flora, small balconies with iridescent glazing, linen lines, narrow stepped passages; carved relief bands (non‑linguistic); warm afternoon light with volumetric beams; neighbors at windows (silhouettes); occluded horizon; warm gold highlights; award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary, A faint, colossal sci-fi man-made moon-like skeleton-structure in orbit, partially obscured by clouds. Alongside it, a natural celestial moon with a rust-red glow, warmer in tone. Both cast layered, distinct shadows at night, with faint translucence in the day sky.
- Negative: (global)
- Settings: SDXL, 3840x2160, DPM++ 2M, steps=34, cfg=6.0, seed=610104
- ControlNet: none
- References: none

5. Transport Hub Concourse (Interior)

- Prompt: realistic anime, wide interior concourse with sculpted turnstiles, platforms suggested by edge lighting and floor light channels, abstract icon signage (no text), surveillance domes integrated into ribs, glass‑resin balustrades with subtle water‑like reflections; clinical lighting; controlled crowd; warm gold highlights; award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary,
- Negative: (global)
- Settings: SDXL, 3840x2160, DPM++ 2M, steps=36, cfg=6.5, seed=610105, ${GLOBAL_HQ_UPSCALE}
- ControlNet: none
- References: none

6. Industrial Belt – Service Road (Dusk)

- Prompt: realistic anime, service road between basalt‑clad warehouses, exposed utility conduits with glowing seam indicators, maintenance doors with abstract relief, safety beacons in amber, dusk haze; limited sky wedge; forklifts parked; sparks of micro‑drones in distance; no city edge; A faint, colossal sci-fi man-made moon-like skeleton-structure in orbit, partially obscured by clouds. Alongside it, a natural celestial moon with a rust-red glow, warmer in tone. Both cast layered, distinct shadows at night, with faint translucence in the day sky.
- Negative: (global)
- Settings: SDXL, 3840x2160, DPM++ 2M, steps=36, cfg=6.5, seed=610106, ${GLOBAL_HQ_UPSCALE}
- ControlNet: none
- References: none

7. Abandoned Factory – Loading Dock (Night)

- Prompt: outdoor view of a loading dock in an abandoned factory, realistic anime, sealed loading doors with worn relief panels, broken clerestory windows, puddled concrete with shimmering dual moon reflections, crate stacks with rope lashings, minimal security fixtures; shafts of dual moonlight and fog; heavy shadows; award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary, A faint, colossal sci-fi man-made moon-like skeleton-structure in orbit, partially obscured by clouds. Alongside it, a natural celestial moon with a rust-red glow, warmer in tone. Both cast layered, distinct shadows at night, with faint translucence in the day sky.
- Negative: (global)
- Settings: SDXL, 3840x2160, DPM++ 2M, steps=36, cfg=6.5, seed=610107, ${GLOBAL_HQ_UPSCALE}
- ControlNet: none
- References: none

8. Administrative Lobby (Enosh) (Day)

- Prompt: refined lobby with polished stone and mother‑of‑pearl inlays, abstract relief wall (non‑linguistic), elegant guard post, translucent resin partitions, realistic anime, award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary, controlled warm sunlight with godrays, mid‑shot composition; Enosh aesthetic; no readable text;
- Negative: (global)
- Settings: SDXL, 3840x2160, DPM++ 2M, steps=36, cfg=6.0, seed=610108, ${GLOBAL_HQ_UPSCALE}
- ControlNet: none
- References: none

### Mini‑Habitats – Districts

1. Sylvari Atrium Courtyard (Day)

- Prompt: realistic anime, indoor‑outdoor courtyard ringed by living walls and phyllotaxis trellises, hanging planters with bioluminescent seedpods, timber/stone textures, softly dappled light through leaf canopies; communal seating carved from living wood; subtle leaf motifs; Sylvari citizens (leaf‑fiber hair, bark‑grain temples); no readable text; award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary, A faint, colossal sci-fi man-made moon-like skeleton-structure in orbit, partially obscured by clouds. Alongside it, a natural celestial moon with a rust-red glow, warmer in tone. Both cast layered, distinct shadows at night, with faint translucence in the day sky.
- Negative: (global)
- Settings: SDXL, 3840x2160, steps=36, cfg=6.5, seed=620201, ${GLOBAL_HQ_UPSCALE}
- ControlNet: none
- References: none

2. Sylvari Atrium Courtyard (Night)

- Prompt: realistic anime, same atrium at night with warm lanterns in leaf lanterns, dual moon shafts, reflective water bowls, gentle spore‑glow along trellises; mist; award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary, A faint, colossal sci-fi man-made moon-like skeleton-structure in orbit, partially obscured by clouds. Alongside it, a natural celestial moon with a rust-red glow, warmer in tone. Both cast layered, distinct shadows at night, with faint translucence in the day sky.
- Negative: (global)
- Settings: SDXL, 3840x2160, steps=36, cfg=6.5, seed=620202
- ControlNet: Depth from Day variant (optional), weight=0.6
- References: assets/s01/habitats/sylvari_atrium_day.png (optional depth)

3. Aquarii Canal Walk (Day)

- Prompt: realistic anime, narrow canal with glass‑lined water channels and prismatic caustic reflections, low bridges, moisture on carved stone, teal lighting cues; translucent resin railings; Aquarii citizens (faint gill lines, soft bioluminescent freckles); no textual signage; award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary, A faint, colossal sci-fi man-made moon-like skeleton-structure in orbit, partially obscured by clouds. Alongside it, a natural celestial moon with a rust-red glow, warmer in tone. Both cast layered, distinct shadows at night, with faint translucence in the day sky.
- Negative: (global)
- Settings: SDXL, 3840x2160, steps=36, cfg=6.5, seed=620203, ${GLOBAL_HQ_UPSCALE}
- ControlNet: none
- References: none

4. Aquarii Canal Walk (Night)

- Prompt: realistic anime, canal at night with teal bioluminescent accents tracing the waterline, shimmering reflections, low mist, rippling light patterns across stone; dual moonlight reflecting in water; quiet foot traffic; award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary, A faint, colossal sci-fi man-made moon-like skeleton-structure in orbit, partially obscured by clouds. Alongside it, a natural celestial moon with a rust-red glow, warmer in tone. Both cast layered, distinct shadows at night, with faint translucence in the day sky.
- Negative: (global)
- Settings: SDXL, 3840x2160, steps=36, cfg=6.5, seed=620204
- ControlNet: Depth from Day variant (optional), weight=0.6
- References: assets/s01/habitats/aquarii_canal_day.png (optional depth)

5. Ferox Market Alley (Afternoon)

- Prompt: realistic anime, muscular architecture with tensioned leather sails and braided cords, bone‑inlaid rail details (non‑linguistic), grit on pavement, robust fixtures; Ferox citizens (athletic posture, warmer undertones, subtle canines); dramatic sun shafts; no readable text; award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary, A faint, colossal sci-fi man-made moon-like skeleton-structure in orbit, partially obscured by clouds. Alongside it, a natural celestial moon with a rust-red glow, warmer in tone. Both cast layered, distinct shadows at night, with faint translucence in the day sky.
- Negative: (global)
- Settings: SDXL, 3840x2160, steps=36, cfg=6.0, seed=620205, ${GLOBAL_HQ_UPSCALE}
- ControlNet: none
- References: none

6. Ferox Market Alley (Night)

- Prompt: realistic anime, same alley at night with hard contrast practicals, warm pools of light and deep shadow; hanging braziers; texture‑rich walls; dual moonlight creating layered shadows; award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary, A faint, colossal sci-fi man-made moon-like skeleton-structure in orbit, partially obscured by clouds. Alongside it, a natural celestial moon with a rust-red glow, warmer in tone. Both cast layered, distinct shadows at night, with faint translucence in the day sky.
- Negative: (global)
- Settings: SDXL, 3840x2160, steps=34, cfg=6.0, seed=620206
- ControlNet: Depth from Afternoon (optional), weight=0.6
- References: assets/s01/habitats/ferox_alley_day.png (optional depth)

7. Mechani Service Tunnel & Workshop (Low‑light)

- Prompt: realistic anime, award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary, maintenance tunnel with cable trays and fiber‑optic veins, access panels with glowing seam lines, tool benches with articulated arms; cool blue‑white LEDs; Mechani citizens (fine sub‑dermal circuit filigree); abstract UI, no readable glyphs;
- Negative: (global)
- Settings: SDXL, 3840x2160, steps=36, cfg=6.5, seed=620207, ${GLOBAL_HQ_UPSCALE}
- ControlNet: none
- References: none

8. Umbra Shadow Arcade (Night)

- Prompt: realistic anime, vaulted arcade with deep shadows and moiré patterned light leaks, obsidian tile floors, reflective eyes in darkness, information kiosks with dim UI glow; Umbra citizens blending into shade; theatrical rim lights; subtle dual moonlight filtering through; no readable text; award‑winning cinematic concept art, striking composition, dramatic lighting, atmospheric perspective, intricate and cohesive material detailing, elegant futuristic architecture with unique cultural motifs, believable but extraordinary, A faint, colossal sci-fi man-made moon-like skeleton-structure in orbit, partially obscured by clouds. Alongside it, a natural celestial moon with a rust-red glow, warmer in tone. Both cast layered, distinct shadows at night, with faint translucence in the day sky.
- Negative: (global)
- Settings: SDXL, 3840x2160, steps=36, cfg=6.5, seed=620208, ${GLOBAL_HQ_UPSCALE}
- ControlNet: none
- References: none

### Street‑Level Props (Kits)

1. Surveillance Camera Node

- Prompt: realistic anime product plate, sleek minimal camera pod with blue status LED, mounted on slender pole or soffit; futuristic but discreet; neutral backdrop
- Negative: (global)
- Settings: SDXL, 2048x2048, steps=30, cfg=6.0, seed=630301
- ControlNet: none
- References: none

2. Micro‑Drone (Patrol)

- Prompt: realistic anime product plate, palm‑sized quad with smooth shell, faint blue light band, near‑silent design; neutral background
- Negative: (global)
- Settings: SDXL, 2048x2048, steps=30, cfg=6.0, seed=630302
- ControlNet: none
- References: none

3. Wayfinding Pylon (No Text)

- Prompt: realistic anime product plate, monolithic signage totem with abstract icons, edge lighting, matte metal + glass; no readable text
- Negative: (global)
- Settings: SDXL, 2048x3072, steps=32, cfg=6.0, seed=630303
- ControlNet: none
- References: none

4. Vendor Crates & Stalls

- Prompt: realistic anime, stack of wooden/composite crates, fabric awnings, wire baskets, produce/goods without readable labels; neutral alley backdrop
- Negative: (global)
- Settings: SDXL, 3072x2048, steps=32, cfg=6.0, seed=630304
- ControlNet: none
- References: none

5. Light Poles & Benches Set

- Prompt: realistic anime product set, slender light poles, benches with wood/metal hybrid, planter variations; consistent design language; neutral plaza backdrop
- Negative: (global)
- Settings: SDXL, 3072x2048, steps=32, cfg=6.0, seed=630305
- ControlNet: none
- References: none

6. Access Terminals (Hand‑held and Wall)

- Prompt: realistic anime product plates, small screen devices with abstract UI, no legible glyphs; cool blue accents; wall‑mount and hand‑held
- Negative: (global)
- Settings: SDXL, 2048x2048, steps=30, cfg=6.0, seed=630306
- ControlNet: none
- References: none

### Background Citizens (Extras)

Enosh Civilians (3 variants)

- Prompt: realistic anime, stylish humanoid civilians with luminous eyes, refined attire, subtle iridescent skin; walking/standing groups; mid‑distance framing
- Negative: (global)
- Settings: SDXL, 3072x1728, steps=30, cfg=6.0, seed=640401..640403 (use three seeds)
- ControlNet: none
- References: none

Sylvari Civilians (3 variants)

- Prompt: realistic anime, civilians with faint leaf‑fiber hair textures, soft bark‑grain at temples, earth‑tone garments with natural weaves; mid‑distance
- Negative: (global)
- Settings: SDXL, 3072x1728, steps=30, cfg=6.0, seed=640404..640406
- ControlNet: none
- References: none

Aquarii Civilians (3 variants)

- Prompt: realistic anime, civilians with faint neck gill lines and soft bioluminescent freckles, cool palette garments with liquid sheen; mid‑distance
- Negative: (global)
- Settings: SDXL, 3072x1728, steps=30, cfg=6.0, seed=640407..640409
- ControlNet: none
- References: none
