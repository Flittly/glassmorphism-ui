# Glassmorphism UI &middot; 毛玻璃 UI

> A Claude Code skill that applies frosted glass design to any web frontend.  
> 一个 Claude Code Skill，为任意前端项目一键施加毛玻璃设计风格。

[![Skill](https://img.shields.io/badge/Claude%20Code-Skill-7C3AED)](https://docs.anthropic.com/en/docs/claude-code)

---

[English](#english) | [中文](#中文)

---

## English

### What is this?

**Glassmorphism UI** is a [Claude Code Skill](https://docs.anthropic.com/en/docs/claude-code/skills). When loaded, it teaches Claude how to apply frosted glass (glassmorphism) visual effects to your web application. Claude can restyle existing components, design new pages, or audit your UI for visual consistency — all following the glass design language defined in this skill.

### What it does

| Capability | Description |
|---|---|
| **Restyle existing UI** | Convert your current buttons, cards, nav bars to glass aesthetic |
| **Design new components** | Generate glass-styled cards, modals, forms from scratch |
| **Audit consistency** | Review your UI and fix elements that don't match the glass system |
| **Color-coded sections** | Apply distinct accent colors (blue/green/gold) per functional area |
| **Ant Design integration** | Override Ant Design default styles with glass effects |
| **Decorative backgrounds** | Add blurred color circles, shine animations, light beams |

### How Claude uses it

When you ask Claude things like:

> "Make this sidebar look like frosted glass"  
> "Style this button with a glass effect"  
> "Apply our glass design system to the whole page"  
> "Make this modal look like the editor sidebar"

Claude reads this skill and applies the exact CSS patterns — same `backdrop-filter` values, same shadow layers, same border-radius conventions — that were battle-tested on a production system.

### Install

```bash
# Clone into your skills directory
git clone <repo-url> ~/.claude/skills/glassmorphism-ui
```

Or copy the `glassmorphism-ui/` folder into your configured skills path.

### Skill Structure

```
glassmorphism-ui/
├── SKILL.md          # The skill instructions Claude reads
└── README.md         # This file
```

`SKILL.md` is the actual skill — it contains the CSS patterns, color palette, anti-patterns, and usage guidance that Claude follows when generating or modifying UI code.

### Real-world Basis

The CSS patterns in this skill were refined over 50+ design iterations on the **Yangtze River Bank Collapse Warning System (长江崩岸预警应用系统)** — a React + TypeScript + Mapbox GL JS + Ant Design scientific computing platform. Every blur value, shadow layer, and border radius was tuned against real map overlays, data tables, and form workflows.

### License

MIT

---

## 中文

### 这是什么？

**Glassmorphism UI（毛玻璃 UI）** 是一个 [Claude Code Skill](https://docs.anthropic.com/en/docs/claude-code/skills)。加载后，它会教会 Claude 如何为你的 Web 应用施加毛玻璃（glassmorphism）视觉风格。Claude 可以改造现有组件、设计新页面、或审查你的 UI 是否风格统一——全部遵循本 Skill 中定义的玻璃设计语言。

### 能做什么

| 能力 | 说明 |
|---|---|
| **改造现有 UI** | 将你的按钮、卡片、导航栏一键转换为毛玻璃风格 |
| **设计新组件** | 从零生成玻璃质感的卡片、弹窗、表单 |
| **风格审查** | 检查 UI 中不符合玻璃设计体系的元素并修复 |
| **按功能区着色** | 编辑器（金）、结果（蓝）、知识库（绿）分段配色 |
| **Ant Design 集成** | 覆盖 Ant Design 默认样式，施加玻璃效果 |
| **装饰性背景** | 添加模糊彩圆、光扫动画、光柱等氛围元素 |

### Claude 如何使用它

当你对 Claude 说类似这样的话：

> "帮我把这个侧边栏改成毛玻璃效果"  
> "把这个按钮做成玻璃风格"  
> "给整个页面应用我们的玻璃设计体系"  
> "让这个弹窗跟断面编辑器的侧边栏风格一致"

Claude 会读取这个 Skill，并严格应用其中定义的 CSS 模式——相同的 `backdrop-filter` 数值、相同的阴影层级、相同的圆角规范——这些模式都在一个生产系统中经过了反复打磨。

### 安装

```bash
# 克隆到你的 skills 目录
git clone <repo-url> ~/.claude/skills/glassmorphism-ui
```

或将 `glassmorphism-ui/` 文件夹复制到你配置的 skills 路径下。

### Skill 结构

```
glassmorphism-ui/
├── SKILL.md          # Skill 指令文件（Claude 真正读取的内容）
└── README.md         # 本文件
```

`SKILL.md` 是核心——它包含了 Claude 在生成或修改 UI 代码时所遵循的 CSS 模式、色板、避坑指南和使用规范。

### 实战来源

本 Skill 中的 CSS 模式在**长江崩岸监测预警应用系统**（React + TypeScript + Mapbox GL JS + Ant Design 科学计算平台）上历经 50+ 轮设计迭代打磨而成。每一个模糊值、每一层阴影、每一个圆角半径，都在真实的地图叠加、数据表格和表单交互中反复校准过。

### 许可证

MIT

---

<p align="center"><sub>Built on real design work. Made for Claude.</sub></p>
