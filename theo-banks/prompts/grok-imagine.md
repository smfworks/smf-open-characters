# Grok Imagine notes

Built-in image and video generation was used to build this kit. These notes are what helped hold the face and the grit.

- Generate the 3:4 front headshot first. Use that file as `reference_image_paths` for every later still, and keep the identity block in the prompt.
- Ask for a candid real photograph, mixed 35mm documentary and phone-camera looks, practical light, sensor noise, moderate pores, and no beauty sheen. Say "no sparkly catchlights, no lash polish" in portrait prompts. "Cinematic" and "beauty lighting" work against the standard.
- Portrait views 01–05 are 3:4. In-world views 06–09, which may become video first frames, are 16:9.
- The tool may return a JPEG even when the requested filename ends in `.png`. Convert to PNG and a quality-85 JPG before a file enters `refs/`.
- For profiles, spell out the hide rule: left-ear hoop and left-cheek scar are hidden in a right profile, never flipped to the visible side.
- For the tattoo, say: postage-stamp-sized faded black chili-pepper silhouette, clearly a chili with a stem, no square stamp border, outer left wrist only, not mid-forearm. "Postage stamp" alone can come back as a literal stamp graphic.
- For the rear view, state hair length in that view: a tight fade, a little fullness on top, ending well above the collar, no streak, no tail.
- Image-to-video: 1080p from a first-frame still, about 5 seconds, one action or one short two-beat, one camera move. Crop 1920×1088 results by 4 pixels top and bottom to 1920×1080. Do not add last-frame, keyframe, or extra reference images if you need 1080p.
- For the tell, demand that the flip finish before the point, and that the spatula stay a spatula. Do not add a third beat.
- Prefer a local inpaint or frequency-separation heal for small mistakes (wrong-side hoop, oversized tattoo, catchlight polish) instead of a full regen, so the headshot lock does not drift.
