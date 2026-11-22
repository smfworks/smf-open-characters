# Grok Imagine notes

Use the built-in image and video tools ($0). The front headshot is the identity lock. Generate it first in the gritty standard (overcast or cold hangar light, tired and wind-burned, a small real smile at most), then pass `refs/01-headshot-front.png` as the reference image for every later still.

## Still generation

- Aspect ratios: 3:4 for views 01–05, 16:9 for views 06–09.
- Keep the identity block in the prompt even when a reference image is set.
- Outdoor and daylight subjects default to ad polish. Ask for overcast weather, or cold hangar light (sodium or fluorescent mixed with grey daylight), and for fatigue, from generation one. A small real smile at most, in one or two frames. Mid-task candid moments, not hero poses.
- Ask for slightly off-white teeth with natural variation if a smile is used, and for "full head with space above the hair" on portraits and full-body frames.
- Name the mountain tattoo as postage-stamp-sized, clearly mountains, no square stamp border, on the outer left wrist only (thumb-side, immediately above the hand, not the back of the hand, not mid-forearm).
- Hide-don't-flip the left-ear stud and the left-eyebrow scar in the right profile.
- For the rear view, state that the short crop ends at the nape, well above the collar, with no ponytail.
- Forbid beauty sheen, sparkly catchlights, lash polish, CGI, and plastic skin. Ask for candid 35mm or phone-camera grit from the first frame.
- Unprinted props only: plain enamel mug, plain radio, unbranded graphite helmet. Fictional tail marking JX-07. No manufacturer or agency logos.
- The tool may return a JPEG even if the filename ends in `.png`. Convert to a PNG and a quality-85 JPG before the file enters `refs/`. Reference images must live under `/workspace` (or the tool's asset folders) to be accepted.

## Image-to-video

- Image-to-video from a reference still as the first frame. Use 1080p only when you do not pass a last frame, keyframes, or extra reference images.
- One action, or one short two-beat, and one camera move. For the tell, she knocks once on her helmet, then her hand comes off. Prefer a first frame with the hand already near the helmet, not planted.
- Clips often arrive at 1920×1088, 24 fps. Crop 4 pixels from the top and bottom to 1920×1080. Concat with libx264, crf 18, native ambient, no score.
- If a late push-in softens the face, trim at the last sharp frame before regenerating.

## What held

Grit, overcast light, and fatigue on generation one; headshot lock first; four one-sided visible locks with hide-don't-flip; short even hair with an explicit rear length; unprinted props from the start; the tell written as one knock with the hand starting near the helmet and coming off afterward.
