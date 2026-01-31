# Hugo Academic Theme Customization - Quick Start

## 🎨 What Has Been Added

This repository now includes comprehensive visual enhancements for the Hugo Academic theme, transforming it into a modern, professional academic website.

## ✨ Key Visual Improvements

### 1. **Custom Branding**
- Organization logo in navigation bar (`assets/media/logo.svg`)
- Professional color scheme (Tech Blue #3498db)
- Custom typography with Inter font

### 2. **Enhanced Components**

#### Profile Card
- Colored border around avatar (4px in primary color)
- Smooth hover zoom effect
- Shadow for depth
- Styled name and title with primary color accent

#### Publication List
- Left accent border (3px primary color)
- Hover effects: background tint + slide animation
- Enhanced author and metadata styling
- Better visual hierarchy

#### Project Cards
- Hover elevation effect (lifts up 5px)
- Image zoom on hover
- Border color changes to primary
- Enhanced shadows for depth

#### Skill Bars
- Beautiful gradient fills (primary to lighter shade)
- Smooth 1-second width animation
- Subtle shadow for 3D effect
- Professional appearance

#### Tag Cloud
- Gradient background pills
- Rounded corners (pill shape)
- Hover scale and shadow effects
- Modern, colorful design

### 3. **Navigation Enhancements**
- Backdrop blur effect for modern look
- Smooth underline animation on hover
- Logo with hover animation
- Mobile-optimized layout

### 4. **Interactive Features**
- **Back-to-top button**: Appears after scrolling 300px
- **Smooth scrolling**: Site-wide smooth anchor link scrolling
- **Page animations**: Fade-in effects on sections
- **Hover transitions**: All interactive elements have smooth transitions

### 5. **Content Styling**
- Enhanced code blocks with rounded corners and shadows
- Beautiful blockquotes with left border and gradient background
- Image hover zoom effects
- Improved gallery styling

### 6. **Dark Mode**
- Full dark mode support for all components
- Optimized colors for dark backgrounds
- Lighter primary color (#64b5f6) for better visibility
- Consistent styling across both themes

### 7. **Mobile Responsive**
- Mobile-first design approach
- Touch-friendly interactions
- Optimized button sizes
- Responsive typography

## 📁 Files Overview

```
New Customization Files:
├── assets/
│   ├── media/logo.svg                  # Your organization logo
│   └── scss/
│       ├── _variables_custom.scss      # Color and style variables
│       └── custom.scss                 # Component customizations
├── layouts/partials/
│   ├── custom_head.html                # Custom fonts and meta tags
│   └── custom_js.html                  # Interactive features
└── Documentation:
    ├── CUSTOMIZATION.md                # Full English guide
    ├── CUSTOMIZATION_CN.md             # Chinese guide (中文指南)
    ├── COLOR_REFERENCE.md              # Color palette reference
    ├── IMPLEMENTATION.md               # Implementation details
    └── QUICKSTART.md                   # This file
```

## 🚀 Usage

### The customizations are already active!

No action required - the Hugo Academic theme automatically includes:
1. `assets/scss/custom.scss` → Compiled into main CSS
2. `layouts/partials/custom_head.html` → Inserted in page `<head>`
3. `layouts/partials/custom_js.html` → Inserted before `</body>`

### Local Development

```bash
# Start local server
hugo server -D

# View at http://localhost:1313
```

### Production Build

```bash
# Build for production
hugo --minify

# Output in ./public directory
```

## 🎨 Quick Customization

### Change Primary Color

Edit `assets/scss/_variables_custom.scss`:
```scss
$primary: #your-color !default;           // Light mode
$dark-primary: #your-color !default;      // Dark mode
```

### Change Logo

1. Replace `assets/media/logo.svg` with your logo
2. Or update path in `config/_default/params.yaml`:
```yaml
logo: media/your-logo.png
```

### Change Font

Edit `layouts/partials/custom_head.html`:
```html
<link href="https://fonts.googleapis.com/css2?family=Your+Font&display=swap">
```

Then update `assets/scss/_variables_custom.scss`:
```scss
$font-family-sans-serif: "Your Font", sans-serif !default;
```

## 🎯 Feature Highlights

### Current Color Scheme

**Light Mode:**
- Primary: #3498db (Tech Blue)
- Secondary: #2c3e50 (Academic Blue)
- Success: #27ae60 (Green)

**Dark Mode:**
- Primary: #64b5f6 (Light Blue)
- Background: #121212 (Dark)
- Text: #e0e0e0 (Light Gray)

### Typography
- **Body Font**: Inter (Google Fonts)
- **Code Font**: JetBrains Mono
- **Weights**: 300, 400, 500, 600, 700

### Animations
- Smooth scrolling (0.3s ease)
- Hover transitions on all interactive elements
- Fade-in animations for sections
- Back-to-top button with smooth scroll

## 📚 Documentation

For detailed information, see:

1. **CUSTOMIZATION.md** - Complete English documentation
   - Full feature list
   - Customization guide
   - Troubleshooting

2. **CUSTOMIZATION_CN.md** - Chinese documentation (中文文档)
   - 完整功能列表
   - 自定义指南
   - 问题排查

3. **COLOR_REFERENCE.md** - Color palette guide
   - All colors with hex codes
   - Gradient examples
   - Shadow values

4. **IMPLEMENTATION.md** - Technical details
   - Architecture overview
   - Performance optimization
   - Best practices

## ✅ What's Working

- ✅ Custom branding with logo
- ✅ Professional color scheme
- ✅ Enhanced typography
- ✅ Beautiful component styling
- ✅ Smooth animations
- ✅ Dark mode support
- ✅ Mobile responsive
- ✅ Accessibility features
- ✅ Print optimization
- ✅ SEO optimization

## 🔧 Requirements

- **Hugo**: Extended version 0.119.0+
- **Go**: 1.21+
- **Internet**: For loading Google Fonts and Font Awesome

## 🐛 Troubleshooting

### Styles not applying?
```bash
hugo --gc  # Clear cache
hugo       # Rebuild
```

### Logo not showing?
Check:
1. File exists at `assets/media/logo.svg`
2. Path in `config/_default/params.yaml` is correct
3. `show_logo: true` in navbar settings

### Build fails?
Ensure you have Hugo Extended version:
```bash
hugo version
# Should show: hugo v0.119.0+extended
```

## 📖 Next Steps

1. **Customize colors** to match your brand
2. **Replace logo** with your organization's logo
3. **Adjust fonts** if desired
4. **Test locally** with `hugo server -D`
5. **Deploy** to GitHub Pages (automatic via workflow)

## 🎓 Tips

- All colors use SCSS variables for easy customization
- Test changes in both light and dark modes
- Check mobile responsiveness
- Validate accessibility with keyboard navigation
- Review print preview for PDF export

## 📞 Support

For questions about:
- **Customization**: See CUSTOMIZATION.md
- **Implementation**: See IMPLEMENTATION.md
- **Colors**: See COLOR_REFERENCE.md
- **Hugo**: See [Hugo Docs](https://gohugo.io/documentation/)
- **Wowchemy**: See [Wowchemy Docs](https://wowchemy.com/docs/)

## 📄 License

MIT License - Same as Hugo Academic Theme

---

**Ready to use!** Your site now has professional academic styling. 🎉

For more details, explore the documentation files listed above.
