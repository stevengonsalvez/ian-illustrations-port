---
name: ian-xiaohei-illustrations
description: Generate Ian-style body illustrations for articles. Use when the user asks to create "weird"/"Blot"/"hand-drawn"/"body illustration"/"article illustration"/"illustration suggestions"/"shot list"/"de-title/edit-image" assets for an article, post, blog, Notion doc, workflow doc, methodology, process, structure, state, metaphor, or argument. Defaults to the Blot IP, pure-white hand-drawn line art, sparse red/orange/blue annotations, and a clean but wildly imaginative visual style.
user-invocable: true
---

# Ian Blot Weird Body Illustrations

## Core positioning

Design and generate 16:9 landscape body illustrations for articles. The goal is not commercial illustration, PPT infographics, or cute cartoons. It is to turn the article's key judgments, processes, structures, states, or metaphors into one clean, weird, creative, readable-but-not-instructional hand-drawn explanatory image.

The default visual IP is **Blot**: solid black, white dot eyes, thin legs, blank expression, earnestly doing something absurd yet coherent. Blot must take part in the core action of the image — never just stand beside it as decoration.

## Read these references first

Read on demand per task; do not stuff them all into context at once:

- `references/style-dna.md`: style DNA, color, text, taboos.
- `references/xiaohei-ip.md`: Blot's appearance, personality, action library, and taboos.
- `references/composition-patterns.md`: structure types, original-metaphor method, and the anti-copy rules.
- `references/prompt-template.md`: single-image generation prompt template.
- `references/qa-checklist.md`: post-generation checks and iteration rules.
- `assets/examples/`: low-frequency visual calibration only; not part of the default generation path. Do not copy these cases' compositions, objects, or labels.

## Workflow

### 1. Digest the article

First read the article, link, Notion page, Markdown file, or screenshot content the user gives you. Extract:

- What is the core argument
- Which paragraphs carry the cognitive turns
- Which content is well suited to being explained with an image
- Which spots are better left as text and need no image

Do not illustrate evenly. Prioritize "cognitive anchors" such as: the core judgment, two breakpoints, an input/output loop, a split, a before/after contrast, one-fish-many-uses, a handoff path, common pitfalls, a role's state change.

### 2. Propose the illustration strategy first

If the user only says "analyze how to illustrate this / think about where illustrations are needed," give a shot list first. For each image, spell out:

- Which paragraph it goes after
- The image's theme
- The core idea
- The structure type
- What Blot is doing in the image
- Suggested elements
- Suggested label words

Default to 4-8 images. For very short articles, 1-3; for long pieces, don't casually exceed 9. Enough is enough — don't turn the article into a picture book.

### 3. Single-image generation

If the user explicitly asks to "generate / output / make the image / generate it for me," don't stop to wait for confirmation; use the built-in `image_gen` to generate each one separately. Do not collage multiple images into one.

Each image conveys only one core structure. The prompt must include:

- 16:9 landscape article body illustration
- Pure white background
- Black hand-drawn line art
- A few red/orange/blue handwritten annotations
- Plenty of white space
- Blot as the core acting subject
- No PPT, commercial illustration, childish cuteness, complex architecture, or top-left type-title

Do not reproduce past cases. The examples only convey style density and how Blot participates; you cannot directly reuse existing compositions like "conveyor breakpoints / Blot pulling a lever / material fish / stamping toolbox / common-pitfalls path" unless the user explicitly asks to reproduce a specific image. Every time, reinvent a strange-yet-coherent metaphor from the current article.

### 4. Check and iterate

After generation, check `references/qa-checklist.md`. If any of the following occur, prefer regenerating or doing a local edit:

- Blot is just decoration
- The frame is too crowded
- Too much like a flowchart/PPT
- Too much text or serious typos
- A title like "common pitfalls/flowchart/system architecture" appears in the top-left
- The style is too cute, childish, or stiff
- The background is not a clean white base

### 5. Save and deliver

If the user is working inside a workspace, copy the final images to:

```text
assets/<article-slug>-illustrations/
```

Name them in order:

```text
01-topic-name.png
02-topic-name.png
```

Keep the original generated files; do not overwrite existing assets unless the user explicitly asks to replace them.

## Output style

Pre-generation strategy output should be short and precise. Post-generation delivery should include:

- How many images were generated
- What each image is for
- The save path
- Which images are most solid and which are optional

Don't write long explanations of style theory; let the images speak for themselves.
