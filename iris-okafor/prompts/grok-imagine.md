# Grok Imagine notes

Use the built-in image and video tools ($0). The front headshot is the identity lock. Generate it first in the gritty standard (dim back-office fluorescent mixed with dome spill, tired, a faint closed-lip smile at most), then pass `refs/01-headshot-front.png` as the reference image for every later still.

## Still generation

- Aspect ratios: 3:4 for views 01–05, 16:9 for views 06–09.
- Keep the identity block in the prompt even when a reference image is set.
- Low-light interiors (dome, console, back office) gave real grit on generation one. Name the practical sources: fluorescent tube, desk lamp, console LEDs, projector spill. Dark dome frames with a bright Milky Way drift toward a pretty poster; ask for heavy grain and a faint star field.
- The thumb ring is the hardest lock. In five of six hand frames the model put the band on the ring or index finger even with "RIGHT thumb only". What worked: "thumb clearly visible along the side of the fader, a thin plain silver band on that RIGHT THUMB only; her fingers have no rings at all". A finger ring heals cleanly with a horizontal interpolation across the band; drawing a new band on a thumb works at small sizes with a supersampled stroke.
- Say "one pair of glasses only, not on her face" when you want them on the cord. A "glasses worn at the console" prompt produced a second pair hanging on the cord at the same time.
- For profiles, say which edge of the frame she faces and which temple is visible. Facing the right edge shows the grey right temple; facing the left edge shows the dark left temple.
- Ask for "full head with space above the hair" in portraits and full-body frames.
- Unprinted props only: plain black pointer with a single button, plain off-white mug, unlabeled console, unbranded projector. Check walls for pinned notices; blank any pseudo-text with a local fill.
- The tool may return a JPEG even if the filename ends in `.png`. Convert to a PNG and a quality-85 JPG before the file enters `refs/`. Reference images must live under `/workspace` (or the tool's asset folders) to be accepted.

## Image-to-video

- Image-to-video from a reference still as the first frame, 1080p, 5 seconds.
- The tell reads best as a beam going out: start with the green beam on and the thumb beside the button. In the proof the beam goes out at about 2.6 s and she is looking up by about 3.4 s. The model also lifted her index finger off the pointer as the beam went out; ask for "fingers stay wrapped around the pointer" if that matters.
- A clip with the band on the thumb in the first frame kept it there for all five seconds.
- Clips arrive at 1920×1088, 24 fps. Crop 4 pixels from the top and bottom to 1920×1080. Concat with libx264, crf 18, native ambient, no score.

## What held

Low-light grit on generation one; headshot lock first; three one-sided visible locks with hide-don't-flip on the grey temple; short even coils with an explicit rear length; unprinted props; a one-beat tell with a visible result (the beam going out).
