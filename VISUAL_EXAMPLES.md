# Visual Examples - Before & After

This document shows specific code examples of what has been customized.

## 🎨 Avatar / Profile Picture

### Before (Default)
```scss
.avatar {
  border-radius: 50%;
}
```

### After (Customized)
```scss
.avatar {
  border: 4px solid #3498db;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  
  &:hover {
    transform: scale(1.05);
    box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
  }
}
```

**Visual Changes:**
- Added colored border (Tech Blue)
- Added shadow for depth
- Hover effect: zooms to 105% size
- Smooth transitions

---

## 📚 Publication List Items

### Before (Default)
```scss
.pub-list-item {
  margin-bottom: 1rem;
}
```

### After (Customized)
```scss
.pub-list-item {
  border-left: 3px solid #3498db;
  padding-left: 1rem;
  margin-bottom: 1.5rem;
  transition: all 0.3s ease;
  border-radius: 0.25rem;
  
  &:hover {
    background-color: rgba(52, 152, 219, 0.05);
    transform: translateX(5px);
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  }
}
```

**Visual Changes:**
- Left accent border (3px primary color)
- Hover: slight background tint
- Hover: slides right 5px
- Added shadow on hover

---

## 🏷️ Tag Cloud

### Before (Default)
```scss
.tag-cloud a {
  display: inline-block;
  padding: 0.25rem 0.5rem;
  margin: 0.25rem;
}
```

### After (Customized)
```scss
.tag-cloud a {
  display: inline-block;
  margin: 0.25rem;
  padding: 0.4rem 0.8rem;
  background: linear-gradient(135deg, #3498db, #5dade2);
  color: #ffffff;
  border-radius: 2rem;
  transition: all 0.3s ease;
  font-size: 0.9rem;
  font-weight: 500;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  
  &:hover {
    transform: translateY(-2px) scale(1.05);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
    background: linear-gradient(135deg, #2980b9, #3498db);
    text-decoration: none;
  }
}
```

**Visual Changes:**
- Gradient background (blue to lighter blue)
- Pill-shaped design
- White text on colored background
- Hover: lifts up and scales
- Enhanced shadow on hover

---

## 📊 Skill Progress Bars

### Before (Default)
```scss
.progress-bar {
  background-color: #3498db;
}
```

### After (Customized)
```scss
.skill-bar {
  height: 10px;
  background-color: #e9ecef;
  border-radius: 0.375rem;
  overflow: hidden;
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  
  .skill-level {
    height: 100%;
    background: linear-gradient(90deg, #3498db, #5dade2);
    border-radius: 0.375rem;
    transition: width 1s ease-in-out;
    box-shadow: 0 2px 4px rgba(52, 152, 219, 0.3);
  }
}
```

**Visual Changes:**
- Gradient fill (left to right)
- Smooth 1-second animation
- Inset shadow on track
- Drop shadow on bar
- Rounded corners

---

## 🎴 Project Cards

### Before (Default)
```scss
.card {
  border: 1px solid #dee2e6;
}
```

### After (Customized)
```scss
.card {
  border: 1px solid #e9ecef;
  border-radius: 0.5rem;
  box-shadow: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.075);
  transition: all 0.3s ease;
  overflow: hidden;
  
  &:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.12);
    border-color: #3498db;
  }
  
  .card-img-top {
    transition: transform 0.3s ease;
  }
  
  &:hover .card-img-top {
    transform: scale(1.05);
  }
}
```

**Visual Changes:**
- Hover: lifts up 5px
- Hover: enhanced shadow
- Border changes to primary color
- Image zooms to 105% on hover
- Rounded corners

---

## 🔝 Back to Top Button

### New Feature (Added)
```scss
#back-to-top {
  position: fixed;
  bottom: 30px;
  right: 30px;
  z-index: 1000;
  display: none;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background: linear-gradient(135deg, #3498db, #5dade2);
  color: #ffffff;
  border: none;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
  cursor: pointer;
  transition: all 0.3s ease;
  
  &:hover {
    transform: translateY(-5px);
    box-shadow: 0 6px 20px rgba(0, 0, 0, 0.2);
    background: linear-gradient(135deg, #2980b9, #3498db);
  }
}
```

**Features:**
- Fixed position bottom-right
- Circular button (50px)
- Gradient background
- Appears after scrolling 300px
- Smooth scroll to top on click
- Hover: lifts up with enhanced shadow

---

## 📝 Code Blocks

### Before (Default)
```scss
pre {
  background: #f5f5f5;
}
```

### After (Customized)
```scss
pre {
  border-radius: 0.5rem;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  border: 1px solid #e9ecef;
  
  code {
    font-family: "JetBrains Mono", "Fira Code", monospace;
    font-size: 0.875em;
    line-height: 1.6;
  }
}

code {
  color: #e83e8c;
  background-color: #f8f9fa;
  padding: 0.2rem 0.4rem;
  border-radius: 0.25rem;
  font-family: "JetBrains Mono", monospace;
  font-size: 0.9em;
}
```

**Visual Changes:**
- JetBrains Mono font
- Rounded corners
- Shadow for depth
- Border for definition
- Pink color for inline code
- Light background

---

## 💬 Blockquotes

### Before (Default)
```scss
blockquote {
  border-left: 4px solid #ccc;
  padding-left: 1rem;
}
```

### After (Customized)
```scss
blockquote {
  border-left: 4px solid #3498db;
  padding-left: 1.5rem;
  margin: 1.5rem 0;
  font-style: italic;
  color: #495057;
  background: linear-gradient(to right, rgba(52, 152, 219, 0.05), transparent);
  padding: 1rem 1.5rem;
  border-radius: 0.375rem;
}
```

**Visual Changes:**
- Primary color border
- Gradient background (subtle)
- Italic text
- Rounded corners
- Better padding

---

## 🎯 Navigation Bar

### Before (Default)
```scss
.navbar {
  background: #fff;
}
```

### After (Customized)
```scss
.navbar {
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.08);
  backdrop-filter: blur(10px);
  transition: all 0.3s ease;
  
  .navbar-nav {
    .nav-link {
      font-weight: 500;
      transition: all 0.3s ease;
      position: relative;
      
      &::after {
        content: '';
        position: absolute;
        bottom: 0;
        left: 50%;
        transform: translateX(-50%);
        width: 0;
        height: 2px;
        background: #3498db;
        transition: width 0.3s ease;
      }
      
      &:hover::after,
      &.active::after {
        width: 80%;
      }
    }
  }
}
```

**Visual Changes:**
- Backdrop blur effect
- Shadow for elevation
- Underline animation on hover
- Smooth transitions
- Active link indicator

---

## 🌓 Dark Mode Example

### Light Mode
```scss
.avatar {
  border-color: #3498db;
}

.pub-list-item {
  border-left-color: #3498db;
}
```

### Dark Mode
```scss
[data-theme="dark"] {
  .avatar {
    border-color: #64b5f6;
    box-shadow: 0 4px 12px rgba(100, 181, 246, 0.2);
  }
  
  .pub-list-item {
    border-left-color: #64b5f6;
    background-color: #2d2d2d;
  }
  
  code {
    color: #f48fb1;
    background-color: #2d2d2d;
  }
}
```

**Visual Changes:**
- Lighter blue for better visibility (#64b5f6)
- Dark backgrounds (#2d2d2d)
- Adjusted shadows
- Light pink code color
- Consistent styling

---

## 📱 Mobile Responsive

### Mobile Adjustments
```scss
@media (max-width: 768px) {
  .avatar {
    border-width: 3px;  // Thinner on mobile
  }
  
  .portrait-title h2 {
    font-size: 1.5rem;  // Smaller heading
  }
  
  .navbar-brand img {
    height: 35px;  // Smaller logo
  }
  
  #back-to-top {
    width: 45px;
    height: 45px;
    bottom: 20px;
    right: 20px;
  }
  
  .pub-list-item {
    &:hover {
      transform: translateX(0);  // No slide on touch
    }
  }
}
```

**Mobile Optimizations:**
- Thinner borders
- Smaller text
- Reduced button sizes
- Disabled some hover effects
- Touch-friendly spacing

---

## 🎨 Color Variables

### All Colors Defined
```scss
// Primary colors
$primary: #3498db;
$secondary: #2c3e50;
$success: #27ae60;
$warning: #f39c12;
$danger: #e74c3c;

// Dark mode
$dark-primary: #64b5f6;
$dark-background: #121212;
$dark-surface: #2d2d2d;

// Code
$code-color: #e83e8c;
$code-bg: #f8f9fa;

// Shadows
$box-shadow-sm: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.075);
$box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15);
```

All these variables are used consistently throughout the stylesheet!

---

## ✨ Animation Examples

### Smooth Scrolling
```scss
html {
  scroll-behavior: smooth;
}
```

### Fade In Animation
```scss
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.home-section {
  animation: fadeIn 0.6s ease-out;
}
```

### Transition Speeds
```scss
$transition-fast: all 0.15s ease;
$transition-base: all 0.3s ease;
$transition-slow: all 0.5s ease;
```

---

**All these examples are working in your site!** 🎉

The customizations create a cohesive, professional look throughout the entire website.
