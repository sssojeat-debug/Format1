# Format1 Connected Clip / Scene Plan

**One row per VideoExpress generation (duration >0 and ≤10 seconds).** Every row is a continuous story moment. Use 9:16 framing and preserve character / voice references throughout. No generated subtitles or other on-screen text.

| Clip / time | Duration (≤10s) | Beat & physical action | Set / cast / camera | Exact dialogue & locked speaker voice | SFX / music | IN: prior clip last frame | OUT: last frame for next clip | QA / status |
|---|---:|---|---|---|---|---|---|---|
| 01 / 0:00–0:10 | 10s | Opening | | | | Opening reference | Ending pose / frame 01 | Planned |
| 02 / 0:10–0:20 | 10s | Continuous next action | | | | Match frame 01 | Ending pose / frame 02 | Planned |
| 03 / 0:20–0:30 | 10s | Next natural beat | | | | Match frame 02 | Ending pose / frame 03 | Planned |

Continue rows until target runtime. A five-minute part needs **at least 30 ten-second clips**, or more if the selected generation length is shorter. Do not invent a single 5-minute generation.

## For each clip
- Reference asset IDs for characters and immutable voice IDs/descriptions:
- Starting shot: same exact moment, positions, face directions, props, lighting, camera as previous clip OUT:
- Action: ONE principal movement, physically plausible within runtime:
- Dialogue: speaker-name / exact short phrase / voice / lip-sync; avoid overlap unless scripted:
- Ending shot: capture the actual last rendered frame as the next start reference if tool allows; otherwise matching keyframe:
- Strict no-subtitles text ban repeated in every generation prompt:
- Generation status: planned / submitted / processing / generated / failed / rejected / accepted / unverified
- Continuity status: matched / retake / unverified

## Part-to-part join
- Last shot of Part N and first shot of Part N+1 must also connect.
- Track scene IDs, approved output filenames and clip durations before timeline assembly.
- Actual runtime = sum of accepted trimmed clip durations, not just planned timestamps.
