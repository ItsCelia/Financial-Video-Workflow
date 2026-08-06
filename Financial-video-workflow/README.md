# micron-video-workflow

一套可复用的**财经/股票研究短视频制作 workflow**，把一只股票或一个行业的研究结论，快速做成 60–120 秒的短视频。

> 核心方法：先生成静态预览图确认视觉风格 → 再用 Remotion 渲染 → 最后在剪映做精简与素材补充。

---

## 这是什么？

它包含两部分，彼此独立：

1. **流程 + Prompt 模板**（任何 AI 助手都能用）
   `references/prompt_templates.md` 和 `references/capcut_materials.md` 是纯文本的工作流说明和可复制的 prompt。你不需要 WorkBuddy，只要把里面的 prompt 贴进 ChatGPT / Claude / 通义 / Kimi 等任意 AI 助手，就能按相同流程产出视频大纲、预览图、剪辑建议。

2. **WorkBuddy Skill**（WorkBuddy 用户一键触发）
   `SKILL.md` 让 WorkBuddy 在你说“帮我做一支存储行业短视频”时自动套用这套流程。不装 Skill、用别的 AI 也完全不影响上面第 1 点的使用。

**所以别人不用 WorkBuddy 也能直接用** —— 本质是一套写好的 prompt 和方法论。

---

## 目录结构

```text
micron-video-workflow/
├── SKILL.md                       # WorkBuddy Skill 定义（用户级/项目级安装）
├── README.md                     # 本文件
└── references/
    ├── prompt_templates.md       # 各阶段可直接复制的 prompt（A–E）
    └── capcut_materials.md       # 剪映素材关键词、AIGC 生图/生视频 prompt、动效技巧
```

---

## 五阶段流程

| 阶段 | 做什么 | 关键产出 |
|---|---|---|
| 1. 选股/选行业 | 确定标的与投资逻辑 | 一页研究 brief |
| 2. 视频大纲 | 写旁白、分镜、章节 | 场景表格（含时长/比例/风格/字幕/配音确认） |
| 3. Preview 预览图 | 生成章节标题图与关键数据页 | 静态预览图（必须含 Intro + Closing） |
| 4. Remotion 视频生成 | 把 approved 预览转化为可渲染视频 | MP4 + React/TS 项目 |
| 5. 剪映后期 | 精简、补素材、做动效 | 最终成片 |

---

## 用法 A：不用 WorkBuddy（通用 AI 助手）

1. 打开 `references/prompt_templates.md`。
2. 按阶段顺序，把 Prompt A → B → C → D → E 依次复制给任意 AI 助手。
3. 在 Phase 2 先回答时长/画面比例/风格/字幕/配音五个问题；Phase 3 等预览图确认后再继续。
4. 拿到 Remotion 渲染的 MP4 后，按 `references/capcut_materials.md` 在剪映补素材、做动效。

---

## 用法 B：WorkBuddy 用户

1. 解压本文件夹，放到：
   - 用户级：`~/.workbuddy/skills/micron-video-workflow/`
   - 项目级：`{项目目录}/.workbuddy/skills/micron-video-workflow/`
2. 在 WorkBuddy 中直接说：“帮我做一支美光/存储行业的短视频”，即可触发完整流程。

---

## 复用到其他股票/行业

保留流程和 prompt 模板不变，只替换 Phase 1 的标的数据即可。视觉关键词可按行业微调（如新能源用绿色系、消费用暖色系）。

---

## 许可

Prompt 模板与文档以 **CC BY 4.0** 发布，可自由复用、改写、商用，请保留署名。
