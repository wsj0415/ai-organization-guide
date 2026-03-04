# 🚀 销售页部署指南

**产品:** 《2026 AI 组织变现实战指南》  
**预览幻灯片:** `slides/01_sales_preview.html`  
**部署平台:** Vercel

---

## 📁 文件结构

```
products/
├── vercel.json                    # Vercel 配置
├── slides/
│   └── 01_sales_preview.html      # 预览幻灯片（已就绪）
├── images/                        # 封面图（待生成）
└── DEPLOYMENT.md                  # 本文件
```

---

## 🎯 部署步骤

### 方法 A: 使用 vercel-deploy 技能（推荐）

```bash
# 在 OpenClaw 中调用
vercel-deploy --prod
```

**预期输出:**
- 部署到生产环境
- 获得预览链接（如：`https://ai-organization-guide-2026.vercel.app`）
- 自动配置自定义域名（如有）

---

### 方法 B: 手动部署

```bash
# 1. 安装 Vercel CLI
npm i -g vercel

# 2. 登录 Vercel
vercel login

# 3. 部署
cd /root/.openclaw/workspace-kilroy-content/products
vercel --prod
```

---

## 🎨 幻灯片功能

### 已实现功能

✅ **6 页完整幻灯片**
1. 封面页 - 书名 + 副标题 + 作者
2. 痛点页 - 3 大困境
3. 解决方案页 - 4 大特征
4. 学习收获页 - 5 个要点
5. 定价页 - 早鸟价 $19.99
6. 福利页 - 3 大赠品

✅ **交互功能**
- 键盘导航（← → 空格）
- 触摸滑动（移动端）
- 导航圆点
- 进度条

✅ **设计风格**
- Swiss Modern 风格
- 深蓝 + 橙色配色
- 响应式设计
- 渐变背景

---

## 🖼️ 待完成：封面图生成

**使用技能:** `gemini-image-simple`

**Prompt 已准备:** `products/images/cover_prompt.txt`

**生成后用途:**
1. Notion 产品页面封面
2. 销售页 header
3. 社交媒体宣传图

---

## 📊 部署后验证

部署完成后，检查以下链接：

| 页面 | 链接 | 状态 |
|------|------|------|
| 预览幻灯片 | `https://[项目名].vercel.app/` | ⏳ 待部署 |
| 直接访问 | `https://[项目名].vercel.app/preview` | ⏳ 待部署 |

---

## 🔗 下一步

1. **[ ] 部署到 Vercel** - 使用 vercel-deploy 技能
2. **[ ] 生成封面图** - 使用 gemini-image-simple
3. **[ ] 更新 Notion 产品页** - 添加预览链接
4. **[ ] 准备发布文案** - 使用 social-media-agent

---

## 📝 销售页文案（草稿）

### 标题
**2026 AI 组织变现实战指南**

### 副标题
从 AI Agents 到 AI Organizations - 单人团队如何替代整个功能层

### 核心卖点
- 📘 80-100 页实战指南
- 🎯 12 章完整内容 + 3 个附录
- 💡 50+ 提示词模板
- 🔄 免费更新 1 年

### 早鸟优惠
- 原价：$29.99
- 早鸟价：$19.99（节省 33%）
- 前 100 名赠送 Discord 会员

### 适合人群
- 独立开发者想用 AI 构建被动收入
- 小企业主想降低人力成本
- 创业者寻找 AI 变现机会
- 自由职业者想提升效率 10 倍

---

**准备就绪，等待部署指令！** 🚀
