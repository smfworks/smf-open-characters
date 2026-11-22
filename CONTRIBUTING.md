# Contributing

This library is maintained by SMF Works. New characters are original inventions, not portraits, lookalikes, or thinly veiled versions of real people or existing copyrighted characters.

## Proposing a character

A character is ready for the catalog when the folder matches [`docs/kit-format.md`](docs/kit-format.md) and the practice in [`LESSONS.md`](LESSONS.md). At minimum that means:

- A unique `id` in kebab-case and a full name that does not collide with anyone already in `characters.json`
- Pronunciation, age range, a one-line hook, genres, and a signature color hex
- A short story in a warm human voice (about 150 words) and one on-camera tell
- A verbatim identity block covering face, hair, eyes, build, signature wardrobe, and distinguishing details
- Nine reference stills (the views listed in the kit format), saved as PNG plus lightweight JPG, plus a contact sheet
- Stills prompts, image-to-video guidance, and Grok Imagine notes
- A Suno voice prompt and four song directions
- One short proof video cut from stills (three shots, one action and one camera move each)

Add a row to the table in `README.md` and an entry to `characters.json` when the kit is complete, with `status` set to `review` until the owner locks it.

## Originality and consent

- Invent the look. Do not prompt from a celebrity, influencer, coworker, or any other real person, and do not use a real person's photograph as a face reference.
- Do not reuse trademarked mascots or characters from other libraries without a clear license that allows it.
- Keep the SMF Works hosts and other brand characters out of this open catalog. This library is for purpose-built open characters only.

## License on contributions

By adding a character or asset to this library, you dedicate that contribution to the public domain under CC0 1.0, the same license as the rest of the catalog. Credit remains optional.

## Review

Kits are reviewed for identity consistency across the nine stills, clarity of the tell, prompt quality, and whether the proof video holds the face. Nothing is published from this tree until SMF Works approves the release.
