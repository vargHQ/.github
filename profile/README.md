<div align="center">
  <picture>
    <img alt="varg" src="https://raw.githubusercontent.com/vargHQ/.github/main/profile/banner-varg.svg" width="100%">
  </picture>

  <p><strong>AI-native video creation for agents and growth teams.</strong></p>

  <a href="https://x.com/vargaihq"><img src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white" /></a>
  <a href="https://docs.varg.ai"><img src="https://img.shields.io/badge/Docs-143D52?style=for-the-badge&logo=gitbook&logoColor=white" /></a>
</div>

---

### Quick Start

```bash
npm i vargai ai && vargai init
```

```tsx
import { Render, Clip, Image, Video, render } from "vargai/react";
import { varg } from "vargai/ai";

const video = (
  <Render width={720} height={720}>
    <Clip duration={3}>
      <Video
        prompt={{
          text: "robot waves hello, friendly gesture",
          images: [
            Image({
              prompt: "a friendly robot waving hello, cartoon style",
              model: varg.imageModel("flux-schnell"),
            }),
          ],
        }}
        model={varg.videoModel("wan-2.5")}
      />
    </Clip>
  </Render>
);

await render(video, { output: "hello.mp4" });
```

---

Installing skills
```bash
# 1. Install the varg skill
npx skills add vargHQ/skills

# 2. Set your API key (get one free at app.varg.ai)
export VARG_API_KEY=varg_live_xxx

# 3. Create your first video
claude "create a 10-second product video
  for white sneakers, 9:16, UGC style,
  with captions and background music"

# That's it. Agent writes JSX, picks models,
# renders in cloud, returns video URL.
```


---

### Core
- **[sdk](https://github.com/vargHQ/sdk)** — TypeScript SDK with JSX video composition, CLI, and AI provider integrations
- **[app](https://varg.ai/app)** — Claude Code for Video Ads. Web dashboard with auth, billing, and AI chat agent
- **[skills](https://github.com/vargHQ/skills)** - AI agent skills for video, image, speech & music generation. Works with Claude Code, Cursor, Windsurf, OpenCode, OpenClaw
- **[seedance 2.0 tutorial](https://github.com/vargHQ/seedance-sizzle-tutorial)** - Build a cinematic sizzle reel with Seedance 2.0 AI video generation + Remotion
- **[docs](https://docs.varg.ai)** — Documentation
- **[docs repo](https://github.com/vargHQ/docs)** -- Documentation repo

### Templates & Skills
- **[templates](https://github.com/vargHQ/templates)** — Remotion-based video templates (talking head, slideshow, product showcase)
- **[skills](https://github.com/vargHQ/skills)** — Agent Skills for AI media generation (Claude Code, Cursor, OpenCode)

---

**Questions?** [Discord](https://discord.com/invite/VAecJay7R9)

P.S. Best contributors get swag from varg.ai :)
