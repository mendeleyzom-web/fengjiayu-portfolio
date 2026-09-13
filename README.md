# 个人网站 · 5 套 3D 风格

基于个人简介设计整理的 **5 套不同 3D 风格**个人网站，纯静态、零构建、零 CDN 依赖。

## 在线预览

| 页面 | 路径 |
|---|---|
| 🎠 作品集门户（3D 旋转展台，可浏览全部 5 套） | `/` |
| 🌊 深蓝·水产人（海洋生态风） | `/01-ocean/` |
| ⚡ 赛博·兴农（赛博朋克霓虹风） | `/02-cyber/` |
| 📖 素白·手记（极简编辑杂志风） | `/03-editorial/` |
| 🧱 黏土·元气（Claymorphism 柔和 3D） | `/04-clay/` |
| 🥇 黑金·雅（暗黑奢华风） | `/05-luxe/` |

## 目录结构

```
.
├── index.html              门户导航页（Three.js 3D 转台）
├── 01-ocean/               每站均为单文件 HTML（CSS/JS 全内联）
├── 02-cyber/
├── 03-editorial/
├── 04-clay/
│   ├── index.html          含「日常」板块（拍立得 + 灯箱）
│   ├── assets/daily/       日常照片
│   └── vendor/three.min.js 自包含依赖（可独立发布）
├── 05-luxe/
├── vendor/three.min.js     共享 Three.js r128（01/02/05 站引用）
├── .nojekyll               关闭 GitHub Pages 的 Jekyll 处理
└── README.md
```

## 技术要点

- **零构建**：直接打开 `index.html` 即可运行，无需 npm / 打包工具
- **离线可用**：Three.js 已内置在 `vendor/`，不依赖任何 CDN
- **单文件页面**：每个站点的 CSS 与 JS 全部内联，便于单独分发
- **无障碍**：统一处理 `prefers-reduced-motion`，关闭动画时内容仍完整可见
- **响应式**：覆盖桌面 / 平板 / 移动端三档断点

## 可访问性说明

站点遵循 `prefers-reduced-motion: reduce`：除禁用动画外，所有入场元素
（`.rv` / 标题词元）都会显式恢复 `opacity: 1`，避免动画被禁用后内容消失。

## 部署

仓库根目录即为站点根目录，开启 GitHub Pages（Source: `main` 分支 / `/` 根目录）即可。
`.nojekyll` 已就位，无需额外配置。
