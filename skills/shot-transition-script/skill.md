---
name: shot-transition-script
description: Analyze a pair of start-frame and end-frame images to determine visual style, image quality, materials, characters, lighting, and special effects, then generate a detailed mid-transition shot script of a user-specified duration. Use when the user uploads two images (a first frame and a last frame), asks to generate a transition script between them, or mentions creating a mid-sequence shot list for a video transition. Also triggers on keywords like "首尾帧", "过场脚本", "transition script", "首帧图", "尾帧图", "中间过场", and "shot transition". The output is a Markdown file containing visual analysis and a timed shot-by-shot transition plan.
---

# Shot Transition Script

Generate a professional mid-sequence transition script between a start-frame and end-frame image.

## Workflow

1. **Accept inputs**
   - First-frame image (start keyframe)
   - Last-frame image (end keyframe)
   - Target duration for the transition (e.g., "15s", "5s", "30s")

2. **Visual analysis** (for each image, compare side-by-side in the output)
   - **Style**: Overall aesthetic (cinematic, anime, realistic, stylized, abstract, etc.)
   - **Image Quality**: Resolution impression, sharpness, noise, compression artifacts, color depth
   - **Materials**: Surfaces, textures, fabric, metal, glass, skin, organic vs. synthetic, PBR qualities
   - **Characters**: Presence, count, pose, attire, expression, movement direction, focal points
   - **Lighting**: Key light direction, color temperature, mood, shadows, bounce, rim light, time-of-day feel
   - **Special Effects**: Particles, glow, lens flares, motion blur, depth of field, chromatic aberration, fog, haze, volumetrics, other VFX

3. **Cross-frame comparison**
   - Identify shared visual elements and matching features between the two frames
   - Note differences that will need bridging (camera angle, lighting shift, object presence, character position)
   - Assess similarity level to guide the complexity of the transition (e.g., simple cut-like dissolve vs. complex multi-shot sequence)

4. **Determine transition strategy**
   - Based on similarity, choose a transition approach:
     - **High similarity** (same scene, same subjects, slight camera move): Simple continuous motion or very few intermediate shots
     - **Medium similarity** (same scene, different angle/lighting): 2-5 bridging shots
     - **Low similarity** (different scene/location, different subjects): Complex montage with visual metaphors or match-cuts
   - Choose transition type: match cut, dissolve, wipe, morph, continuous camera movement, graphic match, or thematic bridge

5. **Generate timed shot-by-shot transition script**
   - Divide the user-specified total duration into individual shots with precise timestamps
   - For each shot include:
     - **Timestamp** (e.g., `00:00:00.000` - `00:00:03.500`)
     - **Shot Type / Camera**: e.g., Wide shot, Close-up, Dolly in, Crane up, Tracking, Pan, Tilt, Handheld, Static, Drone
     - **Subject / Action**: What appears and what happens in this interval
     - **Lighting / Atmosphere**: How light and mood evolve
     - **Effects**: Any VFX, particles, transitions, or post-processing
     - **Purpose / Narrative Function**: Why this shot exists in the sequence (bridging element, emotional beat, visual continuity)
   - Ensure the sequence logically bridges the start frame to the end frame
   - Ensure the sum of all shot durations equals the requested total duration

6. **Output a Markdown file**
   - Save the result as `<timestamp>_transition_script.md` in the active workspace
   - Structure:
     ```markdown
     # Transition Script — <Total Duration> Mid-Sequence

     ## 1. Frame Analysis

     ### Start Frame (首帧)
     - **Style**: ...
     - **Image Quality**: ...
     - **Materials**: ...
     - **Characters**: ...
     - **Lighting**: ...
     - **Special Effects**: ...

     ### End Frame (尾帧)
     - **Style**: ...
     - **Image Quality**: ...
     - **Materials**: ...
     - **Characters**: ...
     - **Lighting**: ...
     - **Special Effects**: ...

     ### Cross-Frame Comparison
     - **Similarities**: ...
     - **Differences**: ...
     - **Similarity Assessment**: High / Medium / Low
     - **Transition Strategy**: ...

     ## 2. Transition Script (<Total Duration>)

     | Shot | Timestamp | Duration | Camera | Subject / Action | Lighting / Atmosphere | Effects | Purpose |
     |------|-----------|----------|--------|------------------|----------------------|---------|---------|
     | 1 | 00:00:00.000 - 00:00:02.500 | 2.5s | ... | ... | ... | ... | ... |
     | 2 | ... | ... | ... | ... | ... | ... | ... |
     ...

     ## 3. Summary & Notes
     - Total shots: N
     - Total duration: Xs
     - Key continuity devices: ...
     - Recommended rendering settings: ...
     - Optional variations: ...
     ```

## Constraints & Best Practices

- **If the user does not specify a duration**, default to **10 seconds** and explicitly state the default.
- **If only one image is provided**, ask the user to provide the second frame before proceeding.
- **If more than two images are provided**, ask the user to clarify which is the start and which is the end, or treat the first and last as the keyframes.
- **Shots should be as short as 0.5s** for fast cuts, and no longer than 5s per shot unless the transition is intentionally slow.
- **Always explain the visual continuity** between adjacent shots so the transition feels deliberate, not random.
- **When the two frames share a common element** (color, shape, object, character), use it as a match-cut or graphic bridge.
- **Use filmmaking terminology** for camera movements and shot types to ensure the script is production-ready.
- **Include technical notes** for AI video generation tools where relevant (e.g., motion prompts, camera controls, seed continuity).

## Output Format

The final deliverable is a single Markdown file with all analysis and the timed shot list. The file must be saved in the current workspace and the path returned to the user.
