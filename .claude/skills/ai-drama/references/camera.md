# Camera grammar for AI drama

Pick each shot's size and angle for what the viewer must feel, then write those exact English terms into the image prompt (models know them better than Thai).

## Shot sizes

| Term | Frames | Use it for |
| --- | --- | --- |
| Extreme Wide Shot (EWS) | the whole place, people tiny | opening a new location, loneliness, scale |
| Wide Shot (WS) / Full Shot (FS) | whole body with surroundings | entrances, blocking, who is where |
| Medium Full Shot (MFS) | knees up | walking, two people standing and talking |
| Medium Shot (MS) | waist up | ordinary dialogue, gestures |
| Medium Close-Up (MCU) | chest up | dialogue that matters, reactions |
| Close-Up (CU) | face | emotion, a decision, a lie |
| Extreme Close-Up (ECU) | eyes, lips, a hand | the moment of shock, a detail that matters |
| Insert / Macro | an object | a letter, a ring, a phone screen, a clue |

## Angles

| Term | Effect |
| --- | --- |
| Eye level | neutral, honest |
| Low angle | the character is powerful, threatening |
| High angle | the character is small, weak, watched |
| Over-the-Shoulder (OTS) | two people talking; we stand behind the listener |
| Point of View (POV) | we see what the character sees |
| Dutch angle | unease, something is wrong |
| Two-shot | both characters in frame: relationship, tension |

## Moves (video prompt; one per shot)

`static shot` (default, cheapest to get right) · `slow push-in` (tension, realisation) · `slow pull-out` (reveal, isolation) · `pan left/right` (follow a look or a walk) · `tracking shot` (walk-and-talk) · `handheld` (panic, chase).

## Scene recipes

- **Dialogue between two people:** MS two-shot to establish → OTS on A → OTS on B → CU on whoever has the key line.
- **Reveal:** CU of the reacting face first → Insert of what they see → WS to show the consequence.
- **Hook (shot 1):** start on the most emotional frame of the episode (CU or ECU), not on an establishing wide.
- **Cliffhanger (last shot):** CU on a face that just learned something, slow push-in, cut before the answer.

Vary sizes inside a scene: wide → medium → close is the safe rhythm; two shots of the same size in a row look like a jump cut.

## The 8-angle sheet (one prompt, eight frames)

To explore a moment before choosing, ask Nano Banana for one image laid out as a 2×4 grid of the same moment from eight angles: `wide shot, medium shot, close-up, extreme close-up, low angle, high angle, over-the-shoulder, side profile` — with the identity block and the location block, same lighting in every panel. Pick the panel you like and regenerate it alone at full size as that shot's image.
