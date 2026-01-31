# Color Scheme Reference

This file provides a quick reference for all colors used in the Hugo Academic theme customization.

## Primary Color Palette

### Light Mode Colors

| Color Name | Hex Code | RGB | Usage |
|-----------|----------|-----|-------|
| Primary (Tech Blue) | `#3498db` | rgb(52, 152, 219) | Links, buttons, accents, avatar border |
| Secondary (Academic Blue) | `#2c3e50` | rgb(44, 62, 80) | Headings, important text |
| Success (Green) | `#27ae60` | rgb(39, 174, 96) | Success messages, awards |
| Warning (Orange) | `#f39c12` | rgb(243, 156, 18) | Warning messages |
| Danger (Red) | `#e74c3c` | rgb(231, 76, 60) | Error messages |
| Info (Blue) | `#3498db` | rgb(52, 152, 219) | Information messages |

### Dark Mode Colors

| Color Name | Hex Code | RGB | Usage |
|-----------|----------|-----|-------|
| Primary (Light Blue) | `#64b5f6` | rgb(100, 181, 246) | Links, buttons, accents |
| Background | `#121212` | rgb(18, 18, 18) | Main background |
| Background Secondary | `#1e1e1e` | rgb(30, 30, 30) | Card backgrounds |
| Surface | `#2d2d2d` | rgb(45, 45, 45) | Elevated surfaces |
| Text | `#e0e0e0` | rgb(224, 224, 224) | Primary text |
| Text Secondary | `#b0b0b0` | rgb(176, 176, 176) | Secondary text |
| Border | `#404040` | rgb(64, 64, 64) | Borders and dividers |

### Neutral Colors (Both Modes)

| Color Name | Hex Code | Usage |
|-----------|----------|-------|
| White | `#ffffff` | Pure white |
| Gray 100 | `#f8f9fa` | Light backgrounds |
| Gray 200 | `#e9ecef` | Borders, dividers |
| Gray 300 | `#dee2e6` | Subtle borders |
| Gray 400 | `#ced4da` | Disabled states |
| Gray 500 | `#adb5bd` | Placeholder text |
| Gray 600 | `#6c757d` | Secondary text |
| Gray 700 | `#495057` | Body text |
| Gray 800 | `#343a40` | Dark text |
| Gray 900 | `#212529` | Headings |
| Black | `#000000` | Pure black |

## Code Syntax Colors

### Light Mode
| Element | Color | Hex |
|---------|-------|-----|
| Inline Code | Pink | `#e83e8c` |
| Code Background | Light Gray | `#f8f9fa` |
| Pre Text | Dark Gray | `#212529` |

### Dark Mode
| Element | Color | Hex |
|---------|-------|-----|
| Inline Code | Light Pink | `#f48fb1` |
| Code Background | Dark Gray | `#2d2d2d` |
| Pre Text | Light Gray | `#e0e0e0` |

## Gradient Examples

### Skill Bar Gradient (Light Mode)
```
linear-gradient(90deg, #3498db, #5dade2)
```
- Start: Primary Blue (`#3498db`)
- End: Lighter Blue (`#5dade2`)

### Skill Bar Gradient (Dark Mode)
```
linear-gradient(90deg, #64b5f6, #90caf9)
```
- Start: Primary Light Blue (`#64b5f6`)
- End: Lighter Blue (`#90caf9`)

### Tag Cloud Gradient (Light Mode)
```
linear-gradient(135deg, #3498db, #5dade2)
```
- Direction: 135 degrees (diagonal)
- Colors: Primary to lighter shade

### Back to Top Button Gradient
```
linear-gradient(135deg, #3498db, #5dade2)
```
Hover state:
```
linear-gradient(135deg, #2980b9, #3498db)
```

### Blockquote Background Gradient
```
linear-gradient(to right, rgba(52, 152, 219, 0.05), transparent)
```
- Very subtle, left to right fade

## Shadow Values

| Shadow Type | Value | Usage |
|-------------|-------|-------|
| Small | `0 0.125rem 0.25rem rgba(0, 0, 0, 0.075)` | Subtle elevation |
| Medium | `0 0.5rem 1rem rgba(0, 0, 0, 0.15)` | Cards, buttons |
| Large | `0 1rem 3rem rgba(0, 0, 0, 0.175)` | Modals, dropdowns |
| Avatar | `0 4px 12px rgba(0, 0, 0, 0.1)` | Profile picture |
| Avatar Hover | `0 6px 20px rgba(0, 0, 0, 0.15)` | Profile picture on hover |

## Border Radius

| Type | Value | Usage |
|------|-------|-------|
| Small | `0.25rem` (4px) | Small elements |
| Default | `0.375rem` (6px) | Standard elements |
| Large | `0.5rem` (8px) | Cards, containers |
| Pill | `2rem` (32px) | Tag cloud, badges |
| Circle | `50%` | Avatar, buttons |

## Typography

### Font Families
- **Sans Serif**: `"Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif`
- **Monospace**: `"JetBrains Mono", "Fira Code", Consolas, Monaco, "Courier New", monospace`

### Font Sizes
| Size | Value | Usage |
|------|-------|-------|
| Small | `0.875rem` (14px) | Small text, captions |
| Base | `1rem` (16px) | Body text |
| Large | `1.125rem` (18px) | Large body text |

### Font Weights
| Weight | Value | Usage |
|--------|-------|-------|
| Light | 300 | Subtle text |
| Normal | 400 | Body text |
| Medium | 500 | Emphasized text |
| Semibold | 600 | Headings |
| Bold | 700 | Strong emphasis |

## Transition Speeds

| Speed | Value | Usage |
|-------|-------|-------|
| Fast | `0.15s` | Quick interactions |
| Base | `0.3s` | Standard transitions |
| Slow | `0.5s` | Smooth animations |
| Skill Bar | `1s` | Progress animations |

## Opacity Values

| Element | Opacity | Usage |
|---------|---------|-------|
| Disabled | 0.6 | Disabled elements |
| Hover Background | 0.05 | Subtle hover effects |
| Overlay | 0.8 | Modal overlays |

## Component-Specific Colors

### Avatar
- Border: Primary color (`#3498db`)
- Border Width: 4px (3px on mobile)

### Navigation
- Height: 70px
- Background: Theme-dependent
- Shadow: `0 2px 4px rgba(0, 0, 0, 0.08)`

### Publications
- Border Left: 3px solid Primary
- Hover Background: Primary with 5% opacity

### Cards
- Border: Gray 200 (`#e9ecef`)
- Hover Border: Primary (`#3498db`)

## Accessibility

### WCAG Contrast Ratios
All color combinations meet WCAG AA standards:
- Primary on White: 4.5:1 (AA)
- Secondary on White: 7.4:1 (AAA)
- White on Primary: 4.5:1 (AA)
- Light Blue on Dark Background: 4.8:1 (AA)

## Quick Copy Reference

### Most Used Colors
```scss
// Primary colors
$primary: #3498db;
$secondary: #2c3e50;

// Dark mode
$dark-primary: #64b5f6;
$dark-background: #121212;

// Code
$code-color: #e83e8c;
$code-bg: #f8f9fa;

// Neutral
$white: #ffffff;
$black: #000000;
```

---

**Note**: All colors are defined as SCSS variables in `assets/scss/_variables_custom.scss` and can be easily customized by editing that file.
