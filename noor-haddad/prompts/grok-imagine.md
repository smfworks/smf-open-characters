# Grok Imagine notes

Built-in image and video generation was used to build this kit. These notes are what helped hold the face, the mole side, the cobalt, and clean backgrounds.

- Generate the 3:4 front headshot first. Use that file as `reference_image_paths` for every later still, and keep the identity block in the prompt. The locked identity still is `refs/01-headshot-front.png`. Do not regenerate or locally edit the locked headshot. A slight balm smoothness on the locked headshot lips is a residual weak spot.
- Ask for a candid real photograph, mixed 35mm documentary and phone-camera looks, hard fluorescent tubes and monitor glow, sensor noise, moderate pores, natural unpainted matte lips, and no beauty sheen. Say "no sparkly catchlights, no lash polish, no lip gloss" in portrait prompts. "Cinematic" and "beauty lighting" work against the standard.
- Portrait views 01–05 are 3:4. In-world views 06–09, which may become video first frames, are 16:9. In-world stills in this kit are 1280×720.
- The tool may return a JPEG even when the requested filename ends in `.png`. Convert to PNG and a quality-85 JPG before a file enters `refs/`.
- The shirt must stay true to newsroom cobalt #1F4EAD — a deep saturated cobalt, not a bright mid-blue and not navy.
- For the mole, always name both sides: on the upper right cheekbone (photo-left in a front view). Hide it in a left profile (02) and in left-facing views such as 07; never flip it to the left cheek. If a generation peeks or duplicates a mole on the left cheek, hide it with a tight local inpaint rather than shipping a flip. If the mole cannot be placed correctly, hide it.
- Backgrounds: demand blank or abstract charts, no readable typography, no faces on boards, no logos, and no stray silhouettes or reflections. An empty newsroom — if a desk shot comes back with other people, redo it. A window shot must not pick up a back-of-head silhouette or a figure in the glass.
- True 90° profiles may come back as near-profiles. That is an honest limit, not a reason to leave a flipped mole in place.
- Prefer a local inpaint or a tight heal for small mistakes (flipped or duplicate mole, typography, a logo on a bezel) instead of a full regen, so the headshot lock does not drift. Do not ship a blotchy heal.
- A capped red pen as a first frame for the tell was hard to get; several attempts returned an already-uncapped pen with the cap posted, tip on the page. This kit keeps `06-newsroom-desk` (capped pen on the desk) and `09-red-pen` (already circling an abstract color block) and splits the tell across those two proof shots rather than spending further still redos.
- Image-to-video: 1080p from a first-frame still, about 5 seconds, one action or one short two-beat, one camera move. Crop 1920×1088 results by 4 pixels top and bottom to 1920×1080. Do not add last-frame, keyframe, or extra reference images if you need 1080p. Concat with libx264, crf 18, native ambient, no score.
- For the tell, do not invent readable numbers on the page. Circle an abstract color block. Mouth stays closed. Count arms, hands, and fingers at full size on every proof frame. No other people may appear mid-shot.
