# VANGINES 品牌网站

## 项目说明

这是一个响应式静态网站，完美兼容PC端和移动端，展示VANGINES黑头刮刀 & 冰敷滚轮产品。

## 功能特点

### ✅ 已实现功能

1. **响应式布局**
   - 使用 flexible.min.js 实现移动端适配
   - PC端和移动端完美兼容
   - 断点适配：768px

2. **轮播功能**
   - 顶部Hero Banner轮播（3张图）
   - 产品展示轮播（3张图）
   - 左右箭头切换
   - 自动播放
   - 分页器指示

3. **中英文切换**
   - 一键切换中英文
   - 所有内容完整翻译
   - 语言状态记忆

4. **页面结构**
   - 首页（Hero轮播）
   - 产品展示（轮播）
   - 功能介绍（4个功能卡片）
   - 使用方法（4步骤，左图右文/左文右图交替）
   - 使用场景（3个场景卡片）
   - 品牌故事
   - 底部信息栏

5. **交互效果**
   - 平滑滚动导航
   - 悬停动效
   - 移动端汉堡菜单
   - 响应式导航

## 文件结构

```
vangines/
├── index.html          # 主页面文件
├── readme.md          # 说明文档
├── js/
│   ├── flexible.min.js    # 移动端适配
│   ├── swiper.min.js      # 轮播功能
│   └── js.cookie.min.js   # Cookie管理（备用）
└── images/
    └── logo.png           # Logo图片（占位）
```

## 使用说明

### 1. 直接打开
双击 `index.html` 文件即可在浏览器中打开网站。

### 2. 本地服务器运行（推荐）
```bash
# 使用Python启动本地服务器
python -m http.server 8000

# 或使用Node.js
npx http-server
```

然后在浏览器访问 `http://localhost:8000`

### 3. 替换产品图片

网站中的图片使用占位符，需要替换为真实产品图片：

#### Hero轮播区Banner图
- 文件路径：`images/banner.jpg`
- 建议尺寸：1200x600px（或更高，保持2:1比例）
- 用途：首页左侧大图展示（产品主图或模特使用场景）
- 注意：如需多张轮播图，可准备 banner-2.jpg, banner-3.jpg

#### 产品展示轮播（3张）
- 位置：第149-179行
- 建议尺寸：800x600px
- 产品整体展示：`images/product-1.jpg`
- 冰敷滚轮细节：`images/product-2.jpg`
- 黑头铲功能区：`images/product-3.jpg`

#### 使用方法（4张）
- 位置：第241-326行
- 建议尺寸：600x400px
- 使用前准备：`images/usage-1.jpg`
- 深层清洁：`images/usage-2.jpg`
- 冰敷舒缓：`images/usage-3.jpg`
- 工具清洁收纳：`images/usage-4.jpg`

### 4. 图片替换步骤

1. 将产品图片放入 `images/` 文件夹
2. 在 `index.html` 中找到对应的 `<img>` 标签
3. 替换 `src="images/logo.png"` 为实际图片路径
4. 例如：`src="images/product-1.jpg"`

### 5. 修改内容

所有文本内容都在 `index.html` 文件中：

- **中文内容**：在HTML标签的文本内容中
- **英文翻译**：在JavaScript的 `translations.en` 对象中（第474-551行）

## 技术栈

- HTML5
- CSS3（Flexbox、Grid）
- JavaScript（原生）
- Swiper.js 3.x（轮播）
- Flexible.js（移动端适配）

## 浏览器兼容性

- Chrome（推荐）
- Firefox
- Safari
- Edge
- 移动端浏览器

## 注意事项

1. **图片优化**：建议使用压缩后的图片，提高加载速度
2. **CDN链接**：Swiper CSS使用了CDN链接，确保网络连接正常
3. **本地JS**：flexible.min.js和swiper.min.js已本地引用
4. **字体**：使用系统字体 PingFang SC / Microsoft YaHei

## 自定义配置

### 修改品牌颜色
在CSS中修改主色调（第17行）：
```css
--primary-color: #8B4789; /* 紫色 */
```

### 修改轮播速度
在JavaScript中修改（第569、579行）：
```javascript
autoplay: 5000,  // 自动播放间隔（毫秒）
speed: 800,      // 切换速度（毫秒）
```

### 添加新的翻译
在 `translations` 对象中添加新的键值对：
```javascript
'key.name': '中文文本',  // zh对象中
'key.name': 'English text',  // en对象中
```

## 后续优化建议

1. 添加图片懒加载
2. 添加动画效果（AOS.js）
3. 添加联系表单
4. SEO优化（meta标签）
5. 添加社交媒体分享功能
6. 添加在线购买功能

## 联系方式

如有问题或需要帮助，请联系开发团队。

---

**版本**：1.0.0  
**更新日期**：2025-12-29  
**开发者**：VANGINES Team
