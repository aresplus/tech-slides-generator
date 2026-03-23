# Tech Slides Design System (Python-PPTX Parameters)

> The aesthetic knowledge base for tech-slides-generator. This defines how CSS/Cyberpunk aesthetics are translated into `python-pptx` RGB parameters.

## 1. Expanded Color Themes (HEX mapped to RGB)

When writing Python code, convert these HEX values to `RGBColor(R, G, B)`.

### 1.1 Cyber-Purple (AI / Default)
- `bg_primary`: #0B0D17 -> `RGBColor(11, 13, 23)`
- `panel_bg`: #131629 -> `RGBColor(19, 22, 41)`
- `accent_primary`: #7B2FFF -> `RGBColor(123, 47, 255)`
- `text_main`: #E8E6F0 -> `RGBColor(232, 230, 240)`

### 1.2 Matrix-Green (Cybersecurity)
- `bg_primary`: #000000 -> `RGBColor(0, 0, 0)`
- `panel_bg`: #0A0F0A -> `RGBColor(10, 15, 10)`
- `accent_primary`: #00FF41 -> `RGBColor(0, 255, 65)`
- `text_main`: #C8E6C9 -> `RGBColor(200, 230, 201)`

### 1.3 Crimson-Red (Automotive / Hardcore Tech)
- `bg_primary`: #0F0505 -> `RGBColor(15, 5, 5)`
- `panel_bg`: #1A0A0A -> `RGBColor(26, 10, 10)`
- `accent_primary`: #FF003C -> `RGBColor(255, 0, 60)`
- `text_main`: #F5F5F5 -> `RGBColor(245, 245, 245)`

### 1.4 Solaris-Orange (Aerospace / Hardware)
- `bg_primary`: #1A1A1A -> `RGBColor(26, 26, 26)`
- `panel_bg`: #252525 -> `RGBColor(37, 37, 37)`
- `accent_primary`: #FF6B2B -> `RGBColor(255, 107, 43)`
- `text_main`: #F0E6DC -> `RGBColor(240, 230, 220)`

### 1.5 Deep-Black (Ultimate Minimalism)
- `bg_primary`: #000000 -> `RGBColor(0, 0, 0)`
- `panel_bg`: #111111 -> `RGBColor(17, 17, 17)`
- `accent_primary`: #FFFFFF -> `RGBColor(255, 255, 255)`
- `text_main`: #CCCCCC -> `RGBColor(204, 204, 204)`

### 1.6 Pure-White (Clinical / Apple-Style)
- `bg_primary`: #FFFFFF -> `RGBColor(255, 255, 255)`
- `panel_bg`: #F2F2F7 -> `RGBColor(242, 242, 247)`
- `accent_primary`: #0066CC -> `RGBColor(0, 102, 204)`
- `text_main`: #1D1D1F -> `RGBColor(29, 29, 31)`

## 2. Typography Rules (Python Implementations)

- **English Fonts**: Set `run.font.name = 'Arial'` or `'Consolas'` (for tech vibe).
- **Chinese Fonts**: Set `run.font.name = 'Microsoft YaHei'` (微软雅黑) or `'PingFang SC'`.
- **Title Weight**: Set `run.font.bold = True`, size = `Pt(44)` to `Pt(64)`.
- **Colors**: ALWAYS set `run.font.color.rgb` to ensure text is visible against dark backgrounds.

## 3. Simulating Tech UI in PPTX

Since native PPTX doesn't support CSS glassmorphism easily via code, we simulate the "Bento Box" / "Cyber Panel" aesthetic:
1. Create a shape: `shape = slide.shapes.add_shape(MSO_SHAPE.ROUNDED_RECTANGLE, left, top, width, height)`
2. Set fill: `shape.fill.solid()`, `shape.fill.fore_color.rgb = panel_bg`
3. Set glowing border: `shape.line.color.rgb = accent_primary`, `shape.line.width = Pt(1.5)`
4. Add text into the shape using the `text_main` color.

## 4. Image Prompting Rules
Fetch Unsplash images directly in Python using `requests` and `BytesIO` to insert real images into the slides.
Example URL: `https://source.unsplash.com/800x600/?neural-network,dark`