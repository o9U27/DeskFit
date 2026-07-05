# DeskFit 网站自定义指南

## 快速开始

DeskFit 网站是一个**单一 HTML 文件**（`index.html`），所有内容都在其中。您可以用任何文本编辑器打开并修改。

### 推荐编辑工具
- **VS Code** — 免费、强大、支持实时预览
- **Sublime Text** — 轻量级、快速
- **Notepad++** — 简单易用
- 甚至 **记事本** 也可以！

---

## 📸 替换照片 / 图片

网站中有 **3 个主要的占位符图片区域**，都用绿色渐变背景和 SVG 图标表示。

### 1️⃣ **Hero 区块 - 主图（第 1 个图片）**

**位置：** 网站顶部，右侧大图

**当前代码（第 ~680-700 行）：**
```html
<div class="hero-img-placeholder" role="img" aria-label="Person exercising at their desk — hero image placeholder">
  <svg width="64" height="64" viewBox="0 0 64 64" fill="none" aria-hidden="true">
    <!-- SVG 代码 -->
  </svg>
  <strong style="font-size:0.95rem; color:#2D5A3D;">Hero Image Placeholder</strong>
  <span style="color:#5a8a6a; font-size:0.78rem;">Replace with a high-quality photo of<br>a professional exercising at their desk</span>
</div>
```

**替换方法：**

将上面的整个 `<div class="hero-img-placeholder">...</div>` 替换为：

```html
<img src="your-image-url.jpg" alt="Professional exercising at their desk" style="width: 100%; border-radius: 24px; box-shadow: 0 4px 24px rgba(45,90,61,0.15);">
```

**或者本地文件：**
```html
<img src="./images/hero-workout.jpg" alt="Professional exercising at their desk" style="width: 100%; border-radius: 24px; box-shadow: 0 4px 24px rgba(45,90,61,0.15);">
```

**图片建议：**
- 尺寸：至少 800×1000px（宽×高）
- 格式：JPG、PNG、WebP
- 内容：办公室工作者在做健身运动的照片
- 风格：专业、现代、充满活力

---

### 2️⃣ **Coach 区块 - 教练头像（第 2 个图片）**

**位置：** 网站中部，"Your Coach"部分左侧

**当前代码（第 ~1050-1070 行）：**
```html
<div class="coach-photo" role="img" aria-label="Coach photo placeholder — replace with real headshot">
  <svg width="56" height="56" viewBox="0 0 64 64" fill="none" aria-hidden="true">
    <!-- SVG 代码 -->
  </svg>
  <strong style="color:#2D5A3D; font-size:0.88rem;">Photo Placeholder</strong>
  <span style="color:#5a8a6a; font-size:0.72rem;">Replace with<br>real headshot</span>
</div>
```

**替换方法：**

将上面的整个 `<div class="coach-photo">...</div>` 替换为：

```html
<img src="./images/coach-sarah.jpg" alt="Dr. Sarah Chen, DeskFit Coach" style="width: 100%; border-radius: 20px; aspect-ratio: 3/4; object-fit: cover;">
```

**图片建议：**
- 尺寸：至少 400×550px（宽×高）
- 格式：JPG、PNG
- 内容：教练的专业头像照片
- 风格：友好、专业、可信任

---

### 3️⃣ **Client Transformations - Before/After 照片（第 3 和 4 个图片）**

**位置：** 网站中下部，"Client Transformations"部分

**当前代码（第 ~1200-1250 行）：**

有 **2 个客户故事**，每个都有 Before 和 After 两张照片。

**故事 1 - Before 照片：**
```html
<div class="transform-photo before" role="img" aria-label="Before photo placeholder">
  <svg width="32" height="32" viewBox="0 0 64 64" fill="none" aria-hidden="true">
    <!-- SVG 代码 -->
  </svg>
  <strong>BEFORE</strong>
  <span>Photo placeholder</span>
</div>
```

**替换方法：**

将 `<div class="transform-photo before">...</div>` 替换为：

```html
<img src="./images/client1-before.jpg" alt="Client transformation - before" style="width: 100%; aspect-ratio: 1; object-fit: cover;">
```

**故事 1 - After 照片：**
```html
<div class="transform-photo after" role="img" aria-label="After photo placeholder">
  <!-- 类似替换 -->
</div>
```

**替换为：**
```html
<img src="./images/client1-after.jpg" alt="Client transformation - after" style="width: 100%; aspect-ratio: 1; object-fit: cover;">
```

**重复此过程处理故事 2 的 Before/After 照片。**

**图片建议：**
- 尺寸：至少 400×400px（正方形）
- 格式：JPG、PNG
- 内容：真实的客户转变照片（或示例照片）
- 风格：真实、鼓舞人心

---

## 📝 修改文本内容

### 修改标题和描述

**Hero 标题（第 ~720 行）：**
```html
<h1 class="hero-title" id="hero-title">
  Stop Letting Your <span class="accent">Desk Job</span> Destroy Your Body
</h1>
```

直接编辑文本，保留 `<span class="accent">...</span>` 来保持绿色强调。

### 修改教练信息

**教练名字（第 ~1080 行）：**
```html
<h3 class="coach-name">Dr. Sarah Chen <span style="font-size:1rem; font-weight:400; color:#6b7280;">(Fictional Example)</span></h3>
```

**教练职位（第 ~1081 行）：**
```html
<p class="coach-title">Certified Corrective Exercise Specialist & Posture Coach</p>
```

**教练资质标签（第 ~1083-1088 行）：**
```html
<div class="coach-creds" aria-label="Credentials">
  <span class="cred-tag">NASM-CES</span>
  <span class="cred-tag">NSCA-CSCS</span>
  <span class="cred-tag">Postural Restoration Institute</span>
  <span class="cred-tag">8+ Years Experience</span>
</div>
```

**教练简介（第 ~1090-1099 行）：**
```html
<p class="coach-bio">
  After spending years treating office workers for chronic back pain...
</p>
```

### 修改定价

**Starter 价格（第 ~1160 行）：**
```html
<div class="pricing-price"><sup>HKD$</sup>299</div>
```

**Transform 价格（第 ~1185 行）：**
```html
<div class="pricing-price"><sup>HKD$</sup>499</div>
```

**Elite 价格（第 ~1210 行）：**
```html
<div class="pricing-price"><sup>HKD$</sup>799</div>
```

### 修改客户故事

**客户 1 名字和角色（第 ~1250 行）：**
```html
<h3 class="transform-name">Marcus T. <span style="font-size:0.82rem; font-weight:400; color:#6b7280;">(Fictional Example)</span></h3>
<p class="transform-role">Senior Software Engineer, Age 34</p>
```

**客户 1 成果标签（第 ~1254 行）：**
```html
<div class="transform-results">
  <span class="result-pill">Lost 8 kg in 3 months</span>
  <span class="result-pill">No more back pain</span>
  <span class="result-pill">+40% energy</span>
</div>
```

**客户 1 推荐语（第 ~1257 行）：**
```html
<blockquote class="transform-quote">
  "I'd had lower back pain for three years. After 6 weeks with DeskFit..."
</blockquote>
```

---

## 🎨 修改颜色

所有颜色都在 HTML 文件顶部的 CSS 变量中定义（第 ~15-28 行）：

```css
:root {
  --green:   #2D5A3D;           /* 森林绿 - 主色 */
  --green-light: #3a7350;       /* 浅绿 - 悬停效果 */
  --green-pale: #e8f0eb;        /* 淡绿 - 背景 */
  --bg:      #F5F3EE;           /* 米白 - 页面背景 */
  --text:    #2B2B2B;           /* 炭灰 - 文字 */
  --white:   #ffffff;           /* 白色 */
  --gray:    #6b7280;           /* 灰色 - 副文本 */
  --gray-light: #e5e7eb;        /* 浅灰 - 边框 */
}
```

**修改颜色：**
1. 找到要修改的颜色变量
2. 将十六进制值替换为新的颜色代码
3. 保存文件

**例如，改变主色为蓝色：**
```css
--green: #1e40af;  /* 改为蓝色 */
```

---

## 📂 文件结构建议

为了更好地组织文件，建议创建以下文件夹结构：

```
DeskFit/
├── index.html          （主文件）
├── images/
│   ├── hero-workout.jpg
│   ├── coach-sarah.jpg
│   ├── client1-before.jpg
│   ├── client1-after.jpg
│   ├── client2-before.jpg
│   └── client2-after.jpg
├── README.md
├── LICENSE
└── .gitignore
```

然后在 HTML 中引用图片：
```html
<img src="./images/hero-workout.jpg" alt="...">
```

---

## 🔧 本地预览修改

修改后，在本地预览您的更改：

```bash
# 进入项目目录
cd DeskFit

# 启动本地服务器
python3 -m http.server 8080

# 在浏览器中打开
# http://localhost:8080
```

---

## ✅ 修改检查清单

在发布前，请检查以下内容：

- [ ] 替换了所有占位符图片
- [ ] 更新了教练信息（名字、资质、简介）
- [ ] 更新了客户故事（名字、角色、成果、推荐语）
- [ ] 更新了媒体提及/推荐语
- [ ] 移除或更新了所有黄色警告标签（"Fictional Example"）
- [ ] 检查了所有链接（邮箱、社交媒体等）
- [ ] 在多个设备上测试了响应式设计
- [ ] 验证了所有图片都正确加载

---

## 🚀 发布到 GitHub

修改完成后，推送更改到 GitHub：

```bash
git add .
git commit -m "Update: Replace placeholder images and content"
git push origin master
```

---

## 📞 需要帮助？

如果您需要：
- **生成图片** — 我可以为您创建或编辑图片
- **代码修改** — 我可以帮您修改 HTML/CSS
- **部署到 Cloudflare** — 我可以帮您完成部署

只需告诉我！
