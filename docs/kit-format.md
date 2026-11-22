# Kit format

Every character lives in one folder named after its `id`. The front page of the library is assembled from `characters.json` and the thumbnail path in each entry.

Process notes from Marisol Vey and Theo Banks — photography grit, few visible locks, natural teeth and real headroom from the first generation, unprinted props, tells a video model can actually perform, trim a proof at the last sharp frame, local edits before regens — live in [`LESSONS.md`](../LESSONS.md). Follow those when you start a new character.

## Folder layout

```
<id>/
  README.md
  character.json
  character-block.md
  contact-sheet.png
  refs/
    01-headshot-front.png
    01-headshot-front.jpg
    02-profile-left.png
    02-profile-left.jpg
    03-profile-right.png
    03-profile-right.jpg
    04-fullbody-front.png
    04-fullbody-front.jpg
    05-fullbody-rear.png
    05-fullbody-rear.jpg
    06-<in-world-scene-a>.png
    06-<in-world-scene-a>.jpg
    07-<in-world-scene-b>.png
    07-<in-world-scene-b>.jpg
    08-<in-world-scene-c>.png
    08-<in-world-scene-c>.jpg
    09-<action-or-outfit-variant>.png
    09-<action-or-outfit-variant>.jpg
  prompts/
    stills.md
    image-to-video.md
    grok-imagine.md
  voice/
    suno.md
  story/
    story.md
  proof/
    <id>-proof.mp4
```

File names for views 06 through 09 may be descriptive, but they must stay numbered so a contact sheet and a front-end gallery can sort them.

## Front-page index (`characters.json`)

Each character contributes one object to the library index:

| Field | Notes |
| --- | --- |
| `id` | Folder name, kebab-case, stable |
| `name` | Display name |
| `pronunciation` | Pronunciation respelling, uppercase stressed syllables |
| `age` | Range or decade, not a celebrity age |
| `hook` | One sentence |
| `genres` | Array of short labels |
| `signature_color` | Hex, including the leading `#` |
| `thumbnail` | Path from the library root, usually the headshot JPG |
| `folder` | Path from the library root, trailing slash optional |
| `status` | `review` while the kit is being checked; `locked` once the owner approves the character |
| `locked_date` | ISO date (`YYYY-MM-DD`), only when `status` is `locked` |

The character folder also has its own `character.json` with the same fields plus story, tell, wardrobe, and asset paths for tooling.

## Identity block

`character-block.md` is pasted verbatim into image and video prompts. It must be specific enough to lock a face: bone structure, skin, hair (cut, color, and any streak or pin), eye color and shape, build and height, signature wardrobe, and two or three distinguishing details that survive a profile or a wide shot (a scar, a mole, a tattoo, a necklace, a headset).

Write the block as a single character description, not as a biography. Do not mention real people.


## Photography standard

Every reference still in this library should read as a real person's photograph, not a cinematic still, not a beauty campaign, and not a render.

- Mix cameras across a kit: some frames like a handheld 35mm documentary photo, some like a slightly messy phone picture.
- Use practical and mixed light that belongs to the character's world. Harsh sodium lamps, a fluorescent tube, a bare bulb, or a phone flash are better than soft beauty lighting. Slight under- or over-exposure is welcome where it would happen naturally.
- Keep real skin: pores, peach fuzz, under-eye texture, uneven tone, fine lines, natural asymmetry, stray hairs. Add sensor noise or grain and, where it helps, mild chromatic aberration and imperfect focus.
- Forbid beauty sheen, glossy over-finished eyes or hair, perfect catchlights, airbrush, CGI, and plastic skin.
- Generate the headshot first as the identity lock, then use it as the reference image for every later still. If a frame still looks like a polished render, regenerate it before it enters the contact sheet.
- The on-camera tell should be a single, small, visible gesture a performer or a video model can actually do. Prefer one beat over a two-step routine.

## Reference stills

Generate the headshot first. Use that approved headshot as the reference image for every later still so identity stays locked. Portrait views (01–05) are 3:4. In-world and action views that may become video first frames (06–09) are 16:9.

1. Smiling headshot, front
2. Left profile
3. Right profile
4. Standing front, full body
5. Standing rear, full body
6. In-world scene A (the character's primary workplace or habitat)
7. In-world scene B (a second location that shows range)
8. Close listening or close reacting shot
9. Action or outfit variant

Save a lossless PNG and a lightweight JPG (quality around 85, reasonably sized for the web) for each view. Build `contact-sheet.png` from the nine PNGs, labeled, in a 3×3 grid.

If a frame drifts off model, or still looks like a cinematic beauty portrait, regenerate it against the headshot before moving on.

## Prompts and video

- `prompts/stills.md` holds a ready-to-paste prompt for each of the nine views, each starting with the identity block or a clear instruction to prepend it.
- `prompts/image-to-video.md` states the house rule: one action and one camera move per shot, first-frame lock from a reference still, no new wardrobe mid-shot.
- `prompts/grok-imagine.md` records tool notes: reference-image use, aspect ratios, and any model-specific wording that helped hold the face.
- Proof video is three shots, about four to six seconds each, image-to-video from the stills, cut together in 16:9 unless the character kit clearly calls for 9:16. Music is optional.

## Voice

`voice/suno.md` includes one reusable voice prompt and four song directions that fit the character's world and genre. Keep the voice invented. Do not describe it as sounding like a named singer.

## Story

The README holds the canonical story and the on-camera tell. `story/story.md` may repeat them for tooling. The tell should be a visible gesture or habit a performer or a video model can actually do on camera, not only a personality trait.
