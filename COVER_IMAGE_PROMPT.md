# 📘 封面图生成指令

**用于:** gemini-image-simple 技能

---

## 主封面 (电子书封面)

**Prompt:**

```
Book cover design for "2026 AI Organization Guide"

Visual style: Swiss Modern Design
- Clean grid layout
- Bold sans-serif typography
- Minimalist aesthetic

Key elements:
- Title: "2026 AI 组织变现实战指南"
- Subtitle: "从 AI Agents 到 AI Organizations"
- Author: "KilroyContentBot"

Color scheme:
- Primary: Deep blue (#1a4d8f)
- Accent: Electric orange (#ff6b35)
- Background: Clean white or light gray

Imagery:
- Abstract representation of AI network/organization
- Geometric shapes connecting (nodes → network)
- NOT robot hands, NOT brains, NOT generic AI clichés

Mood: Professional, authoritative, forward-thinking
Aspect ratio: 3:4 (book cover)
```

---

## 章节配图 (第 1 章)

**Prompt:**

```
Infographic comparing AI Agents vs AI Organizations

Visual style: Clean business infographic
- Two-column comparison
- Icons and simple illustrations

Left side (AI Agents):
- Single person with assistant icon
- Label: "AI Agents = 超级助手"
- Characteristics: 单任务、人类发起、无决策权

Right side (AI Organizations):
- Team of connected AI nodes
- Label: "AI Organizations = AI 员工团队"
- Characteristics: 多 Agent 协作、自主决策、结果导向

Color scheme:
- AI Agents side: Cool blue
- AI Organizations side: Warm orange
- Clear visual contrast

Aspect ratio: 16:9 (slide/image)
```

---

## 销售页 Banner

**Prompt:**

```
Hero banner for ebook sales page

Visual style: Modern tech landing page
- Bold headline area
- Clean, professional

Text overlay area for:
- "2026 AI 组织变现实战指南"
- "早鸟价 $19.99"
- CTA button area

Background:
- Abstract AI network visualization
- Gradient from deep blue to electric purple
- Subtle geometric patterns

Mood: Premium, trustworthy, cutting-edge
Aspect ratio: 21:9 (wide banner)
```

---

**使用方式:**
```bash
# 调用 gemini-image-simple
gemini-image-simple: "[复制上方任一 Prompt]"
```

**输出:**
- 保存到 `products/images/` 目录
- 上传到 GitHub CDN (kilroy-cdn)
- 更新 Notion 产品页面
