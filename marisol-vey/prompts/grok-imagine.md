# Grok Imagine notes

These notes are for producing the kit with Grok Imagine (built-in image and video generation). They are practical, not a requirement for people using the kit in other tools.

## Grit and realism

Ask for candid real photography, not a cinematic portrait and not a beauty headshot. Mix 35mm documentary frames with a few phone-camera frames. Name harsh practical light (sodium, fluorescent, bare tungsten, or a phone flash). Allow slight under- or over-exposure, sensor noise, mild chromatic aberration, and imperfect focus. Call out under-eye texture, uneven skin, stray hairs, and asymmetry. Forbid beauty sheen, glossy over-finished eyes or hair, perfect catchlights, airbrush, and CGI.

## Stills

- Invent the face from the identity block on the first generation. Do not attach a photograph of a real person as a reference.
- Generate the smiling front headshot first (`01-headshot-front`, 3:4). Review it for the lock points below and for whether it could pass as a candid photograph of a real person, including under close inspection.
- Use that approved headshot as `reference_image_paths` for every later still.
- For true profiles, say "true profile, no three-quarter cheat." On the left profile, the mole must sit on the far side of the philtrum or be hidden; never place it on the visible lip. On the right profile, the visible side has no silver.
- Portrait refs (01–05) use aspect ratio 3:4. Scene refs that may become video first frames (06–09) use 16:9.
- The mermaid tattoo must stay postage-stamp sized and on the outer right wrist, not mid-forearm.
- If a still is off-model or still looks like a rendered beauty portrait, regenerate it against the headshot. Do not accept a drifted or overly polished frame into the contact sheet.
- Avoid readable text and brand logos on walls or equipment.

## Image-to-video

- Use image-to-video with the still as `image_path` so it becomes the first frame.
- Keep the prompt short after the lock. The current tell is a single token tap against the collarbone; do not add a console double-tap or a hair tuck.
- After each clip, compare late frames to the headshot. Also check that props hold: the gooseneck mic must stay a gooseneck and stay put, and a headset that starts on must stay on.
- Proof cut is 16:9. Music is optional.

## Identity lock points (checklist)

- Small round mole on the upper lip just to the right of the philtrum (her right); hide it in left profile rather than place it wrong
- Natural silver streak at the left temple only
- Thin pale vertical scar, outer third of the left eyebrow
- Moss-green eyes, amber ring, not over-sharpened, no perfect catchlights
- Dark chestnut waves just past the collarbone, deep left part, stray hairs
- Olive waxed field jacket over navy cable-knit, or sweater-only in view 09
- Thin gold ferry-token necklace
- Brass headset: around the neck, or one cup on and one cup hanging off in the radio room
- Postage-stamp-sized mermaid tattoo, outer right wrist only
- Scuffed chestnut mid-calf lace-up deck boots in full-body views
