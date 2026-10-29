# VideoExpress Cinematic Story Creator

A practical workflow for turning a story idea into short, connected VideoExpress clips. It is tailored to the creator's established preferences while keeping style, characters, subject matter, language, runtime, and subtitle choices configurable per project.

## Repository layout

```text
videoexpress_creator_workflow/
├── README.md                         # Start here: setup and end-to-end workflow
├── SYSTEM_PROMPT.md                  # Instructions for the production agent
└── templates/
    ├── PROJECT_BRIEF.md              # Fill in one project before production
    ├── CHARACTER_BIBLE.md            # Reusable character continuity records
    ├── SCENE_PLAN.md                 # Timed scene and handoff template
    └── VIDEOEXPRESS_PROMPT.md        # Per-clip prompt template and negative locks
```

## Defaults for this creator

- Vertical 9:16, 1080 × 1920, unless the brief specifies another ratio.
- Short social clips are about 60 seconds. Longer films are split into reviewable parts; each part gets its own beat map and clear handoff.
- Use the requested visual style. For the creator's animated series, use cinematic 3D and preserve supplied character references; don't force a named studio style unless the brief asks for it.
- No generated subtitles, captions, titles, logos, or readable signs in the video. Add subtitles later in editing when requested. The common subtitle layout is Khmer near 7% from the top and English near 17% from the bottom, bold when requested.
- Dialogue must be short, natural English with clear speaker attribution and lip-sync instructions. Narration is optional and must not conflict with dialogue.
- Keep sound effects and music distinct from dialogue. No unwanted narrator, extra characters, extra limbs, duplicated props, or unintended text.
- Generate and submit in VideoExpress only when the user explicitly asks for execution and the app is accessible. A prepared prompt or production package is not a finished video.

## Workflow

1. **Read the project brief.** Reuse details already supplied. Ask only for missing information that materially changes the story or production. If useful, propose a compact outline first for review.
2. **Lock the story.** Define the hook, character goal, obstacle, escalation, payoff, and ending. Keep historical claims sourced and distinguish documented facts from dramatization for factual stories.
3. **Lock continuity.** Record each character's name, face, hair, clothes, shoes, voice, and recurring props. Apply the same immutable description to every applicable scene. Do not invent cast or change wardrobe mid-story.
4. **Build the scene plan.** Divide the runtime into connected scenes or clips. Each row has time, location, framing, one main action, dialogue/narration, audio, continuity in, and continuity out. A scene's final pose or image should motivate the next scene.
5. **Prepare generation prompts.** Use one clear primary action per clip, specific framing, subject positions, visible cast, prop ownership, motion direction, lighting, and an explicit ending pose. Put negative constraints in direct language.
6. **Generate in controlled batches.** Confirm the target ratio and duration in the interface before submission. If a user has not authorized generating or spending credits, deliver the prompts for review instead. Do not claim that VideoExpress was used unless a job was actually submitted and its result confirmed.
7. **Review and assemble.** Check the rendered clip for correct scene, duration, continuity, dialogue, accidental subtitles/text, duplicated or missing objects, and abrupt joins. Fix only material defects; don't claim visual or lip-sync verification unless performed.
8. **Deliver clearly.** State what was created, where it can be found, what was verified, and what remains unverified. Provide prompt files, subtitle files, or cover art when requested.

## Suggested duration and scene counts

For roughly 60 seconds, use 7–9 scenes of about 6–9 seconds, or more short beats if the generator handles them reliably. Let dialogue length fit the clip: usually one concise line per speaker per beat. For a 5-minute or 1-hour project, split into parts and review each part's outline before expanding the whole production.

## Project-specific overrides

The project brief overrides defaults. Common options:

- **Format:** 9:16 vertical, 16:9 landscape, or another requested ratio.
- **Style:** realistic human, cinematic 3D animation, storybook, documentary reenactment, or a specified visual reference.
- **Audio:** dialogue only, narration, music, effects, or a combination.
- **Text:** no generated text by default; explicitly enable on-screen text only if requested.
- **Subtitles:** off by default; prepare Khmer/English subtitle files separately when requested.
- **Length:** social short, episode, or long-form film split into reviewable parts.

## Important production limits

Text prompts cannot guarantee exact faces, perfect lip-sync, subtitle-free output, or flawless continuity. Review the actual renders when available. Respect the generator's current options and limits; do not invent controls, durations, or completed outputs.
