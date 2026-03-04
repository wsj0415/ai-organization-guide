# 🚀 快速部署方案

**问题:** Vercel token 未配置，无法使用 `vercel-deploy` 技能自动部署。

**解决方案:** 3 种替代方案

---

## 方案 A: GitHub Pages（推荐 - 无需配置）

### 步骤

1. **创建 GitHub 仓库**
   ```bash
   cd /root/.openclaw/workspace-kilroy-content/products
   git init
   git add slides/01_sales_preview.html
   git commit -m "Add sales preview slides"
   git branch -M main
   git remote add origin https://github.com/wsj0415/ai-organization-guide.git
   git push -u origin main
   ```

2. **启用 GitHub Pages**
   - 打开 https://github.com/wsj0415/ai-organization-guide/settings/pages
   - Source 选择 `main` 分支
   - 保存

3. **获得链接**
   - 约 1-2 分钟后生效
   - 链接格式：`https://wsj0415.github.io/ai-organization-guide/`

### 优点
- ✅ 无需 API token
- ✅ 完全免费
- ✅ 永久托管
- ✅ 支持自定义域名

---

## 方案 B: Netlify Drop（最简单 - 拖拽部署）

### 步骤

1. 打开 https://app.netlify.com/drop
2. 将 `slides/` 文件夹拖到上传区域
3. 获得即时预览链接

### 优点
- ✅ 无需注册（临时预览）
- ✅ 30 秒上线
- ✅ 自动生成 HTTPS 链接

### 缺点
- 临时链接（建议注册后绑定）

---

## 方案 C: 配置 Vercel Token（正式部署）

### 步骤

1. **获取 Token**
   - 打开 https://vercel.com/account/tokens
   - 创建新 token
   - 复制 token（以 `...` 开头）

2. **保存 Token**
   ```bash
   mkdir -p ~/.config/vercel
   echo "your_token_here" > ~/.config/vercel/token
   chmod 600 ~/.config/vercel/token
   ```

3. **部署**
   ```bash
   cd /root/.openclaw/workspace-kilroy-content/products
   vercel --prod
   ```

### 优点
- ✅ 正式生产环境
- ✅ 自动 HTTPS
- ✅ 支持自定义域名
- ✅ 自动 CI/CD

---

## 📊 方案对比

| 方案 | 难度 | 时间 | 推荐场景 |
|------|------|------|----------|
| GitHub Pages | ⭐⭐ | 5 分钟 | 长期托管 |
| Netlify Drop | ⭐ | 1 分钟 | 快速预览 |
| Vercel | ⭐⭐⭐ | 10 分钟 | 正式生产 |

---

## 🎯 我的建议

**立即:** 使用 **Netlify Drop** 快速预览（1 分钟上线）  
**今天:** 配置 **GitHub Pages** 长期托管（5 分钟）  
**本周:** 配置 **Vercel** 正式生产（需要 token）

---

## 📝 预览链接管理

部署后更新以下位置：

1. **Notion 产品页面**
   - 添加"销售链接"字段
   - 填入预览链接

2. **产品大纲文档**
   - 更新 `2026-03-04_AI_Organization_Guide.md`
   - 添加预览链接

3. **社交媒体**
   - 准备发布文案
   - 包含预览链接

---

**准备就绪，等待部署指令！** 🚀
