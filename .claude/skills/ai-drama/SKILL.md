---
name: ai-drama
description: Plan a Thai AI drama (ละคร AI / ซีรีส์สั้นแนวตั้ง) episode end to end for Gemini (Nano Banana images), Google Flow (Veo video) and CapCut — story brief, hooked script, character and location reference sheets, a shot list with camera grammar, and copy-ready Thai image and video prompts that keep faces and voices the same in every shot. Use when the person wants to make an AI drama, AI series, AI short film or "ละคร AI", asks for a script, shot list, storyboard or Flow/Veo/Nano Banana prompts for one, or wants to cut wasted generations.
---

# AI Drama (ละคร AI)

The whole job is **planning before generating**. Every generation costs credits; most waste comes from changing a face, a camera or a line after the clip is made. So build the episode as files first, check them, and only then hand the prompts to Gemini and Flow, one shot at a time.

You cannot run Gemini, Flow or CapCut from here. You write everything they need, in Thai, ready to paste, and the person generates. When they bring clips back, help them fix only the shot that is wrong (see "Fixing a shot").

## Defaults

Unless the person says otherwise: vertical 9:16, one episode ≈ 2 minutes = **12 shots × ~10 s**, Thai dialogue, realistic live-action look (DSLR), no music/text/subtitles baked into the video (added in CapCut). Ask only what only they can answer: the story idea, the genre, how many episodes, and whether characters need to look like real people they have rights to. Never use a real person's face without their consent.

## The work loop

Make one folder per series: `drama/<series-slug>/`, one subfolder per episode `ep01/`. Write each file, show it, and move on when the person is happy. Files:

| Step | File | What it holds |
| --- | --- | --- |
| 1 | `brief.md` | Logline (1 sentence), genre, tone, audience, episode count, length, aspect, look |
| 2 | `bible.md` | Characters and locations — the **identity blocks** (below), reused verbatim in every prompt |
| 3 | `refs.md` | Reference-sheet image prompts for every character and location; generate these **first** |
| 4 | `ep01/script.md` | Scenes with Thai dialogue; hook in shot 1, cliffhanger in the last shot (`references/script.md`) |
| 5 | `ep01/shots.md` | The shot list: one row per ~10 s shot (`references/camera.md`) |
| 6 | `ep01/prompts.md` | Per shot: an image prompt (Nano Banana) and a video prompt (Flow/Veo) (`references/prompts.md`) |
| 7 | `ep01/edit.md` | CapCut order, subtitle lines, music cue, title/end card, cover frame |
| 8 | `ep01/check.md` | The pre-generation checklist below, ticked |

### Identity blocks (the core trick)

Each character gets one fixed paragraph: age, ethnicity, face shape, eyes, eyebrows, nose, lips, skin tone, hair (length, colour, parting), body build, one distinguishing mark, default outfit, and a **voice line** (gender, age, pitch, pace, manner, e.g. `เสียงผู้หญิงอายุ 22 โทนสดใส พูดเร็วเล็กน้อย ติดหยอกล้อ`). Paste the same block, word for word, into every prompt that shows that character; change only outfit or emotion, and say so explicitly ("same face, now wearing …"). Locations get the same treatment (time of day, light direction, key props, colour palette).

In Flow, attach that character's reference sheet as an ingredient for every shot they appear in.

### Pre-generation checklist (`check.md`)

- Every shot names its characters by their identity block and attaches their reference images.
- One action and at most one camera move per shot; no shot needs two things to happen in sequence.
- Each spoken line fits its shot: Thai speech runs about 4–5 syllables per second, so an 8–10 s shot holds about one short sentence (≈ 25–35 syllables). Split longer lines across shots.
- Shot sizes vary scene to scene (no three medium shots in a row); dialogue scenes use shot / reverse-shot or OTS.
- The voice line is identical for each character in every shot.
- Every video prompt ends with the no-music / no-text / no-subtitle / no-cut clause.
- Shot 1 hooks within 2 seconds; the last shot ends on an unanswered question.
- Credits estimate: shots × the person's per-clip cost (ask them; do not guess prices).

## Fixing a shot

When a generated clip is wrong, find which layer caused it and fix only that layer, for that shot:

| What is wrong | Fix |
| --- | --- |
| Face or outfit drifted | Re-attach the reference sheet; paste the identity block again; regenerate the **image** first, then the video from it |
| Wrong framing or angle | Change the shot size / angle words in the image prompt (`references/camera.md`) |
| Movement is odd or too much | Simplify the motion line to one verb; prefer "static shot" or "slow push-in" |
| Voice changed | Paste the exact voice line; keep the dialogue in quotes in Thai |
| Lip-sync off, line cut | Shorten the line or split it into two shots |
| Unwanted text, music, cuts | Make sure the no-music/no-text clause is present and last |

Never regenerate the whole episode for one bad shot.

## Assembling and subtitles

Edit in CapCut in shot order (`edit.md`). If the person wants Thai subtitles, a title card or a branded end card added to the finished cut, use `/hyperframes` (this repo's `makin-subs/` project is a working subtitle pipeline).

## What not to do

- Do not recommend buying "shared" or resold AI credits; point the person to the official plans of the tool they use.
- Do not promise a cost per episode; estimate only from numbers the person gives.
- Do not copy another creator's script, characters or course material; write original work.
