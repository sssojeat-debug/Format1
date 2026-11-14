# Format1 — VideoExpress Clip and Assembly Quality Checklist

Use this checklist for a completed film request. A prompt, submitted job, rendered clip, saved timeline and exported MP4 are separate milestones.

## 1. Clip inventory

- Project title and segment/part:
- Total target runtime:
- VideoExpress project location:
- Approved scene ID range:
- Planned clip count:
- Actually generated and accepted clip count:
- Missing/rejected clip IDs:
- Approved clip filenames and actual durations:

For each generated clip:
- [ ] Duration is greater than zero and **no more than 10 seconds**.
- [ ] Vertical **9:16**, target 1080 × 1920, no unintended crop or stretch.
- [ ] Correct visual style, especially cinematic 3D rather than accidental photorealism.
- [ ] Same face, hair, proportions, clothing, shoes and accessories as approved references.
- [ ] Same voice identity, accent, timbre, pacing and locked VoiceChanger profile/settings as character bible; correct speaker.
- [ ] For multi-character dialogue, run Video Split → Audio Save → VoiceChanger separately for each speaker; preserve source audio and original clip/timecode map.
- [ ] Exact intended short dialogue; converted speech reinserted at the original timing with speaker lip-sync checked; no unrequested narrator.
- [ ] No extra or missing people, duplicate characters, extra hands/fingers/limbs or malformed props.
- [ ] Every recurring prop matches its recorded identity/count, holder or resting place, hand, orientation, visibility, and condition at clip IN/OUT; no unexplained disappearance/reappearance, materialization, duplication, morphing, or teleporting. The chip bag stays where the preceding frame/clip left it unless a visible scripted action moves it.
- [ ] **ZERO subtitles, captions, visible words, labels, glyphs, title cards, logos, watermarks or UI text.** Reject and correct any clip that fails.
- [ ] Correct scene location, time, lighting, geometry and plausible movement.
- [ ] Actual last frame recorded for next clip, where supported.
- [ ] Vehicle identity and appearance match the approved vehicle reference across the clip set.
- [ ] In front-facing car shots, the car is on screen-left and fully inside its correct lane; no centerline/lane-divider/shoulder straddling.
- [ ] When the driver faces the camera, the driver appears on screen-right; seat and steering-wheel sides remain physically correct and the shot is not mirrored.
- [ ] For continuous driving, the car is moving from the opening through the ending frame; visible road and roadside scenery move consistently, with no stop/start reset or route/environment jump.

## 2. Frame-to-frame handoffs

| Clip pair | Previous actual last frame | Next actual first frame | Pose/camera/props/light/movement match? | Status / retake |
|---|---|---|---|---|
| 01 → 02 | | | | |
| 02 → 03 | | | | |

Repeat for **every adjacent clip** and for part-to-part boundaries. When possible, use preceding rendered last frame as the next starting image/reference. If not supported, compare frames visually and use a motivated edit; label exact continuity *unverified* unless validated. Ensure hand/prop ownership, speaking turn, screen direction, doors, travel and motion are continuous. Explicitly compare recurring prop states at both sides of every cut; any unexplained vanish/appear blocks acceptance. For a continuous drive, verify that the car does not stop or restart at the cut and that its direction, lane, speed range, road, vehicle interior, weather, lighting and surrounding scenery continue correctly.

## 3. Timeline assembly

- [ ] All accepted clips placed in **scene-number order**, without duplicates, gaps, missing beats or accidental reversed clips.
- [ ] Clip boundaries aligned; no frozen black frames or interrupted dialogue at joins.
- [ ] Clip-to-clip transitions preserve character movement and room geometry.
- [ ] During driving sequences, the same car continues traveling through every cut; there are no stop/start beats, frozen scenery, route jumps, or changes to the vehicle/cabin/environment. Camera-facing driver/car positions stay screen-right/screen-left, respectively, while the car remains in the correct lane.
- [ ] Voices remain matched and intelligible; music and sound effects do not overpower speech.
- [ ] Replacement voice audio is synchronized from first word to last; check offsets and no drift across scene joins. Prevent doubled original dialogue while preserving room tone/ambience and SFX.
- [ ] Room tone/ambience and score continuous where appropriate; no accidental resets at every cut.
- [ ] No on-screen text or subtitle track added inadvertently.
- [ ] Timeline duration calculated from actual trimmed clip lengths, not nominal planned lengths.
- [ ] If producing a multi-part film, exported parts connect naturally; combine parts if requested and supported.

## 4. Final export and verification

- [ ] Final output is a **playable MP4**, vertical 9:16, target 1080 × 1920.
- [ ] Use H.264 video and AAC audio if the available editor supports those options.
- [ ] Verify actual exported duration, resolution, frame rate, audio presence and filename.
- [ ] **Play the exported MP4 from beginning to end** and check all scenes and transitions.
- [ ] Confirm final export has no generated subtitles or unintended readable text, not merely that prompts requested no text. Inspect every scene and dialogue moment, including the final clip; any visible burned-in caption/subtitle blocks delivery and requires a corrected clip/export.
- [ ] Confirm every dialogue line—including the final scene—is audible, assigned to the correct character, synchronized, and consistent with that character's locked reference voice/profile. Compare the last line against preceding lines and the approved sample; any voice change blocks delivery.
- [ ] Preserve the saved VideoExpress/editor project and the approved clip-to-scene mapping.
- [ ] Share verified final file/location only when it exists and is accessible.

## 5. Report accurate status

Record a specific status for each milestone:

| Milestone | Actual status | Evidence/location |
|---|---|---|
| Script and scene plan | Planned / complete | |
| Prompt package | Planned / complete | |
| VideoExpress clips | Not submitted / processing / generated / accepted | |
| Handoffs | Unverified / checked / corrections needed | |
| Timeline | Not assembled / assembled / checked | |
| MP4 export | Not exported / exported / verified playback | |

A GitHub update alone **does not** create a VideoExpress movie. If browser access, frame reference import, voice reference, timeline assembly or MP4 export is unavailable, say which action was blocked. Do not claim completed generation, an assembled film, or background work unless it actually happened.
