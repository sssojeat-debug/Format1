# Format1 Voice Consistency and Lip-Sync Workflow

Use this workflow for every Format1 project with dialogue from more than one character, or whenever the user requests consistent character voices. Run the stages in this order:

**Video Split → Audio Save → VoiceChanger → replace/sync audio → review → export.**

Keep visual clip timing, clip order, character identity, and dialogue assignment as the source of truth. Do not claim a stage is complete unless the app shows the saved output or the timeline has been inspected.

## 1. Lock one voice profile per character

Before processing dialogue, complete the voice section of `templates/CHARACTER_BIBLE.md` for every named speaking character. Give each person an independent profile and reference recording. Record:

- Character ID and dialogue labels used in the script.
- VoiceChanger target/model or approved reference voice.
- Language and accent; vocal age/style, timbre, pitch, and speaking rhythm.
- Pitch, speed, loudness/normalization, and any strength or mix settings that the current VoiceChanger interface exposes.
- Approved sample/reference filename and a short pronunciation note if needed.

Once a sample is approved, freeze that character's VoiceChanger selection and settings for the whole project. Reuse them on every line and every scene. Do not apply one character's profile to another character, combine multiple people into one conversion pass, or silently change settings between clips.

**Starter defaults when the user has not chosen another profile and the current interface exposes them:** English (US), pitch 0, speed 0.9; use `RVC_US_Male_1` or `RVC_US_Female_1` as a starting target when it fits the approved character voice. Confirm the actual target names/settings shown by VideoExpress; if unavailable, record the available user-approved voice ID/reference and keep that exact choice fixed. Distinct characters must still have distinct approved voice identities, even when their accents or gender presentation are similar.

Example profile rows:

| Character | VoiceChanger target/reference | Language/accent and voice character | Pitch | Speed | Loudness/other controls | Locked |
|---|---|---|---:|---:|---|---|
| Jack | RVC_US_Male_1 or approved Jack reference | English (US), natural warm male voice | 0 | 0.9 | Normalize consistently; record available controls | Yes after sample approval |
| Mia | RVC_US_Female_1 or approved Mia reference | English (US), natural warm female voice | 0 | 0.9 | Normalize consistently; record available controls | Yes after sample approval |

These are starter profiles, not a claim that the app currently exposes a particular model. If the story has different characters, build and lock their own rows rather than reusing Jack/Mia's identities.

## 2. Video Split

1. After the scene clips are generated, open the Format1 project and use **Video Split** to separate the movie into its numbered scene clips.
2. Preserve exact scene order, original clip boundaries, and each clip's start time. Do not split through a word, move a cut, or change a scene's duration just to process audio.
3. Where a clip contains more than one speaker, split or mark audio turns at the speaker boundaries when the tool supports it. Keep overlaps explicitly marked; do not assign overlapping speech to the wrong character.
4. Use stable IDs such as `C01`, `C02` and include speaker tags such as `C01_JACK` or `C01_MIA` in the audio map.

## 3. Audio Save

1. Use **Audio Save** on the split clip/turn to save the original dialogue audio separately.
2. Save a clean copy before conversion. Keep the original file and note its exact timeline in/out points.
3. Name each source by clip and speaker, for example `C01_JACK_SRC.wav` and `C01_MIA_SRC.wav`. Save the clean reference samples as `VOICE_REF_JACK.wav` and `VOICE_REF_MIA.wav`.
4. Keep dialogue for different characters in separate files. If Audio Save produces a mixed track, isolate the speaker turns using Video Split or the available editing controls before VoiceChanger. Never use a mixed two-speaker recording as one character's reference.
5. Retain source timing, pauses, room tone, and useful SFX/music as separate elements whenever the editor allows it.

## 4. VoiceChanger

1. Process each speaker's source audio separately through **VoiceChanger**, using that character's locked target/reference and exact saved settings.
2. Use the same profile for every line by that person. Do not change pitch, speed, accent, strength, or model between clips to compensate for a bad line; reprocess the defective line with the locked profile.
3. Save each result with a matching ID, for example `C01_JACK_VC.wav`. Keep source audio untouched until the converted result passes review.
4. Compare every converted line against that character's approved voice sample and neighboring scenes for identity, accent, pitch, rate, loudness, pronunciation, clipping, artifacts, and natural pauses.
5. If conversion changes duration or adds latency, preserve the original dialogue's in/out timing. Correct only the necessary offset or slight duration difference, without making speech unnaturally fast or slow. Reprocess with the same profile if a line no longer fits.

## 5. Replace audio and synchronize

1. Place each converted dialogue file under its matching video clip at the original start time and speaker turn. Use the clip/speaker ID map; never rely on filename order alone.
2. Mute or remove only the replaced source dialogue to prevent doubled speech. Keep ambience, music, and SFX on their own tracks and at the original story positions.
3. Align the first audible phoneme with the character's first mouth movement; check a middle syllable and the last word before the cut. The assigned speaker moves their mouth; listeners remain silent. Keep lip-sync natural and exact dialogue unchanged.
4. Check every clip boundary for silence gaps, duplicate lines, audio tails cut off, and voice or ambience jumps. Verify synchronization again after all clips are assembled; do not assume conversion preserved timing.
5. If the converted dialogue cannot be synchronized with the available controls, restore the original audio for that line or clip and report the limitation instead of leaving visibly incorrect lip-sync.

## 6. Final voice and sync gate

Before export, play the assembled sequence and check all dialogue transitions. Confirm:

- Every character has the correct, unique, unchanged voice profile in all scenes.
- The line belongs to the intended speaker and the line is not clipped, duplicated, or assigned to a listener.
- Pitch, speed, accent, timbre, and loudness remain stable across scene boundaries, including the last clip. Compare each character's final line with the approved reference and earlier lines; if it differs, reprocess that line with the same locked profile/settings and review again.
- Converted speech stays synchronized from first mouth movement through the end of each line; there is no cumulative timing drift.
- Source speech is not doubled, while required music, ambience, and SFX remain.
- The final MP4 is reviewed for voice identity and lip-sync after export.

Record the result in `templates/ASSEMBLY_QA.md`. If Video Split, Audio Save, VoiceChanger, or a required sync control is unavailable, mark that exact stage blocked; never state that audio was processed or synchronized when it was not.
