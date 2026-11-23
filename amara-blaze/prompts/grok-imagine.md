# Grok Imagine notes

Built-in image and video generation was used to build this kit. These notes are what helped hold the face, the tattoo side, and the grit.

- Generate the 3:4 front headshot first. Use that file as `reference_image_paths` for every later still, and keep the identity block in the prompt. The locked identity still is `refs/01-headshot-front.png`.
- Ask for a candid real photograph, mixed 35mm documentary and phone-camera looks, practical light, sensor noise, moderate pores, and no beauty sheen. Say "no sparkly catchlights, no lash polish" in portrait prompts. "Cinematic" and "beauty lighting" work against the standard. Do not copy a beauty-studio finish.
- Portrait views 01–05 are 3:4. In-world views 06–09, which may become video first frames, are 16:9.
- The tool may return a JPEG even when the requested filename ends in `.png`. Convert to PNG and a quality-85 JPG before a file enters `refs/`.
- Hair is jaw-length, fire-red / bright orange-copper, and wavy — not shoulder-length. Eyes are vivid natural green, not grey-green or hazel.
- For the tattoo, always name both sides: on her left side of the neck (photo-right in a front view). Hide it in a right profile (03) and a rear view (05); never flip it to the right side of the neck (photo-left in a front view). If a generation peeks a triangle on the wrong side, hide it with a tight local inpaint rather than shipping a flip. If the tattoo cannot be placed correctly, hide it. The tattoo-free fallback is a green butterfly hair clip on the left side of her hair; do not invent or move a wrong-side tattoo.
- Locked views 02 and 03 came back as three-quarter views rather than true 90° profiles. That is an honest limit of the locked set, not a reason to leave a wrong-side tattoo in place.
- Outfit varies; the grey sweater is incidental, not a wardrobe lock. Small gold hoops when the ears are visible.
- Props stay unprinted: no readable text or logos on diner signs, pie cards, album covers, posters, pumps, or a record label.
- Prefer a local inpaint or a tight heal for small mistakes (wrong-side tattoo peek, typography, a catchlight polish) instead of a full regen, so the headshot lock does not drift.
- Image-to-video: 1080p from a first-frame still, about 5 seconds, one action or one short two-beat, one camera move. Crop 1920×1088 results by 4 pixels top and bottom to 1920×1080. Do not add last-frame, keyframe, or extra reference images if you need 1080p. Concat with libx264, crf 18, native ambient, no score.
- For the tell, demand that the needle land, that she wait a beat, and that both hands stay visible after she leaves the tonearm. A vanished right hand is a fail. Do not add a third beat.
