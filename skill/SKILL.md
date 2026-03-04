---
name: ai-organization-guide-creator
description: "Complete workflow for creating AI Organization guides/ebooks from research to deployment. Use when creating digital products about AI automation including market research, content production, visual design, GitHub deployment, and Notion integration."
---

# AI Organization Guide Creator

Complete workflow for creating AI Organization guides/ebooks from research to deployment.

## Workflow Overview

```
Phase 1: Research & Planning (30 min)
├── Trend analysis (opennews/web_search)
├── Notion database setup
└── Product outline

Phase 2: Content Production (2 hours)
├── 12 chapters (50,000 words)
├── Appendix (tools/templates)
└── Quality audit

Phase 3: Visual Design (30 min)
├── Sales page (UI-UX Pro Max)
├── Preview slides
└── Cover image prompts

Phase 4: Deployment (15 min)
├── GitHub repository
├── GitHub Pages
└── Notion integration
```

## Quick Start

```bash
# 1. Initialize workspace
mkdir -p /root/.openclaw/workspace-kilroy-content/products
cd /root/.openclaw/workspace-kilroy-content/products

# 2. Run content generation
python3 scripts/generate_chapters.py

# 3. Deploy to GitHub
python3 scripts/deploy_github.py
```

## Core Workflow

### Step 1: Research & Planning

**1.1 Trend Analysis**
- Use `opennews` skill for AI/Crypto industry news
- Use `web_search` for market research
- Filter by AI score >= 80
- Save top 5 trends to Notion

**1.2 Notion Setup**
- Create 3 databases: Trends, Products, Publishing
- Use API key from `~/.config/notion/api_key`
- Sync trends to database

**1.3 Product Outline**
- Define target audience
- Set pricing strategy (early bird $19.99, regular $29.99)
- Create chapter outline (12 chapters + appendix)

### Step 2: Content Production

**2.1 Chapter Generation**
Generate 12 chapters following this structure:

| Chapter | Topic | Words |
|---------|-------|-------|
| 1 | AI Agents vs AI Organizations | 3,200 |
| 2 | 5 Characteristics of AI Organizations | 4,500 |
| 3 | Functions to Replace First | 4,200 |
| 4 | Tech Stack Selection | 4,800 |
| 5 | Building AI Customer Service | 5,500 |
| 6 | Building AI Content Organization | 5,800 |
| 7 | Building AI Data Analysis | 4,500 |
| 8 | AOaaS Business Model | 4,200 |
| 9 | Vertical Opportunities | 4,500 |
| 10 | From 0 to $10K/Month | 4,800 |
| 11 | Legal & Ethics | 4,500 |
| 12 | 2027-2030 Trends | 4,500 |
| Appendix | Tools/Templates/Calculators | 4,700 |

**2.2 Quality Audit**
- Use `content-auditor` skill for each chapter
- Check for "AI flavor" removal
- Ensure human vitality and unique insights
- Score target: 8-9/10

**2.3 Progress Tracking**
- Update `PROGRESS.md` after each chapter
- Track word count and completion percentage
- Sync to Notion product page

### Step 3: Visual Design

**3.1 Sales Page (UI-UX Pro Max)**
- Use `ui-ux-pro-max` skill for design patterns
- Apply Swiss Modern style
- Include: Hero, Features, Chapters, Pricing, FAQ, CTA
- Use Tailwind CSS for responsive design

**3.2 Preview Slides**
- Create 6-slide preview (Swiss Modern)
- Include: Cover, Problem, Solution, Benefits, Pricing, Bonus
- Add keyboard/touch navigation

**3.3 Cover Image**
- Use `gemini-image-simple` skill
- Prompt from `assets/cover-prompts.md`
- Upload to GitHub CDN

### Step 4: Deployment

**4.1 GitHub Setup**
```bash
cd products
git init
git add .
git commit -m "📚 Complete first draft"
git remote add origin https://github.com/{user}/{repo}.git
git push -u origin main
```

**4.2 GitHub Pages**
- Enable Pages in repository settings
- Set source to `main` branch
- Wait 1-2 minutes for build
- Verify at `https://{user}.github.io/{repo}/`

**4.3 Notion Integration**
- Update product page with sales link
- Add progress tracking blocks
- Sync trend database

## Decision Points

### Content Strategy
- **Vertical focus**: Choose specific industry (e-commerce, SaaS, finance)
- **Pricing**: Early bird (33% off) for first 100 customers
- **Format**: PDF + ePub + Markdown

### Design Patterns (UI-UX Pro Max)
- **Landing type**: Pricing-focused or Feature-focused
- **Color scheme**: Deep blue (#1a4d8f) + Electric orange (#ff6b35)
- **Style**: Swiss Modern with gradient backgrounds

### Deployment Options
- **GitHub Pages**: Free, fast setup (recommended)
- **Vercel**: More features, requires token
- **Netlify Drop**: Quick preview, temporary

## Output Structure

```
products/
├── drafts/              # 12 chapters + appendix
├── slides/              # Preview slides + sales page
├── images/              # Cover prompts + assets
├── PROGRESS.md          # Progress tracking
├── index.html           # Sales page (homepage)
└── vercel.json          # Deployment config
```

## Quality Standards

- **Word count**: 50,000+ words total
- **Chapter quality**: 8-9/10 audit score
- **Design**: Swiss Modern, responsive
- **Deployment**: GitHub Pages live in <5 minutes

## Tools Integration

| Tool | Purpose | Config |
|------|---------|--------|
| `opennews` | Trend research | AI score >= 80 |
| `content-auditor` | Quality audit | Score 8-9/10 |
| `gemini-image-simple` | Cover generation | Swiss Modern prompt |
| `notion` | Database sync | API key required |
| `ui-ux-pro-max` | Sales page design | Pricing-focused pattern |

## Common Issues

**Issue: GitHub Pages 404**
- Solution: Add `index.html` to root directory

**Issue: Notion API fails**
- Solution: Check API key at `~/.config/notion/api_key`

**Issue: Sales page not loading**
- Solution: Wait 1-2 minutes for GitHub Pages build

## References

- See `references/workflow.md` for detailed workflow
- See `references/chapter-templates.md` for chapter structures
- See `references/design-patterns.md` for UI-UX patterns
- See `assets/cover-prompts.md` for image generation prompts
