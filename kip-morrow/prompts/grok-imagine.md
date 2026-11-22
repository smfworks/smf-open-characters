# Grok Imagine notes

Use the built-in image and video tools ($0). The front headshot is the identity lock. Generate it first in the gritty standard (harsh greenish shop fluorescent mixed with a warm side lamp, tired, the faintest closed-mouth smirk), then pass `refs/01-headshot-front.png` as the reference image for every later still. For any frame with the desk robot, pass a robot still (`refs/09-toggle-tell.png`) as a second reference so the chassis, wiring, eye, and toggle stay the same.

## Still generation

- Aspect ratios: 3:4 for views 01–05, 16:9 for views 06–09.
- Keep the identity block in the prompt even when a reference image is set.
- Night interiors with named practical sources (fluorescent tube, clamp-on lamp, LED glow) and a direct phone flash outdoors came back gritty on generation one. The night-flash frame is the most convincing "real photo" in the kit.
- Three-quarter views facing the RIGHT edge of the frame put the left ear plug and the left-wrist LED band toward the camera every time. The plug and the band never flipped sides in any still or shot.
- The burn mark is the weak lock. In the front full body it landed on the RIGHT cuff (healed and moved with a local edit). In side views it lands mid-forearm on the left sleeve instead of the cuff edge. Write "on the LEFT cuff edge, right above the wrist band, not mid-forearm".
- A robot "eye LED" drifted into a small rectangular camera window on the first bench frame; it was painted into a round lens with a local edit. Write "single round eye LED, like a small dark marble, not a screen or camera". The toggle only appeared when the prompt said "one small silver bat-handle toggle sticks up from the top of the chassis".
- Blank decks held well, but wall racks of complete boards still grew a printed bottom graphic and a stray white mark under the counter glass. Check every background deck and the counter glass at full size; inpaint them out.
- Profiles came back as near-profiles (about three-quarter) with the same face; the ear locks still read.
- The tool may return a JPEG even if the filename ends in `.png`. Convert to a PNG and a quality-85 JPG before the file enters `refs/`. Reference images must live under `/workspace` (or the tool's asset folders) to be accepted.

## Image-to-video

- Image-to-video from a reference still as the first frame, 1080p, 5 seconds.
- The tell reads because the eye lights: start with the eye OFF and the finger hovering beside the toggle. In the proof the eye is lit by about 1.8 s and stays lit; the face stays sharp through the end.
- Clips arrive at 1920×1088, 24 fps. Crop 4 pixels from the top and bottom to 1920×1080. Concat with libx264, crf 18, native ambient, no score.
- The model widens a "tiny smirk" into a soft closed-mouth smile over a long hold. Trim after the action instead of regenerating.

## What held

Night grit on generation one; headshot lock first; three bigger one-sided locks on the same side (plug, LED band, burn) instead of a small ring; a one-beat tell with a visible result (the eye lighting); a second reference image for the recurring prop.
