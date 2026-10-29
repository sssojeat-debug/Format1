# VideoExpress Cinematic Story Creator — Format1

Format1 is a production workflow for connected cinematic stories made from short VideoExpress clips, then assembled into a final movie. It covers script, character and voice locks, clip prompts, rendered-clip quality checks, timeline assembly, export, and honest delivery status. Use the supplied project brief and reference assets as the source of truth.

## Repository layout

    README.md                          — workflow and production rules
    SYSTEM_PROMPT.md                   — instructions for the production agent
    templates/PROJECT_BRIEF.md         — project-specific decisions
    templates/CHARACTER_BIBLE.md       — immutable character, voice, location, and prop locks
    templates/SCENE_PLAN.md            — timed clips and frame-to-frame handoffs
    templates/VIDEOEXPRESS_PROMPT.md   — self-contained prompt for each clip
    templates/ASSEMBLY_QA.md           — clip inspection, timeline and MP4 export checklist

## Non-negotiable Format1 production standards

1. **Vertical video:** 9:16, target 1080 × 1920 pixels for every generated clip and the final MP4. Avoid stretching or cropping away essential subjects. An explicitly different user request requires an updated brief before production.
2. **Maximum 10 seconds per generated clip:** select a supported VideoExpress duration at or below 10 seconds; never submit an individual clip over 10 seconds. Longer stories use sequential clips. Check the actual output duration.
3. **Continuous scenes:** clip N+1 begins at the exact story moment where clip N ends, with the same character positions, actions, props, screen direction, lighting, and background. Reuse clip N's actual last frame as clip N+1's starting image/reference when the available tools support it. Otherwise specify a matching opening keyframe and verify by viewing the join; do not claim exact pixel-level identity.
4. **Locked characters and voices:** preserve supplied reference faces, hair, proportions, outfits, shoes, gestures, speaker identities, voice timbre, accent, and speaking style. Use the same voice selection/reference every time if available; do not switch voices for a recurring role or accidentally give dialogue to another character.
5. **STRICT NO SUBTITLES:** every prompt must prohibit generated subtitles, captions, title cards, lower thirds, labels, overlays, UI text, logos, watermarks, and other readable on-screen text. Inspect every rendered clip. Reject or regenerate a clip containing unintended text; never accept it merely because the story is otherwise correct. If the user later requests Khmer/English subtitles, those belong in separate post-production files/layers, not in the generated clip.
6. **Audio and anatomy:** use exact dialogue, short enough for each clip, with correct speaker lip-sync. No unintended narration, extra cast, extra hands/fingers/limbs, warped faces, duplicated objects, or unmotivated transitions.
7. **Final film required for an end-to-end request:** assemble approved clips in order, verify transitions and sound, export a combined vertical MP4, and check the exported file. Distinguish a planned prompt, generated clip, assembled timeline, and verified MP4.

## End-to-end workflow

1. **Read the brief.** Reuse existing story, references, instructions and user-approved parameters. Confirm whether the request is to write a script, prepare assets, generate clips, or finish an assembled MP4. Do not repeatedly ask for details already provided.
2. **Script and break into parts.** Write the story beats and dialogue. Keep real-world movement and travel physically plausible. A roughly 5-minute segment needs *at least* 30 clips if all are 10 seconds; use more if individual clips are shorter. For an hour, plan twelve roughly 5-minute parts, each with its own join to the next.
3. **Lock references.** Fill CHARACTER_BIBLE with one immutable description per character, including face, wardrobe, shoes, voice anchor, accent and speech characteristics. Lock location geometry, time of day and props.
4. **Build the timed scene plan.** One row per generated clip: time, action, camera, exact dialogue, audio, starting frame/pose, ending frame/pose, and dependency on the preceding clip. Make dialogue and movement feasible within the chosen duration (10 seconds or less).
5. **Generate visual anchors.** Use supplied images and/or a consistent keyframe when supported. Before rendering the next clip, inspect the previous clip's end frame. Reference that end frame for the next opening, if possible. Keep visual style and composition stable.
6. **Prepare one self-contained prompt per clip.** Copy the same character and voice locks into every applicable prompt. Clearly state the opening composition, single primary action, closing pose, exact words, voice, lip-sync, 9:16, maximum 10 seconds and STRICT NO SUBTITLES.
7. **Execute through VideoExpress only when available and authorized.** Verify the actual app mode and permitted duration, ratio, reference, voice, and audio options. Generate in small controlled batches so failed clips can be corrected without disturbing good ones. Report credit estimates shown by the app, if any; do not invent limits or claim browser access without an operational tool.
8. **Inspect every rendered clip.** Check duration and vertical frame, correct cast, face/wardrobe/voice, speaker lip-sync, anatomy, object continuity, background, movement direction and *zero readable text*. Reject defects and regenerate affected clips when authorized. Review the pairwise handoff between consecutive clips.
9. **Assemble the timeline.** Add only approved clips in scene-number order without gaps or duplicates. Trim to the actual clip boundaries, maintain continuity, and balance dialogue, music and SFX. Use motivated cuts; never add an unrelated establishing shot that breaks the chain.
10. **Export and validate.** Export one MP4 for the requested part or film, 1080 × 1920 vertical target, with compatible video/audio encoding (H.264 video and AAC audio if supported). Play the exported MP4 from beginning to end; verify picture, sound, duration, joins, correct clip order, and no generated subtitles. Follow templates/ASSEMBLY_QA.md.
11. **Deliver status truthfully.** Give the real project location and verified asset details. Mark missing or unverified items explicitly. A written prompt does not equal a submitted job, and a set of clips does not equal an exported MP4.

## Timing examples

| Requested length | Clip planning | Assembly |
|---|---|---|
| 60 seconds | At least six clips at 10 seconds, or more shorter clips | One 60-second timeline if rendered durations add up |
| 5 minutes | At least thirty clips at 10 seconds, or more shorter clips | One part, typically around 5 minutes |
| 1 hour | Twelve roughly 5-minute parts (at least 360 ten-second clips for exactly 60 minutes) | Export parts and, if requested, a single combined movie |

Time totals are planning targets: use actual clip durations to calculate timeline length. Never speed up dialogue or insert unrelated footage merely to meet a nominal duration.

## Project options

The brief defines story, tone, visual style (animated 3D or realistic), narration, dialogue, music, SFX, reference cast, and final length. If an unusual project requires a change to 9:16 or the no-subtitles standard, ask for or follow an explicit revised instruction and record it in the brief. The maximum 10-second constraint applies to VideoExpress individual clip generation in this workflow.

## Production limitations

Prompts cannot guarantee perfect faces, voice identity, exact first/last frames, accurate lip-sync or zero text. Review actual renders. If the current VideoExpress interface cannot accept a last-frame reference, voice lock, timeline assembly or MP4 export, document the limitation and use only tools actually available; do not fabricate actions or claim that a finished video exists.

## Safety and permissions

Creating or editing files in this GitHub repository is separate from logging into VideoExpress, purchasing credits, deleting projects, publishing media or sharing videos. Perform account-affecting actions only within the user's authorization. Never put passwords or private account tokens in repository files.
