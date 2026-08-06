---
name: micron-video-workflow
description: This skill should be used when the user wants to create a financial/equity research short video (e.g., a stock deep dive such as Micron Technology) using the Remotion video generation expert. It provides a reusable workflow covering stock selection, script outline, preview frames, video generation, and CapCut post-production.
agent_created: true
---

# Micron Video Workflow

## Overview

This skill packages a reproducible workflow for turning a stock or industry research topic into a polished short video. It is tuned for semiconductor/storage research content and uses the Remotion video generation expert to produce programmatic visuals.

## When to Use This Skill

Use this skill when the user asks to:

- Create a short financial research video (e.g., stock deep dive, industry trend, earnings recap).
- Generate a Remotion-based video from an outline or a set of slides.
- Produce preview frames before committing to full video rendering.
- Refine a video in CapCut and needs material sourcing or editing guidance.

## Workflow

Follow the phases below in order. Load the referenced prompt templates from `references/prompt_templates.md` and `references/capcut_materials.md` when the user reaches the corresponding phase.

### Phase 1: Stock / Industry Selection

1. Ask the user for the target stock/industry and the investment thesis angle.
2. Help gather credible data points using public sources and financial terminals (Wind, iFind, Bloomberg) where available.
3. Output a concise one-page brief with ticker, thesis, key catalysts, and risk factors.

### Phase 2: Video Outline

1. Confirm output specs with the user before writing the outline:
   - Target platform and aspect ratio (Douyin 9:16, Bilibili/YouTube 16:9, Xiaohongshu 3:4, etc.).
   - Target duration (recommended 60–120 seconds; each scene 3–8 seconds).
   - Visual style (dark tech gradient, light corporate, data-heavy, etc.).
   - Subtitle style and language.
   - Voiceover needs (TTS voice, real voice, or none).
2. Generate a scene-by-scene outline that includes:
   - Scene title and timestamp range.
   - Narration copy (short, spoken sentences).
   - On-screen text and key numbers.
   - Visual description (chart, icon, animation, stock footage).
   - Chapter cards (Intro, Closing, and any section dividers).

### Phase 3: Preview Frames

1. Before rendering any video, generate static preview frames for every chapter title card and key data scene.
2. Enforce visual consistency across frames: dark navy background, orange/cyan accent colors, large bold sans-serif Chinese typography, rounded cards, subtle gradients, and Lucide-style icons.
3. Required preview frames: Intro, Closing, and at least one preview for each major section.
4. Present the frames to the user and do not proceed to Phase 4 until the user approves the style.

### Phase 4: Remotion Video Generation

1. After preview approval, invoke the Remotion video generation expert workflow.
2. Build the video as a sequence of React/TypeScript components matching the approved previews.
3. Keep text readable (minimum 24 px on mobile), use bold sans-serif fonts, and maintain the agreed color system.
4. Export as MP4 H.264 by default; ask the user if another format is needed.

### Phase 5: CapCut Post-Production

1. Import the rendered MP4 into CapCut for trimming, pacing, and sound mixing.
2. For missing footage, refer to `references/capcut_materials.md` for:
   - Search keywords for stock footage and images.
   - AIGC prompts for still images and short video clips.
   - CapCut editing tricks (keyframes, animations, effects) to make static slides feel dynamic.

## Key Rules

- Never render a full video before preview frames are approved.
- Keep each scene between 3 and 8 seconds.
- Prioritize data accuracy; cite sources when possible.
- Use copyright-safe music and assets.
- Always ask about platform/aspect ratio and duration before starting the outline.

## References

- `references/prompt_templates.md` — Copy-paste prompts for each phase.
- `references/capcut_materials.md` — Material sourcing and CapCut editing guide.
