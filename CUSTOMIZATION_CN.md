# Hugo Academic主题美化定制指南

本文档详细介绍了为提升Hugo Academic网站视觉外观和用户体验而应用的各项定制。

## 📁 文件结构

```
xiahaa.github.io/
├── assets/
│   ├── media/
│   │   └── logo.svg                    # 组织Logo
│   └── scss/
│       ├── _variables_custom.scss      # 自定义SCSS变量
│       ├── custom.scss                 # 主要自定义样式表
│       └── components/                 # 组件特定样式（预留）
├── config/
│   └── _default/
│       └── params.yaml                 # 已更新Logo和功能配置
└── layouts/
    └── partials/
        ├── custom_head.html            # 自定义头部（字体、元标签）
        └── custom_js.html              # 自定义JavaScript（返回顶部、动画）
```

## 🎨 配色方案

### 浅色模式
- **主色调**: `#3498db` (科技蓝) - 用于强调、链接和交互元素
- **次要色**: `#2c3e50` (学术蓝) - 用于标题和重要文本
- **成功色**: `#27ae60` (绿色)
- **警告色**: `#f39c12` (橙色)
- **危险色**: `#e74c3c` (红色)

### 深色模式
- **主色调**: `#64b5f6` (浅蓝色) - 在深色模式下有更好的可见性
- **背景色**: `#121212` (深灰色)
- **表面色**: `#2d2d2d` (中深灰色)
- **文本色**: `#e0e0e0` (浅灰色)

## 🎯 已实现的关键功能

### 1. 品牌形象

**Logo设置**
- Logo文件: `assets/media/logo.svg`
- 显示位置: 导航栏左侧
- 尺寸: 40px（移动端35px）
- 效果: 鼠标悬停时轻微缩放动画
- 支持深色/浅色模式

### 2. 字体排版

**字体选择**
- **主字体**: Inter（从Google Fonts加载）
- **等宽字体**: JetBrains Mono（用于代码块）
- **字重**: 300, 400, 500, 600, 700
- **优化**: 启用抗锯齿以获得更平滑的文本渲染

### 3. 组件美化

#### 个人资料卡片
```scss
.avatar {
  border: 4px solid $primary;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
  &:hover { transform: scale(1.05); }
}
```
特点：
- 头像周围的彩色边框
- 阴影效果增加深度
- 鼠标悬停时的缩放动画

#### 出版物列表
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
特点：
- 左侧强调边框
- 鼠标悬停时背景着色和滑动动画
- 增强的作者和元数据样式

#### 项目卡片
- 平滑的悬停上升效果（translateY -5px）
- 图片在悬停时放大
- 悬停时边框颜色变为主色调
- 增强的阴影效果

#### 技能进度条
```scss
.skill-bar {
  .skill-level {
    background: linear-gradient(90deg, $primary, lighten($primary, 15%));
    transition: width 1s ease-in-out;
  }
}
```
特点：
- 渐变填充视觉效果
- 平滑的宽度动画
- 阴影增加深度感

#### 标签云
- 标签的渐变背景
- 胶囊形状设计（border-radius: 2rem）
- 悬停时的缩放和阴影效果
- 不同标签的颜色变化

### 4. 导航增强

#### 导航栏
- 背景模糊效果，呈现现代感
- 悬停时平滑的下划线动画
- 固定阴影增加层次感
- Logo集成及悬停效果

#### 返回顶部按钮
- 固定位置（右下角）
- 滚动超过300px后显示
- 平滑滚动到顶部
- 渐变背景和悬停效果
- 移动端优化尺寸（小屏幕上45px）

### 5. 代码块和语法高亮

#### 功能特性
- 圆角现代外观
- 边框和阴影增加定义感
- 带分隔符的行号
- 增强的配色方案：
  - 浅色模式: `github-light`
  - 深色模式: `dracula`

#### 行内代码
- 粉色强调色（`#e83e8c`）
- 浅色背景
- 内边距和圆角提高可读性

### 6. 内容增强

#### 引用块
```scss
blockquote {
  border-left: 4px solid $primary;
  background: linear-gradient(to right, rgba($primary, 0.05), transparent);
  padding: 1rem 1.5rem;
  border-radius: $border-radius;
}
```
特点：
- 左侧强调边框
- 渐变背景
- 斜体文本，支持署名

#### 图片
- 所有图片圆角处理
- 悬停时的缩放效果
- 阴影增加深度感
- 画廊项目增强样式

### 7. 交互功能

#### 平滑滚动
- 通过 `scroll-behavior: smooth` 在整个网站启用
- 锚点链接的自定义JavaScript滚动
- 区块显示时的平滑动画

#### 动画效果
- 区块的淡入动画
- 交互元素的悬停过渡
- 页面过渡效果
- 基于滚动的显示动画

### 8. 响应式设计

#### 断点
- 移动端: `< 768px`
- 平板: `768px - 1024px`
- 桌面: `> 1024px`

#### 移动端优化
- 减小头像边框宽度
- 较小的Logo尺寸
- 调整按钮大小
- 禁用触摸设备上不适用的悬停效果

### 9. 深色模式支持

所有组件都有深色模式变体：
- 调整颜色以获得更好的对比度
- 较浅的主色调以提高可见性
- 深色表面和背景
- 边框和阴影调整

### 10. 可访问性

#### 已实现的功能
- 带可见轮廓的键盘焦点样式
- 交互元素上的ARIA标签
- 跳到主内容链接
- 足够的颜色对比度
- 语义化HTML结构

### 11. 打印样式

为PDF导出优化：
- 隐藏导航和交互元素
- 正确的分页处理
- 黑色文本白色背景
- 显示外部链接的URL
- 清晰、专业的布局

## ⚙️ 配置说明

### params.yaml 更新

```yaml
# Logo配置
logo: media/logo.svg

# 启用的功能
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

## 🚀 实现细节

### CSS变量
所有样式都使用 `_variables_custom.scss` 中定义的SCSS变量，便于全局更新颜色和样式。

### 组件组织
- `_variables_custom.scss` 中的基础变量
- `custom.scss` 中的所有组件样式
- 未来的组件特定样式可以放在 `scss/components/` 中

### JavaScript增强
位于 `layouts/partials/custom_js.html`：
- 返回顶部按钮逻辑
- 锚点链接的平滑滚动
- 滚动动画的交叉观察器
- 移动端友好的触摸处理

### 自定义头部
位于 `layouts/partials/custom_head.html`：
- Google Fonts集成（Inter, JetBrains Mono）
- Font Awesome图标
- 移动端优化的元标签
- 性能优化的预加载指令

## 🎨 自定义指南

### 更改颜色
编辑 `assets/scss/_variables_custom.scss`:
```scss
$primary: #your-color !default;
$secondary: #your-color !default;
```

### 更改字体
编辑 `layouts/partials/custom_head.html`:
```html
<link href="https://fonts.googleapis.com/css2?family=Your+Font&display=swap">
```

然后更新 `_variables_custom.scss`:
```scss
$font-family-sans-serif: "Your Font", sans-serif !default;
```

### 添加新组件
在 `assets/scss/components/` 中创建新文件，并在 `custom.scss` 中导入：
```scss
@import 'components/your-component';
```

## 🐛 故障排除

### 样式未生效
1. 清除Hugo缓存: `hugo --gc`
2. 重建网站: `hugo`
3. 检查浏览器缓存

### Logo未显示
1. 验证文件存在于 `assets/media/logo.svg`
2. 检查 `params.yaml` 中的路径是否正确
3. 确保导航栏配置中 `show_logo: true`

### 深色模式问题
1. 检查 `_variables_custom.scss` 中是否定义了深色模式变量
2. 验证 `custom.scss` 中的 `[data-theme="dark"]` 选择器
3. 在浏览器中测试主题切换

## 📝 未来改进

潜在的进一步定制：
- [ ] 更多动画预设
- [ ] 更多配色方案变体
- [ ] 高级排版选项
- [ ] 自定义小部件样式
- [ ] 社交媒体集成样式
- [ ] 增强的移动菜单
- [ ] 阅读进度条
- [ ] Cookie同意横幅样式

## 📖 参考资料

- [Hugo文档](https://gohugo.io/documentation/)
- [Wowchemy主题](https://wowchemy.com/docs/)
- [SCSS指南](https://sass-lang.com/guide)
- [CSS变量](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Using_CSS_custom_properties)

## 📄 许可证

这些定制遵循与Hugo Academic主题相同的许可证（MIT许可证）。

---

**最后更新**: 2026-01-31
**版本**: 1.0
**作者**: Hugo Academic自动定制
