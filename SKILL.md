---
name: glassmorphism-ui
description: |
  Apply frosted glass (glassmorphism) UI design to web applications. Use this skill whenever the user wants glass effects, frosted glass, liquid glass, blurred backgrounds, glass cards, glass buttons, modern translucent UI, or mentions making their interface look "premium", "modern", "frosted", or "glassy". Also use when designing navigation bars, sidebars, cards, buttons, modals, or form elements with a soft translucent aesthetic. This skill covers CSS patterns for React + CSS Modules + Ant Design, but the CSS principles apply universally.
---

# Glassmorphism UI Design System

Apply frosted glass effects using pure CSS. No JavaScript libraries needed.

## Core Principles

1. **Layered transparency** - stack multiple semi-transparent backgrounds
2. **Backdrop blur** - `backdrop-filter: blur()` with saturation boost
3. **Edge lighting** - white inset shadows for 3D glass feel  
4. **Radial light spots** - gradient ellipses mimicking light reflections
5. **Consistent rounding** - 10-22px border-radius everywhere
6. **Color-coded accents** - one accent per section/surface

## Core Glass Effect

```css
.glass {
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(16px) saturate(1.4) brightness(1.05);
  -webkit-backdrop-filter: blur(16px) saturate(1.4) brightness(1.05);
  border: 1px solid rgba(255, 255, 255, 0.3);
}
```

Always include the `-webkit-` vendor prefix. Adjust opacity based on how much of the background should show through:
- `0.6-0.75` for sidebars/panels that contain dense content  
- `0.15-0.25` for cards that should reveal more of what's behind
- `0.05-0.12` for very transparent decorative elements

## Glass Cards (Premium Liquid Effect)

This is the "hero" card style used for section containers. Combines radial light gradients with multi-layer shadows:

```css
.glass-card {
  background:
    radial-gradient(ellipse at 20% 0%, rgba(255,255,255,0.35) 0%, transparent 50%),
    radial-gradient(ellipse at 80% 100%, rgba(168, 210, 255, 0.2) 0%, transparent 50%),
    rgba(255, 255, 255, 0.12);
  backdrop-filter: blur(18px) saturate(1.6) brightness(1.05);
  -webkit-backdrop-filter: blur(18px) saturate(1.6) brightness(1.05);
  border: 1px solid rgba(255, 255, 255, 0.35);
  border-radius: 22px;
  padding: 16px;
  box-shadow:
    0 0 0 1px rgba(255, 255, 255, 0.15),
    0 4px 24px rgba(0, 0, 0, 0.08),
    0 1px 3px rgba(0, 0, 0, 0.04),
    inset 0 1px 0 rgba(255, 255, 255, 0.5),
    inset 0 -1px 0 rgba(0, 0, 0, 0.03);
}
```

**Key elements:**
- Two radial gradients: one white light at top-left (~20% 0%), one colored at bottom-right
- Five-layer shadow: outer ring + spread + tight + top inset white + bottom inset dark
- Higher blur (18px) and saturation (1.6) than regular glass

For colored accent cards, change the second radial gradient color:
- Blue: `rgba(168, 210, 255, 0.2)` or `rgba(59, 130, 246, 0.15)`
- Green: `rgba(16, 185, 129, 0.15)`
- Gold/yellow: `rgba(254, 243, 199, 0.2)`

## Glass Buttons

### Primary (colored)
```css
.glass-btn-primary {
  background: linear-gradient(135deg,
    rgba(255, 255, 255, 0.25) 0%,
    rgba(254, 243, 199, 0.2) 100%);
  backdrop-filter: blur(8px) saturate(1.4);
  -webkit-backdrop-filter: blur(8px) saturate(1.4);
  border: 1.5px solid rgba(251, 191, 36, 0.5);
  border-radius: 14px;
  color: #1e293b;
  padding: 8px 20px;
  font-weight: 500;
  cursor: pointer;
  box-shadow:
    0 0 10px rgba(251, 191, 36, 0.1),
    inset 0 1px 0 rgba(255, 255, 255, 0.5);
  transition: all 0.2s;
}
.glass-btn-primary:hover {
  border-color: rgba(251, 191, 36, 0.7);
  box-shadow:
    0 0 18px rgba(251, 191, 36, 0.18),
    inset 0 1px 0 rgba(255, 255, 255, 0.6);
}
```

### Outline/Secondary
```css
.glass-btn-outline {
  background: linear-gradient(135deg,
    rgba(255, 255, 255, 0.3) 0%,
    rgba(254, 243, 199, 0.15) 100%);
  backdrop-filter: blur(8px) saturate(1.4);
  -webkit-backdrop-filter: blur(8px) saturate(1.4);
  border: 1.5px solid rgba(251, 191, 36, 0.5);
  border-radius: 14px;
  color: #1e293b;
  padding: 8px 4px;
  font-size: 0.8rem;
  font-weight: 500;
  cursor: pointer;
  box-shadow:
    0 0 10px rgba(251, 191, 36, 0.08),
    inset 0 1px 0 rgba(255, 255, 255, 0.5);
  transition: all 0.2s;
}
```

### Circular Icon Buttons (32px)
```css
.glass-btn-circle {
  width: 30px; height: 30px;
  min-width: 30px; min-height: 30px;
  flex-shrink: 0; padding: 0;
  box-sizing: border-box;
  border: 1px solid rgba(0, 0, 0, 0.08);
  background: rgba(255, 255, 255, 0.5);
  backdrop-filter: blur(6px);
  -webkit-backdrop-filter: blur(6px);
  border-radius: 50%;
  display: flex; align-items: center; justify-content: center;
  box-shadow:
    0 2px 8px rgba(0, 0, 0, 0.06),
    inset 0 1px 0 rgba(255, 255, 255, 0.6);
  transition: all 0.15s;
}
```

### Styling Ant Design Buttons
To override Ant Design's default button styles while keeping glass look:
```css
.nav-right .ant-btn {
  background: rgba(255, 255, 255, 0.4) !important;
  backdrop-filter: blur(8px) !important;
  -webkit-backdrop-filter: blur(8px) !important;
  border: 1px solid rgba(0, 0, 0, 0.06) !important;
  border-radius: 14px !important;
  color: #475569 !important;
  font-size: 0.8rem !important;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.5) !important;
  transition: all 0.2s !important;
}
```
Use `!important` to override Ant Design's built-in specificity.

## Color Blur Circles (Background Decoration)

Add large blurred colored circles behind sidebar/panel content using pseudo-elements:

```css
.sidebar-panel {
  position: relative;
}
.sidebar-panel::before {
  content: '';
  position: absolute;
  width: 260px; height: 260px;
  top: 10%; right: -90px;
  background: radial-gradient(circle, rgba(59, 130, 246, 0.22) 0%, transparent 70%);
  border-radius: 50%;
  filter: blur(18px);
  pointer-events: none;
  z-index: 0;
}
.sidebar-panel::after {
  content: '';
  position: absolute;
  width: 200px; height: 200px;
  bottom: 25%; left: -70px;
  background: radial-gradient(circle, rgba(147, 197, 253, 0.18) 0%, transparent 70%);
  border-radius: 50%;
  filter: blur(20px);
  pointer-events: none;
  z-index: 0;
}
```

**Color mapping for different sections:**
- Editor/Blue: `rgba(59,130,246, 0.22)` + `rgba(147,197,253, 0.18)`
- Knowledge/Green: `rgba(16,185,129, 0.15)` + `rgba(52,211,153, 0.1)`
- Section/Gold: `rgba(251,191,36, 0.22)` + `rgba(253,230,138, 0.2)`

Adjust blur (18-32px) for desired softness. Lower = more visible circles.

## Navigation Tabs (Pill Style)

```css
.nav-tabs {
  display: flex;
  background: rgba(255, 255, 255, 0.2);
  backdrop-filter: blur(10px) saturate(1.3);
  -webkit-backdrop-filter: blur(10px) saturate(1.3);
  padding: 4px;
  border-radius: 14px;
  gap: 4px;
  border: 1px solid rgba(255, 255, 255, 0.3);
}
.nav-tab {
  padding: 8px 16px;
  border: 1.5px solid transparent;
  border-radius: 11px;
  font-size: 0.875rem;
  font-weight: 500;
  color: #64748b;
  cursor: pointer;
  transition: all 0.2s;
  outline: none;
}
```

**Active tab - color per section:**
```css
/* Editor/Gold */
.nav-tab:nth-child(1).active {
  background: linear-gradient(135deg, rgba(255,255,255,0.35) 0%, rgba(251,191,36,0.28) 100%);
  border-color: rgba(251, 191, 36, 0.5);
  color: #92400E;
}
/* Results/Blue */
.nav-tab:nth-child(2).active {
  background: linear-gradient(135deg, rgba(255,255,255,0.35) 0%, rgba(59,130,246,0.25) 100%);
  border-color: rgba(59, 130, 246, 0.45);
  color: #1E40AF;
}
/* Knowledge/Green */
.nav-tab:nth-child(3).active {
  background: linear-gradient(135deg, rgba(255,255,255,0.35) 0%, rgba(16,185,129,0.25) 100%);
  border-color: rgba(16, 185, 129, 0.45);
  color: #065F46;
}
```

Add a shine sweep animation on active tabs:
```css
.nav-tab {
  overflow: hidden;
}
.nav-tab.active::after {
  content: '';
  position: absolute;
  top: 0; left: -150%;
  width: 60%; height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.5), transparent);
  transform: skewX(-25deg);
  animation: tabShine 2s ease-in-out infinite;
}
@keyframes tabShine {
  0% { left: -150%; }
  50% { left: 120%; }
  100% { left: 120%; }
}
```

## Section Header Styling

```css
.section-title {
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 0.85rem;
  font-weight: 600;
  color: #475569;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  margin-bottom: 12px;
}
```

Always pair with an icon from lucide-react. Use 14px icons for section headers.

## Input & Select Styling

```css
input, select {
  box-sizing: border-box;
  width: 100%;
  padding: 8px 12px;
  border: 1px solid rgba(0, 0, 0, 0.08);
  border-radius: 10px;
  font-size: 0.875rem;
  outline: none;
  background: rgba(255, 255, 255, 0.4);
  transition: border-color 0.2s;
}
input:focus, select:focus {
  border-color: #3b82f6;
}
```

## Modal Styling

```css
.overlay {
  background-color: rgba(0, 0, 0, 0.3);
  backdrop-filter: blur(4px);
  -webkit-backdrop-filter: blur(4px);
}
.container {
  background:
    radial-gradient(ellipse at 20% 0%, rgba(255,255,255,0.4) 0%, transparent 50%),
    radial-gradient(ellipse at 80% 100%, rgba(254,243,199,0.15) 0%, transparent 50%),
    rgba(255, 255, 255, 0.8);
  backdrop-filter: blur(16px) saturate(1.5);
  -webkit-backdrop-filter: blur(16px) saturate(1.5);
  border-radius: 20px;
  border: 1px solid rgba(255, 255, 255, 0.35);
  padding: 24px;
  box-shadow:
    0 0 0 1px rgba(255,255,255,0.15),
    0 8px 32px rgba(0,0,0,0.12),
    inset 0 1px 0 rgba(255,255,255,0.4);
}
```

## Color Palette

```
--bg-page:      #eef1f6 (cool light gray for page background)
--glass-white:  rgba(255,255,255,0.6-0.75) (panel/sidebar backgrounds)
--glass-card:   rgba(255,255,255,0.08-0.15) (card item background)
--text-primary: #1e293b (dark slate for primary text)
--text-secondary: #64748b (medium gray for secondary text)
--accent-gold:  #fbbf24 (gold for editor/warning elements)
--accent-blue:  #3b82f6 (blue for results/data elements)
--accent-green: #10b981 (green for knowledge/success elements)
--accent-pink:  #f472b6 (pink for chat/messaging elements)
```

## Layout Patterns

**Glass page background:**
```css
body {
  background: #eef1f6;
}
```

**Glass navigation bar:**
```css
.main-nav {
  background: rgba(255, 255, 255, 0.7);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  border-bottom: 1px solid rgba(255, 255, 255, 0.4);
  box-shadow: 0 1px 12px rgba(0, 0, 0, 0.04);
}
```

## Anti-Patterns (Avoid)
- Don't nest `backdrop-filter` elements inside each other (causes rendering issues)
- Don't use full opacity white backgrounds (defeats the glass effect)
- Don't forget `pointer-events: none` on decorative pseudo-elements
- Don't apply glass to elements that need to be fully opaque (like dropdown options)
- Don't use `blur()` without `-webkit-` vendor prefix
- Don't make blur too high on small elements (reduces contrast)
- For Ant Design components, always use `!important` to override defaults

## Technology Notes
- Works with CSS Modules, plain CSS, and inline `style={{}}` patterns
- Compatible with React, Vue, Angular, or any framework
- For Ant Design overrides, target `.ant-btn`, `.ant-tag`, etc. with `!important`
- Use `nth-child()` or data attributes for per-element color variants
- Pseudo-elements (`::before`, `::after`) must be in CSS files, not inline styles
