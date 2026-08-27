# `AI JOINS THE TEAM` bench-reaction keyframes v1

**Date:** 2026-08-26  
**Mode:** Built-in image generation  
**Purpose:** Matched first and last frames for an 8-second Veo bench-reaction clip  
**Campaign brief:** [AI Joins the Team](../../../campaigns/ai-in-the-80s-hockey-campaign-brief.md)  
**Uniform/style reference:** [AI own-goal frame](../../photography/campaign-concepts/ai-in-the-80s-human-player-own-goal-v1.png)

> **Superseded character note — 2026-08-26:** Campaign brief v0.2 changes `THE COACH` to a gruff man aged 62–68. The v1 keyframes and prompts below preserve the earlier female-coach generation for provenance. They may be used as composition references only and must not be used as final Veo first/last frames. Generate a v2 pair with the locked older male coach before production.

## Deliverables

- `bench-reaction-start-frame-v1.png` — players tense and watching the promising offscreen play.
- `bench-reaction-end-frame-v1.png` — the same players, coach, camera, arena and lighting after the play ends badly.
- `bench-reaction-keyframes-v1.png` — side-by-side continuity comparison; not a Veo input.

For Veo, use the start and end files individually. Keep the generated video at 16:9 and protect the central 4:3 composition for later crop.

## Opening-frame generation prompt

```text
Use case: ads-marketing
Asset type: opening keyframe for an 8-second Veo image-to-video shot in the “AI Joins the Team” campaign
Primary request: Create the exact first frame of a locked-off front-facing shot of a fictional 1983 Canadian minor-league hockey players bench. Four adult male players sit shoulder-to-shoulder, tense and quiet, watching promising hockey action occurring entirely offscreen just past the camera. Two lean forward with gloved hands ready on the top of the boards. Behind them, the recurring female coach paces slowly from left to right holding a battered clipboard and orange grease pencil. Everyone is focused on the same offscreen play; this is the still moment immediately before the bench cheers.
Input images: Image 1 is the approved campaign reference for team uniform, rink palette, early-1980s film texture, and player-world continuity only. Do not recreate its on-ice own-goal action. The human player AI is offscreen and must not appear.
Scene/backdrop: same fictional small Canadian community arena world as Image 1; green-grey painted cinderblock, scratched and fogged rink glass, narrow wooden players bench, scuffed off-white boards across the lower foreground, weak fluorescent arena lighting, sparse indistinct crowd beyond glass. No ads or readable scoreboard.
Subjects: four mixed-age adult male players in their 30s and 40s with ordinary athletic builds and naturally tired faces. Preserve a recurring ensemble: one dark-curly-haired player with a neat moustache; one lean clean-shaven player with short brown hair; one stockier player with receding dark hair; one younger-looking player with shaggy dark hair. Female coach is 48–55, average height, practical bearing, light-to-medium skin, short dark hair with grey at temples, lined expressive face, navy cardigan over cream blouse and dark trousers.
Wardrobe: team uniforms must match Image 1: warm-cream jerseys, navy shoulder yokes and cuffs, narrow faded-rust and muted-gold stripes, navy pants, worn brown gloves. No logos, sponsors, names, numbers, helmet text, or real team identifiers. Coach carries the same clipboard and orange grease pencil.
Style/medium: photorealistic fictional early-1980s sports-comedy film frame; captured on soft 16mm and transferred to worn consumer video; muted cream, navy, rust, brown and rink green; weak green fluorescent cast, visible grain, mild gate weave, restrained chroma bleed and very light bottom-edge tracking texture. Genuine period image, not modern footage with a filter.
Composition/framing: 16:9 landscape generation with every essential person and action protected inside the central 4:3 safe area for later crop. Camera locked on tripod across the ice at rink level, front-facing medium-wide 50–70mm broadcast-lens view. Top edge of boards crosses the bottom of frame. Players visible from waist/chest upward; coach fully visible behind them in mid-stride. Imperfect early-1980s broadcast framing, but no tilt, no camera movement, no view of the on-ice play.
Lighting/mood: tense anticipation, dry and affectionate, natural adult expressions, no mugging.
Constraints: this is the opening frame before any cheering; all four players remain seated and quiet; hands may rest on boards but nobody is clapping, shouting, standing, pointing or looking at camera. AI player remains offscreen. No text, logo, trademark, watermark, subtitle, robot, futuristic effect, data overlay, violence, blood, fighting, modern object or recognizable film character.
Avoid: copying any existing hockey movie, professional sports advertising, glossy retro fashion shoot, synthwave, exaggerated comedy faces, crowded bench, modern protective equipment, cutaway to ice, shallow modern bokeh.
```

## Ending-frame edit prompt

```text
Use case: identity-preserve
Asset type: ending keyframe for the same 8-second Veo image-to-video shot
Input images: Image 1 is the exact edit target and approved opening keyframe. Preserve it with maximum fidelity.
Primary request: Change only the characters' body language and expressions to show the moment after the offscreen play has ended badly and the coach has finished her dry comment. The four players have settled back into dejected silence. The coach has stopped behind them, looking toward the same offscreen action with tired resignation. This is the final still frame of the same continuous locked camera shot.
Required performance changes only:
- Keep all four players seated in the same left-to-right order and at the same bench positions.
- Player 1, the curly-haired moustached man, drops his gaze toward his gloves with shoulders slumped.
- Player 2, the lean short-haired man, sits back slightly with hands lower on the boards, staring blankly ahead.
- Player 3, the stockier receding-hair man, exhales and sags heavily, forearms resting on the boards, disappointed.
- Player 4, the shaggy-haired man, lowers his head slightly and looks toward the ice with a defeated expression.
- The female coach remains behind the same players with the identical face, hair, navy cardigan, cream blouse, clipboard and orange grease pencil. She has stopped walking, shoulders slightly lowered, looking offscreen with a dry exhausted expression. Her mouth is relaxed and closed, as if she has just finished saying the line.
Invariants: preserve the exact camera position, 16:9 crop, central 4:3 safe composition, focal length, background architecture, rink glass, spectators, lighting, color grade, grain, analog transfer texture, board scratches, sticks, every person's identity, age, hairstyle, facial structure, uniform construction, glove design, scale, order and placement. Preserve the same fictional 1983 arena and the same frame geometry.
Constraints: change only posture, hand height within natural limits, gaze and facial expression. Do not add, remove, replace or redesign any person, prop, uniform, stick, spectator, board, glass panel or background detail. Nobody cheers, points, stands, shouts, smiles or looks into camera. AI remains offscreen. No new text, logo, trademark, number, name, subtitle, watermark, robot, modern object, motion blur, camera movement or cutaway.
Avoid: identity drift, face changes, wardrobe changes, different number of players, coach relocation, different rink, altered camera angle, altered lighting, exaggerated sadness, crying, anger, comedy mugging, collapse, injury or visual effects.
```

## Continuity notes

- The ending frame is an edit of the opening frame, not a separately generated composition.
- Player order, identities, coach, sticks, spectators, glass seams, camera and arena geometry match closely.
- The primary controlled transition is gaze/posture: alert forward attention becomes shared resignation.
- The coach's mouth is closed in both keyframes. Veo may generate her spoken line during the transition; if dialogue or lip motion is unreliable, keep the visual and replace the sentence in post.
