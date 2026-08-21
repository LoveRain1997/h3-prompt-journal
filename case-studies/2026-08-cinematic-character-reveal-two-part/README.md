# Case Study 007 — Two-Part Cinematic Character Reveal with Continuous BGM

## Inputs

- `<Picture 1>` — Same character's complete pose library, body, costume, hairstyle, accessories, church environment, all photographed poses
- `<Picture 2>` — The ONLY facial identity reference for the same character
- Plus supplementary pose references in the same scene
- Reference BGM track (instrumental) and reference motion sample
- Target duration: **30 seconds total** (Part 1 0–15s + Part 2 15–30s), 16:9, 24fps
- Format: realistic photographic cinematography with high-end motion-graphics editing
- Setting: a believable, restrained British-Puritan-style church — same location throughout

## Media files

| File | Role |
|---|---|
| [`picture-1-pose-library.png`](./picture-1-pose-library.png) | Picture 1 — complete pose library, costume, church environment |
| [`picture-2-face-identity.png`](./picture-2-face-identity.png) | Picture 2 — facial identity lock for the same character |
| [`picture-1-additional-poses.png`](./picture-1-additional-poses.png) | Supplementary poses (same character, same church) |
| [`picture-1-supplementary-poses.png`](./picture-1-supplementary-poses.png) | More reference poses for Part 2 selection |
| [`reference-motion-sample.mp4`](./reference-motion-sample.mp4) | Reference motion / pacing sample |
| [`reference-bgm-tokyo-drifter.wav`](./reference-bgm-tokyo-drifter.wav) | Reference instrumental BGM (no vocals) |

## The problem

A character reveal is not one video. It's two.

Any character trailer longer than ~20 seconds faces a structural break: the first half must *introduce*, the second half must *establish*. These are different jobs. Trying to do both with one continuous prompt produces a flat, unmodulated video — a 30-second opening that never pays off.

But splitting into two separate prompts creates a different disaster: at the seam, the music restarts, the church changes, the lighting shifts, the character "rediscovers" themselves, and the audience feels two unrelated clips glued together instead of one trailer.

The constraint is harder than it sounds because the model's prior is to **reset** between generations. Anything you can name — character, pose, costume, church, palette, BGM key, reverb tail, room ambience — will subtly restart unless you explicitly tell it to keep going.

## The breakthrough

Split the prompt, but write the seam as a contract.

The two parts are issued as two independent prompts. To make them read as one trailer, the contract has six clauses, written into **both** prompts in matching language:

| Contract clause | Part 1 commitment | Part 2 commitment |
|---|---|---|
| Same character / costume / church | "The character remains a realistic photographic subject" | "Use exactly the same character, identity, costume, church established in Part 1" |
| Final-frame continuity | "Final frame should feel like a deliberate pause before the next 15-second section" | "Begin exactly from the final visual state of Part 1" |
| BGM continuity | "Do not create a musical ending at 15 seconds" + "keep harmonic and rhythmic momentum alive" | "Do NOT restart the music" + "exact harmonic and rhythmic state continues" |
| Sound design continuity | "Do not end the sound design at 15 seconds" | "Do not create a new ambience when Part 2 begins" |
| Non-repetition of shots | (implicit — first half) | "Do not repeat Part 1's exact shot mechanisms" + an explicit avoidance list |
| Pose library discipline | "Treat these poses as the ONLY approved major poses" | "Use the remaining approved poses from Picture 1 that were not emphasized in Part 1" |

The non-repetition list in Part 2 is worth highlighting. It doesn't just say "don't repeat." It names the six shot mechanisms Part 1 used — eye-only opening, face reveal, simple architectural reveal, simple hand-to-face match, same negative-space composition, same foreground wipe, same initial pose presentation — and tells the model to avoid them. Without this list, Part 2's first cut will reflexively copy Part 1's first cut, because the model's prior is "this is the structure of a character reveal."

The technique stack:

| Technique | Role |
|---|---|
| **Two-Prompt / One-Video Architecture** | Independent prompts bound by an explicit seam contract |
| **Mirror Contract Clauses** | Each continuity rule appears in BOTH prompts, phrased from that half's point of view |
| **Pose-Library Discipline** | Picture 1 poses are the *only* approved poses; never invent |
| **Face-Lock Separation** | Picture 2 = face only, Picture 1 = everything else (no merge, no redesign) |
| **Beat-Indexed Shot Tables** | 13 cuts per half with explicit time ranges and visual actions |
| **Non-Repetition Avoidance List** | Part 2 names Part 1's exact shot mechanisms to avoid |
| **Continuous-Sound Design** | Room reverb, cloth movement, whoosh vocabulary carry across seam |
| **Sister-Half Pacing** | Part 1 = establishment tempo; Part 2 = escalation → peak → resolve |
| **Final-Frame Hand-off** | Part 1 ends on a pause-state pose; Part 2 starts on that exact state |
| **Pixel-Priority Doctrine** | Face > eyes > hands > environment; never inverse |

## The named language

> **Two-Part Cinematic Reveal with Continuous BGM**

Three things packed into one name. "Two-Part" flags that this is a two-prompt workflow, not one. "Cinematic Reveal" flags the genre — character introduction, not action. "Continuous BGM" flags the hardest constraint, the one the model's prior most wants to violate: the music must not restart.

## 48-hour takeaway

Continuity is a contract, not an assumption.

Anything that needs to survive a prompt boundary — character identity, room ambience, BGM key, visual state — must be named in both prompts. Saying it once in Part 1 and hoping Part 2 inherits it is a recipe for a restart. The model's default between sessions is to begin clean. To defeat that default, you write the inheritance into the second prompt's opening section as a *new* rule the model will follow.

Three more principles worth keeping:

**1. Pose libraries beat pose invention.** A character that has 9–10 photographed poses in Picture 1 can do 30 seconds of varied shots without the model inventing a single new pose. The trick is to never say "show new poses." Say: "treat these as the ONLY approved major poses." This makes the library a constraint, not a suggestion.

**2. Non-repetition lists beat non-repetition platitudes.** "Don't repeat Part 1" is too vague. Listing the exact six shot mechanisms Part 1 used gives the model concrete things to avoid. Vague rules get vague compliance.

**3. Final-frame design is hand-off design.** Part 1's last shot is not a closing shot — it's a *pause-state pose* that Part 2 opens on. The last 1.4 seconds of Part 1 and the first 0.9 seconds of Part 2 are designed together as one continuous breath. The seam disappears when both ends of it are written as handoff.

## The final prompt

See [`prompt.md`](./prompt.md) for both Part 1 and Part 2 in full (usage notes in Chinese + structured English prompts).

The prompt file is organized as:

1. **Usage notes** — two-Picture architecture, BGM contract, non-repetition doctrine
2. **Part 1 (0–15s)** — Eye hook → face reveal → 9 poses with editorial cut grammar → pause-state hand-off
3. **Part 2 (15–30s)** — Continuation from Part 1 final state → escalation montage → Hero reveal → final key visual

Each part has its own beat-indexed shot table (13 cuts each, 26 total), its own negative-list, and matching continuity contract clauses for character / church / BGM / sound design.

## Result

A 30-second two-part character trailer that reads as one film:

- **Part 1 (0–15s):** Eye extreme close-up → face reveal → nine photographed poses strung together with hard cuts, graphic matches, architectural wipes, negative-space compositions, and a shutter-transition final pose held as a pause-state hand-off
- **Part 2 (15–30s):** Continues from Part 1's final pose, escalates tempo through a rapid detail montage and a five-beat character peak, resolves with a slow Hero Reveal into a clean final Key Visual — face locked to Picture 2, character large and dominant, restrained church ambience, sustained instrumental chord
- **Continuous BGM and room ambience** across the seam, with no musical restart, no new church, no character redesign
- **No shot mechanism repeats** between halves — Part 1's eye-hook / face-reveal / architectural-wipe grammar is explicitly absent from Part 2, which uses a different visual vocabulary (callback reinterpretation, rapid detail montage, architectural cut, rhythmic pose montage, momentary silence, peak build, Hero reveal)

## Tags

`#H3` `#prompt-engineering` `#character-reveal` `#two-part-workflow` `#continuous-bgm` `#pose-library` `#face-lock` `#beat-indexed-cuts` `#motion-graphics` `#church-aesthetic` `#cinematic-trailer`
