# Format1 VideoExpress Clip Prompt

Create **ONE vertical 9:16 clip, maximum 10 seconds**, using VideoExpress's actual supported duration. Duplicate this template for every scene. Maintain identical immutable character and voice descriptions across prompts. Never substitute realistic humans for requested 3D animated characters.

**Part / scene:** [part ID / clip number / name]  
**Duration:** [actual app selection: >0s and ≤10s]  
**Output:** vertical 9:16, target 1080 × 1920  
**Visual style:** [same precise project style throughout]  
**Location:** [exact space/layout and time/lighting]  
**LOCATION LOCK:** [paste the immutable master layout and exact environment reference ID; reuse unchanged for every clip in this location]  
**VEHICLE / TRAVEL LOCK (when applicable):** [same exact vehicle identity/design and cabin; driver/passenger seating; camera mount; road, correct lane, direction, speed range, route landmarks, terrain, roadside scenery, weather, time and lighting]  
**CAMERA-FACING DRIVER / FRONTAL CAR LAYOUT (when applicable):** If the driver looks toward the camera, place the driver's face/upper body on screen-right. If the car's front faces the camera, place the car in the screen-left half (prefer the left third when shot scale allows), fully within its correct lane; never straddle the centerline, lane divider or shoulder. Preserve physically correct steering-wheel/seat sides; never mirror the whole image or swap occupants. Hold these positions across matching clips. Reframe the camera if needed instead of moving the car into the wrong lane.  
**CONTINUOUS MOTION RULE (for a moving vehicle):** The car is already traveling in the first frame and continues traveling without slowing to a stop, idling, parking, restarting or resetting through the final frame and across every adjacent clip. Keep direction, lane and speed range stable. Show visible forward travel with road markings advancing and roadside scenery sliding backward at consistent parallax. Stop only if the script explicitly says to stop.  
**FRAME CONTINUITY LOCK:** First and last frames are one continuous scene. Keep the same set, camera axis/framing, lighting, furniture, landmarks and prop placement; change only the action, pose, or story-required prop state.  
**Reference assets:** [supplied character images and, if supported, prior clip's actual last-frame image]

**Characters / fixed voice anchors**
- [Name 1]: [paste exact unchanging face, hair, proportions, clothes, shoes, source voice/reference, unique VoiceChanger target/profile ID, and locked accent, tone, pitch, speed and loudness settings]
- [Name 2]: [same; a distinct character-specific voice identity and profile]
- **Only the listed characters appear.** Preserve each voice identity and assign each line only to its intended speaker. Repeat the assigned character's locked VoiceChanger profile/settings in the audio map; never swap profiles.

**START / first frame:** Immediately continue clip [previous ID] at its ending instant: [camera shot/framing, location, exact pose, screen placement, eye direction, which hand holds which prop, light and background]. Use the actual last rendered frame of clip [previous ID] as the start-image/reference when the story remains in the same scene. Match the approved location master exactly. No teleporting, background swap or unexplained time jump.

**ONE MAIN ACTION:** [single physically plausible movement with direction and timing]. For continuous driving, maintain forward travel for the entire clip; no stopping or restarting at the opening or ending. Keep faces and outfits unchanged, body anatomy natural, and props stable. Use one uninterrupted shot; preserve the location master, camera axis, framing, lighting and surroundings from start to end. Allow camera movement only when both keyframes plan it. Make no background, furniture, landmark or lighting changes.

**DIALOGUE / speech audio:**  
[NAME] ([same source voice ID and locked VoiceChanger profile/settings from the character bible in every clip]): "[Exact concise English sentence.]" [Accurate speaking lip-sync; keep timecode for VoiceChanger replacement.]  
[NAME, if needed]: "[Exact second short sentence.]" [Only this person speaks their line; listener stays silent.]

**Narration:** [None unless requested.]  
**SFX / music:** [scene-specific sounds and continuous music/ambience; keep speech audible].

**END / last frame:** [precise final camera composition, subject positions, gesture, gaze, hand/prop placement, ongoing movement and light]. Keep the same continuous environment and camera setup as the first frame; change only the planned action/pose/prop state. For an uninterrupted drive, the car is still moving in the same direction, lane and speed range, with the road and scenery at the next expected point. This exact instant becomes the next scene's starting state when the story continues without a scripted cut. Save/reuse the rendered final frame when supported.

**STRICT NEGATIVE TEXT RULE — NO SUBTITLES:** Do not generate subtitles, captions, onscreen dialogue text, title cards, lower thirds, logos, watermarks, visible UI, signs, labels, lettering, gibberish glyphs or any other readable text anywhere in ANY frame.

**Other negatives:** No changed faces/hair/clothing/shoes or voice, extra humans, duplicate characters, extra fingers/hands/arms/limbs, morphed objects, switching prop ownership, impossible door directions, background swaps, environment drift, furniture/landmark changes, lighting jumps, reversed walking direction, unrequested narrator, overlapping wrong speaker, jump cuts or unplanned camera angle changes. During continuous driving, no stopping, idle car, start/stop reset, frozen road, scenery reset, lane jump, route jump, direction reversal, sudden speed change or changing vehicle/cabin.

**Acceptance check (after rendering):** actual clip ≤10 seconds, 9:16; no text; same characters and voices; correct speaker lip-sync; correct physical continuity; ending frame matches subsequent start. Retake material failures if authorized; do not claim verification without viewing the result.
