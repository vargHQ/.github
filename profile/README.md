<div align="center">
  <picture>
    <img alt="varg" src="https://raw.githubusercontent.com/vargHQ/.github/main/profile/banner-varg.svg" width="100%">
  </picture>

  <p><strong>AI-native video creation for agents and growth teams.</strong></p>

  <a href="https://x.com/vaboratory"><img src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white" /></a>
  <a href="https://docs.varg.ai"><img src="https://img.shields.io/badge/Docs-143D52?style=for-the-badge&logo=gitbook&logoColor=white" /></a>
</div>

---

### Quick Start

```bash
npm i vargai && vargai init
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


---

### Core
- **[sdk](https://github.com/vargHQ/sdk)** — TypeScript SDK with JSX video composition, CLI, and AI provider integrations
- **[app](https://varg.ai/app)** — Claude Code for Video Ads. Web dashboard with auth, billing, and AI chat agent
- **[docs](https://docs.varg.ai)** — Documentation
- **[docs](https://github.com/vargHQ/docs)** -- Documentation Git

### Templates & Skills
- **[templates](https://github.com/vargHQ/templates)** — Remotion-based video templates (talking head, slideshow, product showcase)
- **[skills](https://github.com/vargHQ/skills)** — Agent Skills for AI media generation (Claude Code, Cursor, OpenCode)

---

**Questions?** [Discord](https://discord.com/invite/VAecJay7R9)

P.S. Best contributors get swag from varg.ai :)



**Questions?** [hello@varg.ai](mailto:hello@varg.ai)
