# Image-to-video

House rule: one action, or one short two-beat action, and one camera move per shot. First-frame lock from a reference still. Wardrobe, helmet, and tools that start in the frame stay as they started. Props stay what they are: a helmet stays a helmet, a radio stays a radio, a mug stays a plain unprinted enamel mug. The hand comes off before the next action. No new wardrobe mid-shot. No manufacturer logos mid-shot. Photoreal, identity locked to the headshot and the first frame.

Prefer about five seconds. Generated 1080p clips are often 1920×1088 at 24 fps; crop 4 pixels from the top and bottom to 1920×1080. Review late frames for softness and for locks (stud, eyebrow scar, tattoo, hair). If a slow push-in softens the face after the action is complete, trim at the last sharp frame rather than immediately regenerating.

The on-camera tell is one beat: She knocks once on her helmet, then her hand comes off. Prefer a first frame with the hand already near the helmet, not planted in a long rest.

## Proof shots

### Shot A — The tell (from `06-cockpit-preflight`)

- **First frame:** `refs/06-cockpit-preflight.png`
- **Action:** She knocks once on her helmet, then her hand comes off. The hand starts near the helmet, not planted. One short tap, then the hand comes off before anything else happens. She does not lift off in this shot. The helmet stays a helmet.
- **Camera:** Almost still, or a very short, sharp push. Do not let a long push soften the face.
- **Duration:** about 5 seconds.
- **Prompt sketch:** First-frame lock. Juniper knocks once on her helmet, then her hand comes off. The hand starts near the helmet. She stays in the seat. Photoreal, identity locked, no beauty sheen, no brand marks.

### Shot B — Ridge scan (from `07-ridge-radio`)

- **First frame:** `refs/07-ridge-radio.png`
- **Action:** If the radio is already at her mouth, do not ask her to lift it. One small mid-task motion: she looks down the ridge in the wind, or speaks a short word into the radio. The radio stays a radio.
- **Camera:** Almost still, or a very slow push.
- **Duration:** about 5 seconds.
- **Prompt sketch:** First-frame lock. The radio is already at her mouth. Juniper looks down the ridge in the wind and speaks a short word into the radio. One motion. The radio stays a plain unbranded radio. Photoreal, identity locked.

### Shot C — Hangar sip (from `08-hangar-mug`)

- **First frame:** `refs/08-hangar-mug.png`
- **Action:** She takes one sip from the plain enamel mug and looks toward the hangar bay. The mug stays a plain unprinted mug, no logos.
- **Camera:** Almost still, or a very slow push.
- **Duration:** about 5 seconds.
- **Prompt sketch:** First-frame lock. Juniper takes one sip and looks toward the open hangar bay. The mug stays a plain unprinted enamel mug. Photoreal, identity locked.
- **Note:** The r2 grit pass rebuilt A and B under a two-video ceiling. C was not rebuilt; do not pair the current 08 still with an older C clip.
