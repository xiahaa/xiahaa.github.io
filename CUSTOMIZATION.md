# Hugo Academic Theme Customization Guide

This document provides detailed information about the customizations applied to enhance the visual appearance and user experience of the Hugo Academic website.

## 📁 File Structure

```
xiahaa.github.io/
├── assets/
│   ├── media/
│   │   └── logo.svg                    # Organization logo
│   └── scss/
│       ├── _variables_custom.scss      # Custom SCSS variables
│       ├── custom.scss                 # Main custom stylesheet
│       └── components/                 # Component-specific styles (future)
├── config/
│   └── _default/
│       └── params.yaml                 # Updated with logo and features
└── layouts/
    └── partials/
        ├── custom_head.html            # Custom head additions (fonts, meta)
        └── custom_js.html              # Custom JavaScript (back-to-top, animations)
```

## 🎨 Color Scheme

### Light Mode
- **Primary Color**: `#3498db` (Tech Blue) - Used for accents, links, and interactive elements
- **Secondary Color**: `#2c3e50` (Academic Blue) - Used for headings and important text
- **Success**: `#27ae60` (Green)
- **Warning**: `#f39c12` (Orange)
- **Danger**: `#e74c3c` (Red)

### Dark Mode
- **Primary Color**: `#64b5f6` (Light Blue) - Better visibility in dark mode
- **Background**: `#121212` (Dark Gray)
- **Surface**: `#2d2d2d` (Medium Dark)
- **Text**: `#e0e0e0` (Light Gray)

## 🎯 Key Features Implemented

### 1. Branding
- **Logo**: Added organization logo (`assets/media/logo.svg`) to navigation bar
  - Height: 40px (35px on mobile)
  - Hover effect: Slight scale animation
  - Supports both light and dark modes

### 2. Typography
- **Primary Font**: Inter (loaded from Google Fonts)
- **Monospace Font**: JetBrains Mono for code blocks
- **Weights**: 300, 400, 500, 600, 700
- **Optimizations**: Anti-aliasing enabled for smoother text rendering

### 3. Component Beautification

#### Profile Card / About Section
```scss
.avatar {
  border: 4px solid $primary;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
  &:hover { transform: scale(1.05); }
}
```
- Colored border around avatar
- Shadow effect for depth
- Hover zoom animation

#### Publication List
```scss
.pub-list-item {
  border-left: 3px solid $primary;
  padding-left: 1rem;
  transition: all 0.3s ease;
  &:hover {
    background-color: rgba($primary, 0.05);
    transform: translateX(5px);
  }
}
```
- Left border accent
- Hover effects with background tint and slide animation
- Enhanced author and metadata styling

#### Project Cards
- Smooth hover elevation (translateY -5px)
- Image zoom on hover
- Border color changes to primary on hover
- Enhanced shadow effects

#### Skill Bars
```scss
.skill-bar {
  .skill-level {
    background: linear-gradient(90deg, $primary, lighten($primary, 15%));
    transition: width 1s ease-in-out;
  }
}
```
- Gradient fills for visual appeal
- Smooth width animation
- Shadow for depth

#### Tag Cloud
- Gradient background for tags
- Pill-shaped design (border-radius: 2rem)
- Hover scale and shadow effects
- Color variations for different tags

### 4. Navigation Enhancements

#### Navbar
- Backdrop blur effect for modern look
- Smooth underline animation on hover
- Fixed shadow for elevation
- Logo integration with hover effect

#### Back to Top Button
- Fixed position (bottom-right)
- Appears after scrolling 300px
- Smooth scroll to top
- Gradient background with hover effects
- Mobile-optimized size (45px on small screens)

### 5. Code Blocks & Syntax Highlighting

#### Features
- Rounded corners for modern appearance
- Border and shadow for definition
- Line numbers with separator
- Enhanced color schemes:
  - Light mode: `github-light`
  - Dark mode: `dracula`

#### Inline Code
- Pink accent color (`#e83e8c`)
- Light background
- Padding and border-radius for readability

### 6. Content Enhancements

#### Blockquotes
```scss
blockquote {
  border-left: 4px solid $primary;
  background: linear-gradient(to right, rgba($primary, 0.05), transparent);
  padding: 1rem 1.5rem;
  border-radius: $border-radius;
}
```
- Left accent border
- Gradient background
- Italic text with attribution support

#### Images
- Rounded corners on all images
- Hover zoom effect
- Shadow for depth
- Gallery items with enhanced styling

### 7. Interactive Features

#### Smooth Scrolling
- Enabled site-wide via `scroll-behavior: smooth`
- Custom JavaScript for anchor link scrolling
- Smooth animations on section reveal

#### Animations
- Fade-in animation for sections
- Hover transitions on interactive elements
- Page transition effects
- Scroll-based reveal animations

### 8. Responsive Design

#### Breakpoints
- Mobile: `< 768px`
- Tablet: `768px - 1024px`
- Desktop: `> 1024px`

#### Mobile Optimizations
- Reduced avatar border width
- Smaller logo size
- Adjusted button sizes
- Disabled some hover effects that don't work on touch

### 9. Dark Mode Support

All components have dark mode variants:
- Adjusted colors for better contrast
- Lighter primary color for visibility
- Dark surfaces and backgrounds
- Border and shadow adjustments

### 10. Accessibility

#### Features Implemented
- Keyboard focus styles with visible outlines
- ARIA labels on interactive elements
- Skip-to-main-content link
- Sufficient color contrast ratios
- Semantic HTML structure

### 11. Print Styles

Optimized for PDF export:
- Hidden navigation and interactive elements
- Proper page break handling
- Black text on white background
- URLs shown for external links
- Clean, professional layout

## ⚙️ Configuration

### params.yaml Updates

```yaml
# Logo
logo: media/logo.svg

# Features enabled
features:
  syntax_highlighter:
    enable: true
    theme_light: github-light
    theme_dark: dracula
  math:
    enable: true
  diagram:
    enable: true
```

## 🚀 Implementation Details

### CSS Variables
All styling is done using SCSS variables defined in `_variables_custom.scss`, making it easy to update colors and styles globally.

### Component Organization
- Base variables in `_variables_custom.scss`
- All component styles in `custom.scss`
- Future component-specific styles can go in `scss/components/`

### JavaScript Enhancements
Located in `layouts/partials/custom_js.html`:
- Back-to-top button logic
- Smooth scrolling for anchor links
- Intersection Observer for scroll animations
- Mobile-friendly touch handling

### Custom Head
Located in `layouts/partials/custom_head.html`:
- Google Fonts integration (Inter, JetBrains Mono)
- Font Awesome icons
- Meta tags for mobile optimization
- Preload directives for performance

## 📊 Performance Considerations

1. **Font Loading**: Using `preconnect` and `display=swap` for optimal font loading
2. **Asset Preloading**: Critical assets like logo are preloaded
3. **CSS Optimization**: Using CSS variables for better performance
4. **Animations**: Hardware-accelerated transforms for smooth animations
5. **Mobile First**: Responsive design ensures fast mobile experience

## 🎨 Customization Guide

### Changing Colors
Edit `assets/scss/_variables_custom.scss`:
```scss
$primary: #your-color !default;
$secondary: #your-color !default;
```

### Changing Fonts
Edit `layouts/partials/custom_head.html`:
```html
<link href="https://fonts.googleapis.com/css2?family=Your+Font&display=swap">
```

Then update `_variables_custom.scss`:
```scss
$font-family-sans-serif: "Your Font", sans-serif !default;
```

### Adding New Components
Create new files in `assets/scss/components/` and import them in `custom.scss`:
```scss
@import 'components/your-component';
```

## 🐛 Troubleshooting

### Styles Not Applying
1. Clear Hugo cache: `hugo --gc`
2. Rebuild site: `hugo`
3. Check browser cache

### Logo Not Showing
1. Verify file exists at `assets/media/logo.svg`
2. Check `params.yaml` has correct path
3. Ensure `show_logo: true` in navbar config

### Dark Mode Issues
1. Check that dark mode variables are defined in `_variables_custom.scss`
2. Verify `[data-theme="dark"]` selectors in `custom.scss`
3. Test theme toggle in browser

## 📝 Future Enhancements

Potential additions for further customization:
- [ ] Additional animation presets
- [ ] More color scheme variations
- [ ] Advanced typography options
- [ ] Custom widget styles
- [ ] Social media integration styling
- [ ] Enhanced mobile menu
- [ ] Reading progress bar
- [ ] Cookie consent banner styling

## 📖 References

- [Hugo Documentation](https://gohugo.io/documentation/)
- [Wowchemy Theme](https://wowchemy.com/docs/)
- [SCSS Guide](https://sass-lang.com/guide)
- [CSS Variables](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)

## 🤝 Contributing

To contribute to the styling:
1. Create new SCSS files in appropriate directories
2. Follow the existing naming conventions
3. Use SCSS variables for colors and spacing
4. Test in both light and dark modes
5. Ensure mobile responsiveness

## 📄 License

These customizations follow the same license as the Hugo Academic theme (MIT License).

---

**Last Updated**: 2026-01-31
**Version**: 1.0
**Author**: Automated Hugo Academic Customization
