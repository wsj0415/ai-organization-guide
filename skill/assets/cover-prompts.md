# Cover Image Prompts

## Main Cover (Book Cover)

### English Prompt (Recommended)

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

### Chinese Prompt

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

## Chapter Images

### Chapter 1: AI Agents vs AI Organizations

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

## Sales Page Banner

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

## Social Media (Xiaohongshu)

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

## Usage Guide

### With gemini-image-simple

```bash
# Call the skill
gemini-image-simple: "[Copy any prompt from above]"

# Output
# - Save to working directory
# - Upload to GitHub CDN manually
```

### With Midjourney

```bash
# Discord command
/imagine prompt: [Copy prompt above] --ar 3:4 --v 6

# Parameters
# --ar 3:4 : Aspect ratio
# --v 6 : Use version 6
```

### With DALL-E 3

```bash
# ChatGPT Plus or API
# Paste prompt directly
# Select size: 1024x1365 (3:4)
```

### With Stable Diffusion

```bash
# WebUI
# Prompt: [Copy prompt above]
# Negative prompt: robot hands, brains, generic AI, stock photo, cluttered
# Steps: 30-40
# CFG: 7
# Model: SDXL or Juggernaut XL
```

---

## Checklist

After generation, verify:

- [ ] Resolution sufficient (at least 1000x1333 for cover)
- [ ] Colors match brand (deep blue + orange)
- [ ] No AI clichés (robot hands, brains, etc.)
- [ ] Space reserved for text
- [ ] Consistent style (Swiss Modern)
- [ ] No obvious defects

---

## File Naming Convention

```
images/
├── cover_main.png              # Main cover
├── cover_chapter1.png          # Chapter 1 image
├── banner_sales.png            # Sales page banner
├── social_xiaohongshu.png      # Xiaohongshu promo
└── source/                     # Original generated files
    └── [date]_[type].png
```

---

## Upload to GitHub CDN

After generation, upload to: https://github.com/wsj0415/kilroy-cdn

```bash
# Upload script (reference)
cd /root/.openclaw/workspace-kilroy-content/products/images
./upload_to_github.sh cover_main.png screenshots/
```

After obtaining Raw link, update:
- Notion product page
- Sales page
- Social media posts

---

**Prompts ready for AI image generation!** 🎨
