# Lessons from the first characters

These notes come from Marisol Vey, Theo Banks, Juniper Hale, Dr. Iris Okafor, and Kip Morrow, the first characters in this library. They are house practice for every later kit. The formal layout still lives in `docs/kit-format.md`. This file is the process memory: what actually held a face, what broke a still or a shot, and what to do differently from the first generation.

## Start on the grit standard

Do not begin with a beauty portrait and try to dirty it up later. The first headshot should already read as a candid photograph of a real person.

- Mix cameras across the kit: some frames like a handheld 35mm documentary photo, some like a slightly messy phone picture.
- Use practical light that belongs to the character's world. Harsh sodium, a fluorescent tube, a bare bulb, a grill flare, or a phone flash beat soft beauty lighting. Slight under- or over-exposure is welcome where it would happen naturally.
- Keep real skin, but stay moderate: visible pores, peach fuzz, under-eye texture, uneven tone, fine lines, natural asymmetry, stray hairs. Sensor noise or grain helps. Over-rendered, crispy, "3D-scanned" pores look as fake as airbrush.
- Forbid beauty sheen, glossy over-finished eyes or hair, sparkly catchlight polish, mascara or lash-bar polish, airbrush, CGI, and plastic skin. A small, dim, natural highlight in the eye is fine. A white beauty sparkle is not.
- If a first take still looks like a campaign still or a render, regenerate it before it becomes the lock. Small leftover polish (catchlights, lash tips, a pore crunch) is cheaper to tone down with a local edit than with a new face.

## Headshot first, then everything else

Generate the smiling front headshot first. That file is the identity lock. Use it as the reference image for every later still, and check late video frames against it.

If you have to retouch the headshot, keep the identity identical: bone structure, moles, scars, hair, and wardrobe must not drift. Prefer a local edit over a new generation.

## Keep identity locks few and visible

A long identity block can describe bone structure, skin, build, and wardrobe. The *locks* — the details you will actually fight to keep in every still and shot — should be three or four, and they should be visible at a distance and in profile.

Good locks are one-sided and durable: a single ear hoop, a short scar on a jaw or eyebrow, a tiny wrist tattoo, a simple haircut with a fixed length. Supporting description (eye color, nose shape, skin tone, clothes) can be rich, but do not treat every adjective as a lock.

## Avoid marks that land in the wrong profile

Do not put a mole or similar mark on or next to the lips, the philtrum, or any other feature that a profile view will invent on the visible side. Models like to "complete" a face and will stamp the mark onto the wrong lip.

If a mark is one-sided, write the rule into the block: it lives on *her or his* left or right, and in the opposite profile it is on the far side and must be hidden, never flipped. Prefer hiding a mark to placing it wrong. Better still, choose locks that do not sit on the mouth.

## Tattoos: tiny, explicit, one place

"Postage stamp" will be taken literally as a rectangular stamp graphic if you are not careful. Write: a postage-stamp-sized faded [color] [subject] silhouette, clearly readable as that subject, no square stamp border, not mid-forearm.

Place it once, in plain language: outer left or outer right wrist only — the thumb-side, radial side of the wrist, facing out when the arm hangs, not the back of the hand, not mid-forearm. Models still drift a small wrist tattoo onto the back of the hand. Name the outer wrist explicitly, and show that outer wrist clearly in at least one frame (a hanging-arm full-body, or a mug or radio still with the sleeve out of the way) so the placement is checkable.

Keep it small relative to the wrist (about 40–50% of local wrist width, or smaller). Match that size across wide and close shots. A mid-forearm tattoo or a large graphic will fight you in later views and in video, where tattoos also like to morph, double, or melt. If a still comes back too large or on the wrong arm, shrink or move it with a local heal-and-stamp rather than a full regen when you can. If a heal blotches, regenerate the still from the headshot rather than shipping a smear. A fill can be numerically clean (matched mean, collapsed high-pass) and still look like a rounded texture island of smoother grain than the surrounding skin. That is a blotch. Do not ship it. A tattoo that lands cleanly on the back of the hand is a weak spot to note, not an automatic blotchy nudge.

In a true front view, the hand on the left of the frame is the subject's right hand. Say which hand holds the prop, and if the lock is on the left wrist, say there is no tattoo on the right hand or arm.

## Hair: same cut and length from behind

A temple streak or a specific length will fail in the rear view if you do not lock it there. From behind, a "thin left-temple streak" should be mostly hidden, not a wide silver swath down the back. Hair that is "just past the collarbone" should end around the collar and upper back, not mid-back, and should not blow out into a long pennant unless every other view agrees.

Simplest path: give the character a short, even cut with no streak, and state the length for the rear view in the first prompt. If you do use a streak, say which side, how thin it is, and that it is mostly hidden from behind.

## Tells the video model can actually perform

The on-camera tell should be one simple, visible gesture, not a personality trait and not a two-step routine with a lean, a smile, and a prop change stacked on top.

- One action, or one short two-beat action, and one camera move per shot.
- If there is a two-beat (tap then lean, flip then point), the first beat must finish and the hand must come off or clear before the second beat starts. "Grasp and hold" does not read as a tap or a flip.
- If the first frame already has the hand on the object (a helmet, a mug), "knock twice, then the hand comes off" often fails: the model holds the contact and then releases, or it lifts the hand into a point or a wave. Audio may add knock-like transients without a visible lift between beats. Prefer a first frame with the hand near the target, not already planted, or write a one-beat tell. Only regenerate if the required ending never happens.
- First-frame lock from a reference still. Wardrobe, headset, hat, and tools that start in the frame stay as they started.
- Keep props simple and name them. A gooseneck microphone must stay a gooseneck and stay put. A spatula must stay a spatula. Tools like to morph into lamps, mics, or extra hands.
- Check tattoo, jewelry, and hair in late frames, not only at t=0.
- Prefer a 5-second shot. Crop generated 1920×1088 clips by 4 pixels top and bottom to 1920×1080. Keep native ambient unless a score is requested. A single duplicate frame at a concat join is a minor encode artifact, not a reason to redo the cut.

## Prefer local edits for small fixes

For catchlights, lash tips, a wrong-side mole, a tattoo that is too large, or a pore crunch, inpaint or a frequency-separation / adjacent-skin clone is cheaper and safer than a new generation. A regen can fix one thing and drift the face, the boots, or the scene.

When healing skin, do not add the original high-pass back into the hole — that reintroduces the tattoo or mole you just removed. Clone from nearby skin of the same tone and lighting, not from a sleeve, a jacket, or the background. After a heal, stamp a smaller tattoo only once the old mark is actually gone.

Spend a generation on a still only when a local edit cannot hold the anatomy (a rear haircut that is a foot too long, a completely wrong pose, a beauty face that will not wash off).


## Natural teeth from the first generation

Smiling headshots default to an even, ad-white row of teeth. Prompt the first headshot for slightly off-white enamel with real variation, less even than a studio smile, and check it before the file becomes the identity lock. A local recolor on the lock is possible, but a leaky mask will stain the lip or cheek, and you must not change the face. Getting the teeth right on generation one is cheaper.

## Headroom: say "full head with space above the hair"

Tight headroom in a 3:4 full-body still will clip the crown when the contact sheet cover-crops that portrait into a near-square card. Write "full head with space above the hair" into the full-body prompts, and keep real sky or ceiling above the hair in the source, not just in the raw file's last few pixels. If a frame comes back tight, zoom out or outpaint/extend the canvas so both the source and the square card show the hair with space above it. Do not invent headroom by cropping the feet off the source. Pin the feet to the bottom if you extend; fill new sky with sky, not a stretched roofline or a smeared awning. For an interior full-body, fill new ceiling with a soft match to the real top plate, not a dark dummy-truss lid or a row of tiled lights.

## Unprinted props, no brand marks

A CC0 kit must not ship real brand marks: soda-can script and ribbons, aircraft manufacturer nameplates, agency seals, radio logos, or readable trademarks on cups and mugs. Prompt unprinted props from the start (a plain paper cup, a plain enamel mug, an unbranded helmet and radio). Invent fictional names, tail numbers, and unit markings rather than borrowing real ones.

Do not start from a branded prop and try to heal the logo off. Inpaint on lettering and ribbons usually smears or reconstructs the mark. If a brand item lands in a still, regenerate that still from the headshot with an unprinted prop.

## Trim the proof at the last sharp frame

A slow push-in often softens the face in the last second of a five-second shot, and a long held gesture makes that soft ending worse. Before you spend a video generation, inspect late frames (and a sharpness measure if you have one). If the tell is already complete and the face is still sharp, trim at that last sharp frame and shorten the hold. Only regenerate the shot if the action is incomplete at the last sharp moment, and if you do, ask for a shorter, sharper push or an almost-still camera.

Generated 1080p clips are often 1920×1088 at 24 fps; crop 4 pixels from the top and bottom to 1920×1080. Review a five-second shot at 0.00, 0.80, 1.80, 2.50, 4.00, and 4.90. If you trim a shot shorter, pick review times that still cover the action. Keep native ambient unless a score is requested.

## Disk and archives

The box fills up. Archive only the files you actually replace, and *move* them, do not copy them. Drop intermediates in `/tmp` when a pass is done. Do not delete earlier round archives. Generated tool assets can stay in the agent asset store; do not duplicate them into the kit.

## Kit hygiene

- Built-in image and video tools may return a JPEG even when the requested filename ends in `.png`. Convert to PNG and a quality-85 JPG before a file enters `refs/`.
- Write "fictional original character, not a likeness of any real person" into the identity block and the stills prompts.
- Credit line, when needed, is "Created by SMF Works." The library is CC0, credit optional. Do not put the owner's employer name in the tree.
- Do not create or push a GitHub repository until the owner reviews the kit.

## Outdoor and daylight subjects

Outdoor and daylight subjects default to ad polish and campaign grins. Ask for overcast weather, or cold hangar light (sodium or fluorescent mixed with grey daylight), and for fatigue, from generation one. A small real smile at most, and only in one or two frames. Mid-task candid moments, not hero poses or recruiting-ad stances. If a first kit still comes back as a recruiting ad, regenerate the lock and the frames that most read as an ad before they set the tone for the rest of the kit.

A one-beat tell ("she knocks once, then her hand comes off") is more reliable than two knocks when the first frame already has the hand near the target. Start with the hand near, not planted.

If a mid-forearm tattoo resists a clean local move after a tight-mask heal or two, regenerate that still from the headshot and restate a postage-stamp mark on the outer wrist immediately above the hand. Do not ship a blotchy heal.

A 3:4 full-body with natural but modest headroom will clip the crown in a center cover-crop on the near-square contact-sheet card. Keep head and feet in the source; for the card, use a top-biased cover crop so the sheet shows the head (the card may crop the boots). Do not invent a dummy ceiling just to feed a center crop.

## Low-light interiors and rings (from Dr. Iris Okafor)

Low-light interiors with named practical sources (a fluorescent tube, a desk lamp, console LEDs, projector spill) came back gritty on generation one. Starting on the grit standard is easier indoors at night than outdoors in daylight. The exception is a frame with a big pretty sky: a dome full of Milky Way drifts toward a poster. Ask for heavy grain and a faint star field there.

A thumb ring is a hard lock. Even with "right thumb only", the model put the band on the ring or index finger in five of six hand frames. Write the thumb into the pose ("thumb clearly visible along the side of the fader, the band on that right thumb; her fingers have no rings at all"), and check every hand at full size before a still enters `refs/`. A finger ring heals cleanly with a horizontal interpolation across the band (the finger runs across the band, so interpolate along the finger). A small band can be drawn onto a visible thumb with a supersampled stroke and a dim highlight; keep it dull, not bright. If the thumb is hidden, remove the wrong ring and leave the lock unshown rather than forcing it. When the first frame has the band on the thumb, the video model kept it there for the whole shot.

Glasses on a cord: "glasses worn low on her nose, on a cord" produced a second pair hanging on the cord at the same time. Say "one pair only", and when you want them on the cord, say "not on her face".

A tell with a visible result reads better than a tell that is only a small finger motion. "She clicks the pointer off" reads because the beam goes out. Start the first frame with the beam on and the thumb beside the button. The model may lift a finger off the pointer as the beam goes out; ask for the fingers to stay wrapped if it matters.

For a 16:9 card on the contact sheet, set the horizontal focus per image so the face stays in the square crop (a face at a third of the frame needs a left-biased crop, not a centered one).

## Bigger one-sided locks, recurring props, and side views (from Kip Morrow)

Bigger locks held. A black ear plug and a glowing circuit-board wrist band were on the correct (left) side in all nine stills and all three shots on the first try, with no local fixes. Size and contrast beat precision: a lock that is big, dark-on-light or glowing, and on the wrist or ear survives where a thin thumb ring does not. Put all the locks on the same side and pose three-quarter views facing the opposite edge of the frame, so one pose shows every lock.

A mark on clothing is the weakest kind of lock. "A burn on the LEFT cuff" landed on the right cuff in the front full body and mid-forearm on the left sleeve in side views. In a front view, say which side of the photo the mark is on ("on the cuff on the right side of the photo") as well as the wearer's side. In side views, say "on the cuff edge, right above the wrist band, not mid-forearm". A burn on the wrong cuff heals by cloning the same sleeve's fabric from about 60 pixels up (a vertical shift along the sleeve) and moves by transplanting the original burn, mirrored and scaled down, onto the correct cuff with a darkness-based alpha. Inpainting a burn from its border pulls in dark background at the sleeve edge; restrict the mask to the sleeve.

A recurring prop needs its own reference. Pass a still that shows it (here the desk robot) as a second reference image alongside the headshot. Name each part the tell needs in plain words: "one round eye LED like a small dark marble, not a screen or camera" and "one small silver bat-handle toggle sticks up from the top". The first bench frame grew a rectangular camera window instead of an eye and had no toggle; once those words and the reference were in, the tell frame came back with both.

A tell with a lighting result reads at once. Start with the light off and the finger hovering beside the switch. The eye was lit by about 1.8 seconds and stayed lit. Over a long hold the model widened "a tiny smirk" into a soft closed-mouth smile, so trim after the result lands rather than regenerating.

Two in-world frames at the same bench (the bench still and the tell frame) look alike on the sheet. If the tell needs its own first frame, make the other bench still a different camera distance or angle.

Night phone flash outdoors (flash-flattened face, hard shadow on a shutter, black street beyond) read as the most "real photo" frame in the kit, and it stayed real in video. Walls of complete skateboards and counter glass still grew printed graphics; check background boards and anything under glass at full size.
