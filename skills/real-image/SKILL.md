---
name: real-image
description: "Turn basic image ideas into grounded, paste-ready prompts for believable and realistic images. Use this skill whenever the user asks for an image prompt, realistic photo prompt, RAW iPhone-style image, product image, ad creative, social graphic, poster, image edit, restyle, background generation, text-in-image layout, or a still image that may later be animated. The full method is in this file - ALWAYS read this entire skill before producing anything."
---

# Prompting Skill

Default output: give the user one clean, paste-ready prompt in a code block. No long explanation unless they ask.

The goal is to create prompts that produce believable, usable images. Avoid the over-polished AI look. The best prompts describe what a real camera would see, including ordinary details, imperfect timing, unperformed behavior, real lighting, texture, shadows, grain, and compression.

## Human realism default: candid first

For realistic people in family, lifestyle, caregiving, home, community, workplace, or social scenes, default to a **controlled candid moment** unless the user explicitly asks for a posed portrait, formal group photograph, character sheet, casting sheet, or studio image.

Candid describes the behavior and timing inside the frame. It does not require an iPhone, poor quality, random blur, or careless composition. A candid image may be captured by a smartphone, a documentary camera, or a controlled commercial camera. Choose the camera separately after deciding how the people are behaving.

A convincing candid moment usually includes:

- one ordinary action already in progress
- attention directed toward the task, another person, or something outside the frame
- different eyelines and slightly unequal reaction timing
- asymmetrical posture, natural overlap, or imperfect spacing between people
- hands physically occupied and making believable contact
- one restrained capture imperfection, such as mild motion softness, a natural crop, slight tilt, or autofocus softness
- one environmental imperfection, such as uneven laundry, a partly hidden book, compressed cushions, or ordinary clutter

Use **controlled candidity**, not chaos. Keep the main action readable, important faces recognizable, anatomy stable, and the composition usable. One behavioral imperfection, one capture imperfection, and one environmental imperfection are usually enough.

A scene is probably still staged when everyone is settled, evenly spaced, fully visible, facing the camera, smiling at the same time, and holding their hands safely away from other objects. Documentary camera language alone will not fix staged behavior.

## Core rule

Do not use lazy quality words as the main realism strategy.

Avoid phrases like:

- 8k
- ultra realistic
- hyper realistic
- masterpiece
- cinematic masterpiece
- insanely detailed
- award-winning
- perfect lighting
- flawless skin
- unreal engine
- octane render
- glossy commercial look

These broad quality terms tend to encourage over-polished, stock-like results.

Use the word photorealistic or phrases like "real photograph" or "taken on a real camera" to set the intended realism mode instead of piling on generic quality adjectives. Camera descriptors (for example, "iPhone photo," "35 mm lens feel," or "professional photography") should act as high-level style cues rather than literal optical specifications. Choose descriptors that fit the use case - professional photography might be appropriate for product or hero images, while candid phone shots demand casual capture language.

Instead, use grounded camera language:

- RAW iPhone photo
- smartphone back camera
- real candid frame grabbed from a phone video
- natural daylight
- practical indoor lighting
- low-light grain
- slight motion blur
- soft autofocus
- imperfect framing
- compression artifacts
- natural skin texture
- visible pores
- real shadows
- believable reflections
- ordinary background clutter
- no glamour retouching

## Decide the image type first

| Request looks like | Output type |
| --- | --- |
| Realistic family, caregiving, lifestyle, workplace, or social scene | controlled candid behavior first, then choose phone or documentary camera |
| Formal portrait, headshot, casting sheet, or character reference | intentionally posed portrait / consistency prompt |
| Social ad or local business visual with people | controlled candid marketing prompt unless posed presentation is explicitly needed |
| Product photo or website hero image | product / hero prompt |
| Poster or graphic with words | exact-text layout prompt |
| Infographic or explainer | infographic prompt |
| Website, app, dashboard, mobile screen | UI mockup prompt |
| Edit an uploaded image | edit prompt |
| Extend, upscale, fix proportions, change background | image repair prompt |
| First frame for image-to-video | video-ready first-frame prompt with one action already underway |
| Character or repeated subject | consistency prompt |

## The structure that works

Use this order:

```
Create [specific image type] for [use case].

Main subject:
[who or what is in the image, with specific visible details]

Candid moment / action:
[what is already happening, where each person is looking, how bodies overlap, what the hands are physically doing]

Scene:
[real location, time of day, background, ordinary details]

Composition:
[camera distance, crop, angle, subject placement, negative space]

Lighting:
[real light sources, direction, shadows, reflections]

Camera / realism:
[camera type, lens feel, focus, grain, motion blur, compression, imperfections]

Text / product / brand requirements:
[exact text, locked product details, logo instructions, what must stay accurate]

Constraints:
[what to avoid]

Output:
[aspect ratio]
```

## How to make images look real

Realism comes from physical detail, not hype words.

Good realism details:

- an ordinary action already in progress
- people reacting at slightly different times
- attention directed away from the camera
- believable hand-to-object and body-to-surface contact
- natural body overlap and unequal spacing
- clothing and hair responding to posture or movement
- what type of camera captured it
- whether it is front camera, back camera, or main camera
- time of day
- light direction
- real shadows
- imperfect framing
- background blur that makes sense
- motion blur when people are moving
- low-light grain when indoors or at night
- skin texture without retouching
- practical clutter in the background
- believable contact shadows under objects
- natural reflections on glass, metal, plastic, or wet pavement

Bad realism details:

- everyone facing the camera
- synchronized smiles or matching expressions
- people evenly spaced with no overlap
- hands displayed clearly but not doing anything
- a passive scene where everyone has already settled
- random mess or blur added without a physical cause
- 8k resolution
- perfect lighting
- ultra sharp everything
- flawless symmetry
- polished skin
- dramatic cinematic color grading when the image should feel candid
- overly clean backgrounds when the scene should feel real
- too many adjectives without camera or lighting direction

## RAW iPhone style

Use this when the image should feel real, casual, social, candid, or user-generated.

Strong phrases:

- RAW iPhone photo
- vertical 9:16
- smartphone back camera
- real candid phone photo
- real frame grabbed from a phone video
- not posed
- not professional
- not commercial
- imperfect framing
- slight motion blur
- soft autofocus
- natural HDR
- low-light grain
- compression artifacts in shadows
- realistic skin texture
- no glamour retouching

Example style line:

```
Camera / realism:
RAW iPhone photo, smartphone back camera, 26mm equivalent lens, natural HDR,
slight phone sharpening, imperfect framing, realistic skin texture, no glamour
retouching.
```

For low light:

```
Camera / realism:
RAW iPhone photo, smartphone back camera, low-light grain, soft autofocus,
slight motion blur, compression artifacts in the shadows, mixed practical
lighting, imperfect framing.
```

Avoid combining RAW iPhone style with studio or luxury-commercial language.

Do not say:

```
RAW iPhone photo, cinematic masterpiece, 8k, ultra sharp, perfect studio
lighting.
```

That creates a confused prompt.

Note: camera specifications such as focal length, sensor type, or lens feel should be treated as broad style cues rather than literal technical requirements. Choose a small number of coherent descriptors (e.g., "main back camera," "35 mm lens feel") and avoid mixing conflicting camera modes.

## Candid behavior and camera type are separate decisions

Choose behavior first:

1. **Controlled candid**, the default for realistic people. An ordinary action is underway, attention is divided, and the frame catches unequal timing.
2. **Directed but unposed**, useful when the image must remain clean and commercially readable. The subject has been given something real to do, but does not perform toward the camera.
3. **Intentionally posed**, use only for headshots, formal portraits, team photos, character sheets, product presentation, or when the user explicitly requests it.

Then choose capture type:

- **Candid phone frame:** casual, social, imperfect framing, phone HDR, mild compression, possible motion softness.
- **Candid documentary photograph:** deliberate photographer, cleaner anatomy and detail, natural lens behavior, but the people remain unperformed.
- **Controlled commercial candid:** readable campaign composition and usable negative space, while the people stay engaged in a real action rather than presenting to camera.

Do not use phone artifacts as a substitute for human realism. A tilted frame with posed people still looks staged. Conversely, a clean professional photograph can feel candid when behavior, timing, eyelines, touch, and physical interaction are believable.

## Building a candid moment

Write the moment around a small event, not a static arrangement. Strong event types include:

- an interruption
- one person helping another
- an object being passed, pulled, adjusted, folded, opened, or set down
- someone noticing something outside the frame
- one person reacting before another
- a task pausing midway
- a child shifting weight, reaching, turning, or losing interest
- fabric, hair, or an ordinary object responding to movement

Specify the physical state at the instant of capture. For example:

```
The toddler has just pulled one sock from the laundry pile. The mother has paused halfway through folding a shirt. One sleeve hangs between her knees while her free hand has started moving toward the toddler but has not reached the sock.
```

This is stronger than:

```
The mother and toddler fold laundry together naturally.
```

The first version gives the model timing, cause, contact, imbalance, and incomplete action. The second invites a polished staged interpretation.

### Controlled imperfection rule

Use imperfections that have a cause:

- motion softness belongs on the moving hand or object, not across the entire face
- a crop should result from spontaneous framing, not remove the main action
- mixed light should come from identifiable practical sources
- clutter should show recent use, not random decoration
- a tilted frame should be slight and plausible
- clothing wrinkles should follow posture and contact

Avoid stacking every imperfection into one prompt. Excessive blur, noise, tilt, clutter, occlusion, and low light can reduce realism by making the image incoherent.

## Documentary realism

Use this when the image should look like a real photograph made by an intentional observer rather than a phone recording. For people, documentary camera language must still be paired with candid behavior.

Good phrases:

- candid documentary-style photo
- an ordinary action already underway
- the photographer quietly observing rather than directing
- eye-level camera
- 35mm lens feel
- 50mm lens feel
- natural skin texture
- practical light only
- real background detail
- restrained depth of field
- soft natural shadows
- no glamour retouching
- slightly imperfect composition

Example:

```
Candid documentary-style photograph made by a quiet observer. The subjects remain
engaged in an ordinary task and do not acknowledge the camera. Eye-level camera,
35mm lens feel, practical daylight, natural skin texture, restrained background
blur, slight framing imperfections, no glamour retouching.
```

Do not rely on the phrase "documentary-style" by itself. A fully settled family looking toward the lens can still become a polished lifestyle photograph.

## Product realism

Use this for e-commerce images, website hero images, product ads, packaging, food, and object scenes.

Always include:

- preserve product shape
- preserve label placement
- preserve packaging proportions
- realistic contact shadows
- believable scale
- no warped labels
- no fake text
- no extra products
- no melted or inflated packaging
- no impossible reflections

For product cutouts:

```
Plain white or other solid opaque background, crisp product silhouette,
realistic edges, no halo, no fringing, preserve product geometry and label
placement.
```

(Transparent backgrounds are not supported by GPT Image 2. Use an opaque background here and remove it later in post-processing if transparency is required.)

For product scenes:

```
Place the product on a real surface with believable contact shadows, natural
reflections, realistic scale, and subtle background detail. Do not change the
label, packaging shape, or product proportions.
```

## Website hero images

Hero images need room for layout and cropping.

Always state:

- 16:9 unless another ratio is requested
- subject on one side
- clean negative space on the other
- no text inside the image unless requested
- important details away from the edges
- usable as a website banner
- safe crop for desktop and mobile

Example:

```
Create a realistic website hero image, 16:9. Place the main subject on the right
third of the image, with clean negative space on the left for a website headline
overlay. Keep important details away from the top, sides, and bottom so it crops
safely on desktop and mobile. No text inside the image.
```

## Exact text in images

When text must appear in the image, keep it short and controlled.

Rules:

- quote every exact phrase
- label each text block by role
- use fewer words
- request large readable text
- say "render verbatim"
- say "no extra words"
- say "no duplicate text"
- avoid tiny legal copy

Example:

```
Exact text:
Headline: "YOUR WEBSITE SHOULD WORK FOR YOU"
Subheadline: "Professional websites for local businesses"
Button text: "Start Today"

Render all text verbatim. No extra words, no duplicate text, no fake logo, no
misspellings.
```

If the text is long, recommend shortening it. A realistic image with wrong text is not usable.

## Image edits

For edits, separate the change from what must stay locked.

Use this structure:

```
Edit the uploaded image by [specific change].
Preserve [locked elements] exactly.
Match the new area to the original image's perspective, scale, lighting
direction, shadows, reflections, focus, grain, and camera quality.
Do not add extra objects, fake text, watermarks, warped shapes, or unrealistic
shadows.
```

Example:

```
Edit the uploaded image by replacing the background with a realistic open field
during late afternoon.
Preserve the product exactly, including its shape, label, color, proportions,
and placement.
Match the new background to the original camera angle, depth of field, lighting
direction, contact shadows, and image quality.
No extra products, no fake text, no watermark, no warped packaging.
```

## Background generation

When adding or replacing a background, do not just say "make a realistic background."

Specify:

- location type
- time of day
- depth of field
- horizon height
- light direction
- surface the subject sits on
- contact shadows
- how much attention the background should take

Good example:

```
Add a realistic softly blurred field background at golden hour. Keep the product
as the clear focus in the foreground. The horizon should sit low in the frame,
with warm sunlight coming from camera-left. Add a believable contact shadow
under the product. The background should support the product, not distract from
it.
```

## Fixing proportions

Use when the user says the image looks warped, too wide, too tall, or the product changed.

Prompt pattern:

```
Adjust the proportions of the uploaded image so the subject looks natural and
physically accurate.
Preserve the product identity, label, colors, textures, and arrangement exactly.
Correct any stretched, inflated, compressed, warped, or oversized elements. Keep
realistic scale, perspective, shadows, and camera angle.
Do not redesign the product, do not add new objects, and do not change the
background unless needed to support the corrected proportions.
```

## First frames for image-to-video

A good video first frame needs depth and one clear motion cue. For people, the frame should usually capture an action already underway rather than a neutral pose waiting for animation.

Include:

- foreground
- midground
- background
- clean subject silhouette
- one visible motion cue
- believable camera path
- no text unless needed
- no watermark

Good motion cues:

- a hand already reaching toward an object
- a shirt paused halfway through folding
- one person beginning to turn toward another
- a child shifting weight or pulling an object
- hair about to move
- fabric lifting
- dust in sunlight
- steam rising
- drink being raised
- papers mid-fall
- rain on pavement
- neon reflections shimmering
- confetti falling
- product slightly angled as if ready for a slow push-in

Template:

```
Create a video-ready first frame for an image-to-video clip.

Scene:
[subject and setting]

Composition:
[foreground, midground, background, clear subject silhouette, camera angle]

Motion cue:
[one visible motion element]

Lighting:
[realistic light source and direction]

Camera / realism:
[RAW iPhone, documentary, or cinematic camera details]

Constraints:
No text, no watermark, no distorted hands, no extra logos, no fake signage.

Output:
[aspect ratio]
```

## Negative instructions

Use negative instructions based on likely failure points. Short, targeted lists (around three to six items) are usually sufficient. Overly long catch-all blacklists can dilute the model's focus. Tailor the negatives to the specific scene rather than copying huge lists verbatim.

Useful negatives:

- no 8k
- no CGI look
- no plastic skin
- no airbrushed face
- no glamour retouching
- no stock-photo look
- no fake text
- no watermark
- no fake logo
- no readable fake signage
- no distorted hands
- no extra fingers
- no warped products
- no changed product labels
- no duplicate products
- no unrealistic shadows

## Aspect ratios

Always include an aspect ratio.

- 1:1: product square, e-commerce, social feed
- 4:5: Instagram feed portrait
- 2:3: poster, vertical editorial
- 9:16: Reels, Stories, TikTok, phone screenshot, UGC
- 16:9: website hero, video first frame, banner
- 4:3: editorial or traditional photo
- 3:4: vertical product or portrait

## Strong prompt templates

### Candid phone-video frame

```
Create a photorealistic frame grabbed from a real vertical phone video, 9:16.
It should feel casually captured, not professionally posed or performed.

Main subject:
[person details, clothing, age-appropriate proportions, identity relationships]

Candid moment / action:
[one ordinary action already underway; specify unequal reaction timing, eyelines,
body overlap, hand contact, and one incomplete movement]

Scene:
[real setting, time of day, signs of recent use, restrained ordinary clutter]

Composition:
[smartphone distance and height, slightly imperfect crop or tilt, readable action,
important faces still recognizable]

Lighting:
[practical light sources, direction, mixed color temperature if physically present,
realistic shadow retention]

Camera / realism:
Smartphone back camera, natural phone HDR, mild sharpening, restrained motion
softness only on the moving body part or object, slight autofocus softness,
compression in darker areas, realistic skin texture, no glamour retouching.

Constraints:
No coordinated posing, no synchronized smiles, no direct camera performance, no
random full-frame blur, no distorted hands, no plastic skin, no stock-photo look,
no fake text or watermark.

Output:
9:16
```

### Candid documentary photograph

```
Create a photorealistic candid documentary-style photograph for [use case].
The photographer is quietly observing an ordinary moment rather than directing it.

Main subject:
[subject details, clothing, natural physical traits, relationship between people]

Candid moment / action:
[one action already underway; specify what each person is doing, where attention is
directed, what the hands touch, how bodies overlap, and what remains incomplete]

Scene:
[location, time of day, ordinary background details and restrained evidence of use]

Composition:
Eye-level camera, [35mm or 50mm] lens feel, [close-up / medium shot / wide shot],
slightly unequal spacing, natural crop, readable action, no formal arrangement.

Lighting:
[real light source] coming from [direction], with realistic shadows, natural
contrast, and no forced even exposure across every face.

Camera / realism:
Natural skin texture, visible real-world texture, restrained background blur,
believable contact shadows, mild softness or grain where physically appropriate,
slight framing imperfections, no glamour retouching.

Constraints:
No direct camera performance, no synchronized expressions, no evenly spaced group
pose, no idle display hands, no plastic skin, no stock-photo look, no fake text,
no watermark.

Output:
[aspect ratio]
```

### Controlled commercial candid with people

```
Create a photorealistic controlled candid image for [campaign or business use].
The composition must be clean and usable, but the people should remain engaged in
a real action rather than presenting themselves to the camera.

Main subject:
[people, relationships, clothing, identity details]

Candid moment / action:
[one clear action already underway, divided attention, natural contact, one small
interruption or incomplete movement]

Scene:
[real location, ordinary details, culturally and geographically appropriate context]

Composition:
[aspect ratio], place the action on [side/third], preserve clean negative space for
layout, keep faces recognizable, allow slight overlap and unequal spacing.

Lighting:
[practical or motivated light source and direction], realistic shadows, no beauty
lighting, no artificial glow.

Camera / realism:
Professional documentary camera feel, restrained depth of field, natural skin and
fabric texture, believable contact shadows, slight timing imperfection, no glossy
lifestyle-ad finish.

Constraints:
No coordinated pose, no synchronized smiles, no direct camera performance unless
explicitly required, no plastic skin, no stock-photo look, no fake text or watermark.

Output:
[aspect ratio]
```

### Product image

```
Create a photorealistic product image for [use case].

Main product:
[product details]

Composition:
[placement, camera angle, crop, negative space]

Surface / background:
[white background, real table, field, kitchen counter, etc.]

Lighting:
[soft daylight / softbox / window light] from [direction], realistic contact
shadows, believable reflections.

Product accuracy:
Preserve the product shape, label placement, packaging proportions, colors, and
texture. Keep the product physically accurate and not warped.

Constraints:
No fake text, no extra products, no changed labels, no warped packaging, no
melted shapes, no watermark, no 8k, no CGI look.

Output:
[aspect ratio]
```

### Website hero image

```
Create a photorealistic website hero image for [business/use case], 16:9.

Main subject:
[subject details]

Composition:
Place the main subject on the [left/right] third of the image with clean
negative space on the opposite side for website headline overlay. Keep important
details away from the edges so the image crops well on desktop and mobile.

Scene:
[realistic setting]

Lighting:
[real light source and direction]

Camera / realism:
[smartphone/documentary/product camera details], realistic shadows, natural
texture, no overly polished stock-photo look.

Constraints:
No text inside the image, no watermark, no fake logos, no warped products, no
unrealistic shadows, no 8k.

Output:
16:9
```

### Image edit

```
Edit the uploaded image by [specific change].

Preserve [locked elements] exactly, including [product/logo/face/background/
camera angle/composition].

Match the edited area to the original image's lighting direction, perspective,
scale, contact shadows, color temperature, focus, grain, and camera quality.

Do not add text, logos, watermarks, extra products, distorted shapes,
unrealistic shadows, or a CGI look.

Output:
[aspect ratio]
```

## Human realism self-check

Before returning any prompt with people in a lifestyle scene, silently verify:

- Is one ordinary action already happening?
- Is attention directed toward the task, another person, or something outside frame?
- Do the people react at slightly different times?
- Are the hands physically occupied and making believable contact?
- Is there natural overlap or unequal spacing instead of a group arrangement?
- Does every imperfection have a physical cause?
- Is the main action still readable and commercially usable?
- Could the result still become a stock photo even with the camera language? If yes, rewrite the behavior and timing.
- Is the camera description coherent and separate from the candid behavior?

Do not force candidity onto formal portraits, character sheets, product cutouts, exact-text graphics, or source-preserving edits where the user has explicitly locked the pose.

## Final output behavior

Default response should be only the prompt in a clean code block.

When multiple versions are useful, separate them with short headers:

```
## RAW iPhone version
[prompt]

## Product hero version
[prompt]

## Video-ready first frame
[prompt]
```

Do not include long explanations unless the user asks.
