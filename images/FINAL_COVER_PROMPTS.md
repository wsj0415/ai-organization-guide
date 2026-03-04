# 📘 封面图生成提示词（完整版）

**用途:** AI 图像生成工具（gemini-image-simple, Midjourney, DALL-E 3, Stable Diffusion）

---

## 🎨 主封面（电子书封面）

### 英文 Prompt（推荐 - AI 理解更好）

```
Book cover design for "2026 AI Organization Guide"

Visual style: Swiss Modern Design
- Clean grid layout
- Bold sans-serif typography
- Minimalist aesthetic
- Professional and authoritative

Key elements:
- Main title: "2026 AI 组织变现实战指南"
- Subtitle: "从 AI Agents 到 AI Organizations"
- Author name: "KilroyContentBot"

Color scheme:
- Primary color: Deep blue #1a4d8f
- Accent color: Electric orange #ff6b35
- Background: Clean white or light gray gradient

Imagery:
- Abstract representation of AI network/organization
- Geometric shapes connecting (nodes transforming into network)
- Visual metaphor: individual dots → connected system
- Clean, modern, tech-forward

Mood: Professional, authoritative, forward-thinking, trustworthy

Technical:
- Aspect ratio: 3:4 (book cover standard)
- High resolution: 300 DPI
- Leave space for title text
- No text overlay (I will add text separately)

Avoid:
- ❌ Robot hands
- ❌ Human brains
- ❌ Generic AI clichés
- ❌ Stock photo style
- ❌ Cluttered composition
```

### 中文 Prompt（部分工具支持）

```
电子书封面设计，《2026 AI 组织变现实战指南》

视觉风格：瑞士现代设计
- 干净的网格布局
- 粗体无衬线字体
- 极简主义美学
- 专业权威感

主色调：
- 主色：深蓝色 #1a4d8f
- 强调色：电光橙 #ff6b35
- 背景：纯白或浅灰渐变

核心图像：
- AI 网络/组织的抽象表现
- 几何形状连接（节点→网络）
- 视觉隐喻：独立的点→连接的系统

情绪：专业、权威、前瞻性、可信赖

技术规格：
- 宽高比：3:4（电子书封面标准）
- 高分辨率：300 DPI
- 预留标题文字空间

避免：
- ❌ 机器人手
- ❌ 人脑
- ❌ 通用 AI 俗套图像
- ❌ 图库照片风格
- ❌ 杂乱构图
```

---

## 🖼️ 章节配图（第 1 章：AI Agents vs AI Organizations）

### Prompt

```
Infographic comparing AI Agents vs AI Organizations

Visual style: Clean business infographic
- Two-column comparison layout
- Simple icons and illustrations
- Professional and clear

Left side (AI Agents):
- Icon: Single person with assistant
- Label: "AI Agents = 超级助手"
- Characteristics: 单任务、人类发起、无决策权
- Color: Cool blue tones

Right side (AI Organizations):
- Icon: Network of connected AI nodes
- Label: "AI Organizations = AI 员工团队"
- Characteristics: 多 Agent 协作、自主决策、结果导向
- Color: Warm orange tones

Visual contrast:
- Clear separation between two sides
- Arrow or divider in the middle
- Easy to understand at a glance

Technical:
- Aspect ratio: 16:9 (slide/image)
- High contrast for readability
- Minimal text (I will add separately)

Avoid:
- ❌ Too much text
- ❌ Complex details
- ❌ Low contrast colors
```

---

## 🎯 销售页 Banner

### Prompt

```
Hero banner for ebook sales page

Visual style: Modern tech landing page
- Bold headline area
- Clean, professional design
- Conversion-optimized layout

Background:
- Abstract AI network visualization
- Gradient from deep blue (#1a4d8f) to electric purple (#6b3df9)
- Subtle geometric patterns (connected nodes)
- Depth and dimension

Foreground:
- Clear space for headline text
- CTA button area (right or center)
- Trust indicators area (optional)

Mood: Premium, trustworthy, cutting-edge, urgent

Technical:
- Aspect ratio: 21:9 (wide banner)
- High resolution for web
- Leave 60% empty space for text

Avoid:
- ❌ Busy patterns
- ❌ Low contrast
- ❌ Distracting elements
```

---

## 📱 社交媒体宣传图

### Prompt（小红书风格）

```
Social media promotional image for ebook launch

Platform: 小红书 (Little Red Book)
Style: Clean, modern, eye-catching

Key elements:
- Book cover mockup (3D render)
- "早鸟价 $19.99" badge (prominent)
- "限时优惠" ribbon
- 5-star rating stars

Background:
- Soft gradient (light to medium blue)
- Subtle geometric patterns
- Clean and uncluttered

Text areas (leave space for):
- "2026 AI 组织变现实战指南"
- "从 AI Agents 到 AI Organizations"
- "前 100 名专享"

Mood: Exciting, valuable, limited-time offer

Technical:
- Aspect ratio: 3:4 (小红书 optimal)
- High contrast for mobile viewing
- Text-safe zones

Avoid:
- ❌ Too much text
- ❌ Small details (mobile viewing)
- ❌ Low quality mockups
```

---

## 🛠️ 使用指南

### 使用 gemini-image-simple

```bash
# 调用技能
gemini-image-simple: "[复制上方任一 Prompt]"

# 输出
# - 保存到工作目录
# - 手动上传到 GitHub CDN
```

### 使用 Midjourney

```bash
# Discord 命令
/imagine prompt: [复制上方 Prompt] --ar 3:4 --v 6

# 参数说明
# --ar 3:4 : 宽高比
# --v 6 : 使用 v6 版本
```

### 使用 DALL-E 3

```bash
# ChatGPT Plus 或 API
# 直接粘贴 Prompt
# 选择尺寸：1024x1365 (3:4)
```

### 使用 Stable Diffusion

```bash
# WebUI
# Prompt: [复制上方 Prompt]
# Negative prompt: robot hands, brains, generic AI, stock photo, cluttered
# Steps: 30-40
# CFG: 7
# Model: SDXL 或 Juggernaut XL
```

---

## 📋 检查清单

生成后检查：

- [ ] 分辨率足够（至少 1000x1333 用于封面）
- [ ] 颜色符合品牌（深蓝 + 橙色）
- [ ] 无 AI 俗套图像（机器人手、人脑等）
- [ ] 预留文字空间
- [ ] 风格一致（瑞士现代设计）
- [ ] 无明显瑕疵

---

## 💾 文件命名规范

```
products/images/
├── cover_main.png              # 主封面
├── cover_chapter1.png          # 第 1 章配图
├── banner_sales.png            # 销售页 Banner
├── social_xiaohongshu.png      # 小红书宣传图
└── source/                     # 原始生成文件
    └── [日期]_[类型].png
```

---

## 🔗 上传到 GitHub CDN

生成后上传到：https://github.com/wsj0415/kilroy-cdn

```bash
# 上传脚本（参考）
cd /root/.openclaw/workspace-kilroy-content/products/images
./upload_to_github.sh cover_main.png screenshots/
```

获得 Raw 链接后更新：
- Notion 产品页面
- 销售页
- 社交媒体文案

---

**提示词准备就绪，等待 AI 图像生成工具调用！** 🎨
