# CapCut 后期与素材获取指南

财经/半导体类短视频最容易卡在“没画面”。下面按素材类型给出可直接搜索的关键词、可投喂给 AIGC 的 prompt，以及让静态画面动起来的剪映技巧。

---

## 1. 剪映素材库搜索关键词

在剪映“素材库”里优先搜这些关键词（中英文结合）：

| 画面类型 | 中文关键词 | 英文关键词 |
|---|---|---|
| 科技/数据氛围 | 科技背景、数据流、芯片电路、蓝色科技 | technology background, data flow, circuit board, blue tech |
| 半导体制造 | 晶圆厂、光刻机、芯片、硅晶圆、电子显微镜 | semiconductor fab, wafer manufacturing, lithography machine, silicon wafer, clean room |
| 服务器/数据中心 | 数据中心、服务器机房、云计算、AI 服务器 | data center, server room, cloud computing, AI server |
| 金融/股市 | 股票走势、K线、交易所、金融数据 | stock chart, candlestick, stock exchange, financial data |
| 抽象概念 | 上升箭头、增长曲线、全球化、供应链 | growth arrow, upward trend, global network, supply chain |
| 品牌相关 | 美光、Micron、内存、DRAM、HBM、NAND | Micron Technology, memory chip, DRAM module, HBM stack, NAND flash |

**提示**：搜索结果若带水印或风格不统一，可用“色度抠图/蒙版”裁切，或改用 AIGC 生成。

---

## 2. AIGC 生图 / 生视频 Prompt

### 文生图（用于关键帧、背景、B-roll 封面）

```
深色科技风背景，深蓝黑色渐变，中央一束柔和的橙色光晕，微妙的电路板纹理，极简，高质感，适合作为半导体财经视频背景，16:9
```

```
一个抽象的三维 HBM 内存堆叠模型，金属质感，橙色和青色灯光，深色背景，科技感，8K，产品渲染风格
```

```
干净的半导体晶圆厂内部，自动化机械臂，蓝色安全灯，远处有穿着无尘服的工程师，电影感，浅景深
```

### 文生视频（3–5 秒动态 footage）

```
Camera slowly pans over a glowing circuit board, blue and orange lights pulse along the traces, dark background, cinematic, 4K, 5 seconds
```

```
Abstract data particles flow upward and converge into a bright light, representing AI computing power, dark navy background, orange and cyan accents, smooth motion, 5 seconds
```

```
Close-up of a silicon wafer rotating under clean room lighting, reflections shimmer, high-tech semiconductor manufacturing, slow motion, 4 seconds
```

**工具推荐**：可灵、Runway Gen-3、Pika、PixVerse、剪映“图文成片”中的 AI 生视频。

---

## 3. 让静态画面“动起来”的剪映技巧

### 关键帧动画（最常用）

- **放大/缩小**：给图片或文字添加“缩放”关键帧，制造推进感。适合数据卡片、K 线图。
- **平移**：给宽图或时间轴添加“位置”关键帧，从左向右缓慢移动。
- **透明度**：让文字/图标淡入淡出，避免画面生硬切换。

### 剪映内置动画

- **入场动画**：渐显、向上滑入、放大进入。用于每页标题和数字。
- **出场动画**：渐隐、向下滑出。用于切换到下一场景。
- **组合动画**：弹跳、故障风（适合科技风）、波浪。谨慎使用，避免花哨。

### 特效与转场

- **光效/粒子特效**：叠加在深色背景上，提升科技感；注意降低透明度，不要抢主体。
- **模糊/镜头光晕**：用于 Intro 和 Closing，增加电影感。
- **转场**：推荐“叠化”“轻微缩放”“方向模糊”，保持商务感；避免花哨的 3D 翻页。

### 图表动起来

- 把 Remotion 导出的数据页拆成多层（背景层、数字层、图标层）。
- 对数字层单独做“放大+透明度”关键帧，让数字逐个出现。
- 用“蒙版”让进度条/柱状图从左到右生长。

### 音效与节奏

- 在转场和数字出现处添加“嗖嗖声”“点击声”等 UI 音效。
- BGM 选择 120–130 BPM 的电子/科技风格，节奏点对应画面切换。
- 优先使用剪映内置可商用音乐或 Pixabay/YouTube Audio Library。

---

## 4. 常见错误与避坑

- **不要直接把整页 PPT 原样贴进视频超过 5 秒**——观众会走神。
- **不要让文字铺满屏幕**——保留 30% 以上留白。
- **不要混用多种字体/颜色**——严格遵循预览图定下的视觉系统。
- **不要忽略字幕安全区**——9:16 视频上下各留 10% 边距，避免被平台 UI 遮挡。
