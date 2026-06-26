# Glassmorphism UI &middot; 毛玻璃 UI

> A CSS-only glassmorphism design system for modern web applications.  
> 纯 CSS 毛玻璃设计体系，适用于现代 Web 应用。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

[English](#english) | [中文](#中文)

---

## English

### Overview

**Glassmorphism UI** is a curated collection of CSS patterns for building frosted glass (glassmorphism) user interfaces. It encompasses cards, buttons, navigation bars, modals, form controls, and decorative elements — all using pure CSS with `backdrop-filter`, radial gradients, and multi-layer box shadows. No JavaScript libraries, no runtime dependencies.

The patterns in this skill were refined across a real-world scientific computing platform (Yangtze River Bank Collapse Warning System), iterated over dozens of design reviews with a focus on visual polish, accessibility, and cross-browser compatibility.

### Features

- **Liquid Glass Cards** — Radial light gradients + five-layer shadows for premium 3D depth
- **Glass Buttons** — Primary, outline, and circular icon variants with colored glow
- **Navigation Tabs** — Color-coded pill-style tabs with shine sweep animation
- **Blur Circles** — Decorative background pseudo-elements for atmosphere
- **Modal Dialogs** — Blurred overlay + gradient glass container
- **Form Controls** — Rounded glass inputs and selects
- **Ant Design Overrides** — `!important` patterns for styling Ant Design components
- **Color Palette** — Curated gold/blue/green/pink accent system

### Quick Start

1. Copy the desired CSS class into your stylesheet.
2. Apply the class to your element.
3. Adjust opacity, blur, and colors to fit your design.

```css
/* Minimal glass effect */
.glass {
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(16px) saturate(1.4) brightness(1.05);
  -webkit-backdrop-filter: blur(16px) saturate(1.4) brightness(1.05);
  border: 1px solid rgba(255, 255, 255, 0.3);
}
```

### Browser Support

| Feature | Chrome | Safari | Firefox | Edge |
|---------|--------|--------|---------|------|
| `backdrop-filter` | ✅ 76+ | ✅ 9+ (with `-webkit-`) | ✅ 103+ | ✅ 79+ |
| `radial-gradient` | ✅ | ✅ | ✅ | ✅ |
| CSS pseudo-elements | ✅ | ✅ | ✅ | ✅ |

> Always include the `-webkit-` vendor prefix for Safari compatibility.

### Project Structure

```
glassmorphism-ui/
├── SKILL.md          # Full design system reference
└── README.md         # This file
```

### License

MIT

---

## 中文

### 概述

**Glassmorphism UI（毛玻璃 UI）** 是一套精选的 CSS 模式集合，用于构建毛玻璃质感的用户界面。涵盖卡片、按钮、导航栏、弹窗、表单控件和装饰元素——全部使用纯 CSS 实现，依赖 `backdrop-filter`、径向渐变和多层盒阴影，无需任何 JavaScript 库或运行时依赖。

这些模式在实际的科学计算平台（长江崩岸监测预警应用系统）中经过数十轮设计评审打磨而成，注重视觉品质、可访问性和跨浏览器兼容性。

### 特性

- **液体玻璃卡片** — 径向光斑渐变 + 五层阴影，呈现高级 3D 深度感
- **毛玻璃按钮** — 主按钮、轮廓按钮、圆形图标按钮，带彩色光晕
- **导航标签页** — 按功能区着色 + 光扫动画
- **彩色模糊圆** — 利用伪元素实现的背景氛围装饰
- **弹窗** — 模糊遮罩 + 渐变玻璃容器
- **表单控件** — 圆角毛玻璃输入框和选择器
- **Ant Design 覆盖** — 用 `!important` 美化 Ant Design 组件
- **色板体系** — 精选金/蓝/绿/粉四色点缀方案

### 快速开始

1. 将所需 CSS 类复制到你的样式表中。
2. 将类名应用到目标元素上。
3. 根据需要调整透明度、模糊度和颜色。

```css
/* 最简毛玻璃效果 */
.glass {
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(16px) saturate(1.4) brightness(1.05);
  -webkit-backdrop-filter: blur(16px) saturate(1.4) brightness(1.05);
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: 16px;
}
```

### 浏览器兼容性

| 特性 | Chrome | Safari | Firefox | Edge |
|------|--------|--------|---------|------|
| `backdrop-filter` | ✅ 76+ | ✅ 9+（需 `-webkit-`） | ✅ 103+ | ✅ 79+ |
| `radial-gradient` | ✅ | ✅ | ✅ | ✅ |
| CSS 伪元素 | ✅ | ✅ | ✅ | ✅ |

> 务必添加 `-webkit-` 前缀以兼容 Safari。

### 项目结构

```
glassmorphism-ui/
├── SKILL.md          # 完整设计体系参考文档
└── README.md         # 本文件
```

### 许可证

MIT

---

<p align="center"><sub>Crafted with ❤️ for modern web aesthetics</sub></p>
