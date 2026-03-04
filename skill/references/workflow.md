# Complete Workflow Reference

## Phase 1: Research & Planning (30 minutes)

### 1.1 Trend Analysis (10 min)

**Tools:** `opennews`, `web_search`

**Process:**
1. Query AI/Crypto news with `opennews`
2. Filter by AI score >= 80
3. Search web for trending topics
4. Select top 5 high-value trends

**Output:**
- 5 trends with scores (80-92 range)
- Source links
- Pain point descriptions

**Example Trends:**
1. AI Organizations replacing AI Agents (92/100)
2. Investor shifts away from traditional SaaS (88/100)
3. Solo founders with AI outpacing teams (85/100)

### 1.2 Notion Database Setup (10 min)

**Tools:** `notion` skill, API key

**Databases to Create:**
1. **Trend Database** (`📈 趋势库`)
   - Fields: Title, Source, Score, Pain Point, URL, Date, Status, Tags
   - Purpose: Track market opportunities

2. **Product Database** (`📦 产品库`)
   - Fields: Title, Type, Status, Price, Sales URL, Production Date, Revenue
   - Purpose: Track product pipeline

3. **Publishing Database** (`📢 发布库`)
   - Fields: Title, Platform, Publish Date, Views, Engagement, Conversion
   - Purpose: Track distribution performance

**API Configuration:**
```bash
# Check API key
cat ~/.config/notion/api_key

# Test connection
curl -X POST "https://api.notion.com/v1/search" \
  -H "Authorization: Bearer $NOTION_KEY" \
  -H "Notion-Version: 2025-09-03"
```

### 1.3 Product Outline (10 min)

**Define:**
- Target audience (indie hackers, entrepreneurs, SMBs)
- Pricing strategy (early bird $19.99, regular $29.99)
- Chapter structure (12 chapters + appendix)
- Timeline (2-3 hours for first draft)

**Output:** `products/2026-03-04_AI_Organization_Guide.md`

---

## Phase 2: Content Production (2 hours)

### 2.1 Chapter Generation

**Rate:** ~10 minutes per chapter

**Chapter Structure:**
```markdown
# Chapter X: [Title]

> **Core Insight:** [One-sentence key takeaway]

## Introduction
- Problem statement
- Why this matters
- What you'll learn

## Main Content (3-5 sections)
- Section 1: Concept/Theory
- Section 2: Framework/Method
- Section 3: Case Study/Example
- Section 4: Implementation Steps

## Summary
- Key points (3-5 bullets)
- Action checklist
- Next chapter preview

**Word count:** ~4,000 words
**Reading time:** ~15 minutes
```

**Content Guidelines:**
- Use conversational tone (avoid AI flavor)
- Include real case studies with data
- Add actionable checklists
- Reference previous chapters
- Preview next chapters

### 2.2 Quality Audit

**Tool:** `content-auditor` skill

**Audit Criteria:**
1. **AI Flavor Detection** (8-10/10 target)
   - Avoid: "First/Second/Finally" structure
   - Avoid: Empty phrases ("In today's digital age")
   - Avoid: Overly formal tone

2. **Human Vitality** (8-10/10 target)
   - Personal expressions (colloquial, humor, emotion)
   - Unique perspectives (non-consensus views)
   - Real cases (specific names/companies/dates)

3. **Unique Insights** (8-10/10 target)
   - New frameworks/classifications
   - Actionable recommendations
   - Data/research support
   - Counter-intuitive conclusions

**Audit Process:**
```python
for chapter in chapters[1:]:  # Chapter 1 already audited
    score = audit_chapter(chapter)
    if score < 8:
        revise_chapter(chapter)
```

### 2.3 Progress Tracking

**File:** `products/PROGRESS.md`

**Update After Each Chapter:**
```markdown
### 2026-03-04 09:00 UTC
- [x] Generate Chapter X (4,500 words) ✅
- [ ] Audit Chapter X
- [ ] Update Notion

**Progress:** [████████░░░░░░░░░░░░] XX%
```

**Sync to Notion:**
- Update product page progress
- Add chapter completion blocks
- Update word count total

---

## Phase 3: Visual Design (30 minutes)

### 3.1 Sales Page Design

**Tool:** `ui-ux-pro-max` skill

**Design Pattern:** Pricing-Focused Landing

**Sections:**
1. **Navigation** - Fixed top, glass effect
2. **Hero** - Title + subtitle + CTA + stats card
3. **Social Proof** - Key metrics (trends, savings, ROI)
4. **Features** - 6 benefit cards
5. **Chapters** - 12 chapter grid
6. **Pricing** - Early bird card with 5 benefits
7. **FAQ** - 4 common questions
8. **CTA** - Final call-to-action
9. **Footer** - Copyright + links

**Style Guide:**
- Colors: Deep blue (#1a4d8f) + Electric orange (#ff6b35)
- Font: Inter (Google Fonts)
- Effects: Gradients, glass morphism, glow
- Animation: Float, pulse

**Tech Stack:**
- Tailwind CSS (CDN)
- Google Fonts (Inter)
- Inline CSS for custom effects

### 3.2 Preview Slides

**File:** `slides/01_sales_preview.html`

**6 Slides:**
1. Cover - Title + subtitle + author
2. Problem - 3 pain points
3. Solution - 4 key features
4. Benefits - 5 learning outcomes
5. Pricing - Early bird $19.99
6. Bonus - 3 exclusive bonuses

**Features:**
- Keyboard navigation (← → Space)
- Touch swipe (mobile)
- Progress bar
- Navigation dots

### 3.3 Cover Image Generation

**Tool:** `gemini-image-simple` skill

**Prompt:** (from `assets/cover-prompts.md`)
```
Book cover design for "2026 AI Organization Guide"
Swiss Modern Design, clean grid layout, bold typography
Deep blue #1a4d8f + Electric orange #ff6b35
Abstract AI network with geometric shapes
Professional, authoritative, 3:4 aspect ratio
```

**Upload:** GitHub CDN (`wsj0415/kilroy-cdn`)

---

## Phase 4: Deployment (15 minutes)

### 4.1 GitHub Repository

**Commands:**
```bash
cd /root/.openclaw/workspace-kilroy-content/products

# Initialize
git init
git add .
git commit -m "📚 Complete first draft: 12 chapters + appendix"

# Connect to remote
git remote add origin https://github.com/{user}/{repo}.git

# Push
git push -u origin main
```

**Token:** Use GitHub token from `~/.config/github/api_key`

### 4.2 GitHub Pages

**Setup:**
1. Go to repository settings
2. Enable Pages
3. Set source: `main` branch, root folder
4. Wait 1-2 minutes for build

**Verify:**
```bash
curl https://{user}.github.io/{repo}/ | head -20
```

**Fix 404:**
- Ensure `index.html` exists in root
- Re-push if needed

### 4.3 Notion Integration

**Update Product Page:**
- Add sales page link (bookmark block)
- Update progress to 100%
- Add completion celebration block

**Update Trend Database:**
- Link related trends to product
- Update status to "Converted to Product"

---

## Quality Checklist

### Content Quality
- [ ] 12 chapters + appendix complete
- [ ] 50,000+ total words
- [ ] All chapters audited (8-9/10 score)
- [ ] No AI flavor detected
- [ ] Actionable checklists included

### Design Quality
- [ ] Sales page responsive (mobile/tablet/desktop)
- [ ] Swiss Modern style applied
- [ ] All sections complete (Hero → Footer)
- [ ] CTA buttons functional
- [ ] Load time < 3 seconds

### Deployment Quality
- [ ] GitHub Pages live
- [ ] No 404 errors
- [ ] Notion databases synced
- [ ] All links working

---

## Timeline Summary

| Phase | Duration | Key Outputs |
|-------|----------|-------------|
| Research | 30 min | 5 trends, 3 databases, outline |
| Content | 2 hours | 12 chapters, 50K words |
| Design | 30 min | Sales page, slides, cover prompt |
| Deployment | 15 min | GitHub Pages, Notion sync |
| **Total** | **~3.5 hours** | **Complete digital product** |

---

## ROI Calculation

**Time Investment:** 3.5 hours
**Expected Revenue:** $19.99 × 100 customers = $1,999 (early bird)
**Hourly Rate:** $571/hour (if 100 sales)

**Cost Savings (for readers):**
- AI Customer Service: $282,000/year
- AI Content Organization: $336,000/year
- AI Data Analysis: $183,200/year
- **Total:** $801,200/year potential savings

**Value Proposition:** $19.99 investment → $800,000+ potential savings
