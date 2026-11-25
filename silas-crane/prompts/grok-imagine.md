# Grok Imagine notes

Built-in image and video generation was used to build this kit. These notes are what helped hold the face, the scars, and the grit.

- Generate the 3:4 front headshot first. Use that file as `reference_image_paths` for every later still, and keep the identity block in the prompt. The locked identity still is `refs/01-headshot-front.png`. Do not regenerate or locally edit the locked headshot.
- Ask for a candid real photograph, mixed 35mm documentary and phone-camera looks, harsh uneven practical forge light, soot, sweat, a messy shop, sensor noise, moderate pores, and no catalog or beauty sheen. "Cinematic" and "beauty lighting" work against the standard.
- Portrait views 01–05 are 3:4. In-world views 06–09, which may become video first frames, are 16:9. In-world stills in this kit are 1280×720.
- The tool may return a JPEG even when the requested filename ends in `.png`. Convert to PNG and a quality-85 JPG before a file enters `refs/`.
- Hair must stay sparse like the locked headshot, with the scalp visible, not a full thick white cap. Several later stills in this kit still read a little fuller than the headshot; treat that as a known weak spot and keep prompting sparse.
- For the nick-scar, always name both sides: on the right cheek just above the beard line (photo-left in a front view). Hide it in a left profile (02); never flip it to the left cheek. If a generation omits it, a small local pale nick can be painted; do not ship a fresh orange scratch or a blotchy heal.
- For the burn, always name both sides: faded pale thumbprint on the outer right forearm just below the rolled sleeve (photo-left in a front view, photo-right in a rear view). Never on the left arm. If a generation flips it, prefer a clean local arm-swap (remove the wrong-side mark, add a faded thumbprint on the right) over another redo. Do not ship a blotchy heal.
- The full-body front still in this kit shows blue jeans rather than dark-brown canvas. That is a wardrobe weak spot; the identity lock stays brown canvas. The burn on that still is also a smaller linear mark rather than a clear thumbprint.
- True 90° profiles may come back as near-profiles. That is an honest limit, not a reason to leave a flipped scar in place.
- Props stay unprinted: no readable typography or logos on drawers, tools, or walls. A small typography heal with TELEA is fine if it stays clean.
- Prefer a local inpaint or a tight heal for small mistakes (missing nick, flipped burn, typography) instead of a full regen, so the headshot lock does not drift. Do not ship a blotchy heal.
- The anvil-horn still needed several tries before the hammer sat over the pointed horn rather than the anvil face. Prompt the horn and the empty face explicitly. Stop after a few redos and heal locks locally if the composition is finally right.
- Image-to-video: 1080p from a first-frame still, about 5 seconds, one action or one short two-beat, one camera move. Crop 1920×1088 results by 4 pixels top and bottom to 1920×1080. Do not add last-frame, keyframe, or extra reference images if you need 1080p. Concat with libx264, crf 18, native ambient, no score.
- For the tell, demand two light taps on the anvil horn, not the anvil face, and that the mouth stay closed. Do not add speech or a third beat. Count arms, hands, and fingers at full size on every proof frame.
