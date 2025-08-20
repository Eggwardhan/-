# 文生图模型场景提示词清单（2025 版）

> 目的：基础的色调，构图修改操作，**仅供参考！！！实际场景需灵活调整**。
> 接触过文生图的可查看进阶的2)配色 3)镜头角度 4)构图
---
<details>

## 0) 通用文本生成图像模板

- **语言**：主提示用英文更稳，必要时附 HEX（如 `#F5F7FA`）。
- **结构**（从重要到次要）：
  1. **Subject**（产品是什么、角度）
  2. **Color & Mood**（配色方案 + 情绪）
  3. **Lighting**（光型/对比）
  4. **Background & Material**（背景材质/肌理）
  5. **Composition**（构图留白/焦段/景深）
  6. **Render Style**（真实/写实/CG/影棚）
  7. **Parameters**（纵横比、风格化等）
- **配色落地技巧**：
  - 用 `palette:` 或 `color palette:` 明示色板；再用 `dominant`, `secondary`, `accent` 指定 60–30–10。
  - 如：`color palette: dominant #F5F7FA, secondary #DDE1E6, accent #111827`。

---

## 1) 通用 Prompt 模板

**通用英文模板**（例子，如需使用可以复制后替换 [变量]）：

```text
[product type], hero shot on [angle/shot],
color palette: dominant [#HEX / color name], secondary [#HEX / color name], accent [#HEX / color name],
[mood adjectives], [style adjectives],
lighting: [softbox/top light/rim light/high key/low key],
background: [material/texture e.g., seamless paper, concrete, wood, fabric, gradient fog],
composition: [minimal/negative space/centered/Rule of Thirds], shallow depth of field,
render: [studio photography / realistic CG / product render], ultra-detailed, crisp edges
```



</details>

---

## 2) 配色 → 提示词块

> 每套均含：**关键词（中英）/ 背景材质 / 灯光 / 色板 / Prompt 片段 / Negative 要点**

### 2.1 纯白高键（High‑key White, Clean E‑commerce）

- **色板**：`#FFFFFF #F5F7FA #DDE1E6`
- **关键词**：clean, high‑key, seamless paper, soft shadows, airy, clinical
- **背景/材质**：white seamless sweep / soft gradient mist
- **灯光**：large softbox top + fill，subtle rim，high key
- **Prompt 片段**：

```text
color palette: dominant #FFFFFF, secondary #F5F7FA, accent #DDE1E6;
lighting: high-key, large softbox, soft shadows; background: white seamless paper, airy gradient
```

- **Negative**：gray cast, strong texture, colored background

### 2.2 高级灰单色（Premium Monochrome Grey, Minimal）

- **色板**：`#111827 #6B7280 #E5E7EB`
- **关键词**：monochrome, slate, minimal, sculptural, tonal contrast
- **背景/材质**：matte concrete / plaster / fog gradient
- **灯光**：directional key + soft fill，medium contrast
- **Prompt 片段**：

```text
color palette: dominant #111827, secondary #6B7280, accent #E5E7EB; background: matte concrete; lighting: directional key, soft fill; mood: minimal, sculptural
```

- **Negative**：colorful accents, warm color cast

### 2.3 暖中性家居（Warm Neutrals, Lifestyle）

- **色板**：`#EDE7DD #CBB7A1 #8B6B52`
- **关键词**：cozy, warm neutral, homey, wood grain, linen
- **背景/材质**：oak wood / linen fabric / plaster wall
- **灯光**：soft window light，warm bounce（\~3200–4000K）
- **Prompt 片段**：

```text
color palette: dominant #EDE7DD, secondary #CBB7A1, accent #8B6B52; background: oak wood and linen; lighting: soft window light, warm bounce; mood: cozy lifestyle
```

- **Negative**：overly saturated colors, glossy plastic feel

### 2.4 冷中性科技（Cool Tech, Rational）

- **色板**：`#0F172A #334155 #93C5FD`
- **关键词**：cool, tech, rational, slate blue, glass, steel
- **背景/材质**：brushed metal / dark glass / grid light
- **灯光**：cool rim + top‑down spot，specular highlights
- **Prompt 片段**：

```text
color palette: dominant #0F172A, secondary #334155, accent #93C5FD; materials: brushed metal, dark glass; lighting: cool rim light, top-down spot; mood: tech, precise
```

- **Negative**：warm yellow cast, wood textures

### 2.5 柔雾奶油（Soft Mist & Cream, Beauty）

- **色板**：`#F7E6E8 #F3D5CE #D7B7A3`
- **关键词**：soft, creamy, blush, hazy, powdery, gentle
- **背景/材质**：pastel gradient fog / satin cloth / cloud dust
- **灯光**：large diffused key，low contrast bloom
- **Prompt 片段**：

```text
color palette: dominant #F7E6E8, secondary #F3D5CE, accent #D7B7A3; background: pastel gradient fog, satin; lighting: diffused, soft bloom; mood: delicate, beauty
```

- **Negative**：hard shadows, sharp textures

### 2.6 大地自然（Earthy Nature, Outdoor/Organic）

- **色板**：`#5B7553 #A3B18A #DAD7CD #6C584C`
- **关键词**：earthy, organic, foliage, stone, moss
- **背景/材质**：moss stone / clay / foliage bokeh
- **灯光**：soft daylight + ambient occlusion，subtle haze
- **Prompt 片段**：

```text
color palette: #5B7553 #A3B18A #DAD7CD #6C584C; materials: stone, clay, moss; lighting: soft daylight, subtle haze; mood: organic, grounded
```

- **Negative**：neon accents, chrome reflections

### 2.7 海滩阳光（Sunny Beach, Refreshing FMCG）

- **色板**：`#00A3C4 #FFE08C #FF6B35`
- **关键词**：sunny, tropical, splash, summer, fresh
- **背景/材质**：turquoise water / sand / splash particles
- **灯光**：backlit sunshine + sparkle highlights，high contrast
- **Prompt 片段**：

```text
color palette: dominant #00A3C4, secondary #FFE08C, accent #FF6B35; background: turquoise water and sand; lighting: bright backlit sunshine, sparkle highlights; mood: energetic, refreshing
```

- **Negative**：overcast, dull tones, muddy water

### 2.8 复古蓝橘（Retro Blue–Orange, Nostalgic）

- **色板**：`#3A5A9F #264653 #F4A261`
- **关键词**：retro, analog vibe, teal & orange, grain
- **背景/材质**：retro tiles / vintage paper / film grain
- **灯光**：warm key + cool fill，filmic contrast
- **Prompt 片段**：

```text
color palette: #3A5A9F #264653 #F4A261; mood: retro nostalgic; lighting: warm key, cool fill; background: vintage paper with subtle film grain
```

- **Negative**：neon glow, modern chrome

### 2.9 宝石深邃 + 金属（Jewel Tones + Metallic, Luxury）

- **色板**：`#0B132B #1B3A4B #D4AF37`
- **关键词**：luxury, jewel tone, velvet, metallic gold, dramatic
- **背景/材质**：velvet drape / lacquer / marble
- **灯光**：low key + edge rim，specular gold highlights
- **Prompt 片段**：

```text
color palette: dominant #0B132B, secondary #1B3A4B, accent #D4AF37; materials: velvet and gold; lighting: low-key, dramatic rim; mood: opulent, premium
```

- **Negative**：pastel, flat lighting

### 2.10 赛博霓虹（Cyber Neon, Sport/Gaming）

- **色板**：`#0A0A0A #00E5FF #FF00A0 #39FF14`
- **关键词**：neon glow, cyberpunk, dark grid, chroma edges
- **背景/材质**：dark grid / holographic fog / light streaks
- **灯光**：RGB rim lights，volumetric fog，specular
- **Prompt 片段**：

```text
color palette: #0A0A0A #00E5FF #FF00A0 #39FF14; background: dark grid with holographic fog; lighting: neon rim lights, volumetric glow; mood: energetic, futuristic
```

- **Negative**：warm wood, daylight, soft pastel

### 2.11 北欧日式（Scandi–Japandi, Natural Minimal）

- **色板**：`#F5F1E6 #D9CBB5 #8D8F8A #8C6A3D`
- **关键词**：calm, natural minimal, wood & stone, wabi‑sabi
- **背景/材质**：ash wood / stone / paper fiber
- **灯光**：soft north light，low contrast
- **Prompt 片段**：

```text
color palette: #F5F1E6 #D9CBB5 #8D8F8A #8C6A3D; materials: ash wood, stone, paper fiber; lighting: soft north light; mood: calm, natural minimal
```

- **Negative**：glossy plastic, saturated neon

### 2.12 黑金戏剧（Black & Gold, Dramatic Commercial）

- **色板**：`#0B0B0C #1F1F1F #D4AF37 #8C7853`
- **关键词**：dramatic, black void, gold accents, spotlight
- **背景/材质**：black velvet / smoke / gold dust
- **灯光**：low key spotlight + rim，hard contrast
- **Prompt 片段**：

```text
color palette: #0B0B0C #1F1F1F #D4AF37 #8C7853; background: black velvet with subtle smoke; lighting: dramatic spotlight and rim; mood: premium, powerful
```

- **Negative**：flat grey background, pastel tones

---

## 3) 镜头角度

### 核心常用角度（主图/详情页最常见）
	•	正面视图 (Front view)：直观展示产品的主体外观，常用于主图。
	•	侧面图 (Side view) / 后视图 (Back view)：帮助展示产品不同角度的细节，适合服装、鞋子、包类等。
	•	全景图 (Panorama / Wide view)：用于大型商品（家具、家电），强调整体感。
	•	特写 (Close up / Extreme closeup)：突出细节、材质、质感，如珠宝、手表、布料。
	•	胸部以上 (Waist shot) / 全身 (Full body)：适合服饰、模特穿搭，展示比例。

⸻

### 细节与氛围增强角度
	•	微距拍摄 (Macro shot)：展示小件商品（首饰、化妆品、电子元件）的细节。
	•	虚化 (Bokeh)：背景模糊，突出产品主体，适合美妆、奢侈品。
	•	高角度视图 (High angle view)：俯拍，适合桌面小物件、餐饮产品，营造干净构图。
	•	低角度视图 (Low angle view / Look up)：让产品显得更有气势，常用于鞋子、汽车、运动用品。

⸻

### 营销场景常见特殊角度
	•	航拍视角 (Aerial view / Bird view / Top view)：常用于餐饮、美妆套装、桌面布置，带来整体协调感。
	•	等距视图 (Isometric view)：适合3C数码类产品，能均衡展示结构与细节。
	•	长焦镜头 (Telephoto lens)：压缩空间感，适合展示产品和背景氛围。
	•	超广角拍摄 (Ultrawide shot)：突出空间感，适合家具、室内装饰场景。

### 常用提示词
| Prompt 中文提示词 | Prompt 英文提示词         |
|------------------|--------------------------|
| 航拍视角         | Aerial view              |
| DSLR拍摄         | Shot by DSLR             |
| 360全景图        | 360 Panorama             |
| 全景图           | Panorama                 |
| 长焦镜头         | Telephoto Lens           |
| 微距拍摄         | Macro shot               |
| 显微镜           | Microscopy               |
| 放大倍数         | Magnification            |
| 特写             | Close up                 |
| 全身             | Full body                |
| 肖像             | Portrait                 |
| 侧身像           | Profile                  |
| 针孔镜头         | Pinhole Lens             |
| 广视角           | Wide view                |
| 望远镜镜头       | Telescope Lens           |
| 卫星图像         | Satellite lmagery        |
| 头部特写         | Headshot                 |
| 极端特写         | Extreme closeup          |
| 超广角拍摄       | Ultrawide shot           |
| 鸟瞰图           | Bird view                |
| 顶视图           | Top view                 |
| 前视图           | Front view               |
| 侧面图           | Side view                |
| 后视图           | Back view                |
| 脸部特写         | Face shot                |
| 胸部以上         | Waist shot               |
| 长距拍摄         | Extra long shot          |
| 仰视             | look up                  |
| 等距视图         | isometric view           |
| 高角度视图       | High angle view          |
| 低角度视图       | Low angle view           |
| 虚化             | Bokeh                    |

---

## 4) 构图
### 常见构图
> Tips: 请注意，本prompt仅作为构图参考，如需要*保持一致性*需要添加额外提示词！！！

| 场景用途 | 场景描述与布置 | 推荐角度/镜头 | Prompt 示例（中 / EN） |
|---|---|---|---|
|图中图|图像中需要插入一个块展示产品细节|根据具体情况决定|中：插入圆形细节框，展示[商品部分区域]，放大细节标注，带引导线和极细轮廓线  En: inset circular detail to show the [商品部分区域] , magnified detail callout, leader line, hairline outline|
|产品图|图像需要标注尺寸+白底图，标题|前视图 Front view + 长焦镜头 Telephoto|中：纯白#FFFFFF背景产品图，正面视图，长宽高尺寸标注，清晰无干扰EN: change the background to #FFFFFF pure white, front view, telephoto lens, clear width/height/depth dimension annotations|
| 主图（白底Packshot） | 纯白背景、主体居中、无阴影干扰，适合电商首页主图 | 前视图 Front view + DSLR拍摄 Shot by DSLR | 中：纯白背景主图，正面视图，DSLR拍摄，产品占画面85%，高质感<br>EN: Main product on pure white background, front view, shot by DSLR, product fills 85% of frame, high fidelity |
| 45°三分之四视角（立体展示） | 轻微俯拍，更显体积与层次 | 高角度视图 High angle view + 等距视图 isometric view | 中：等距视图45°高角度，灰渐变背景，柔光<br>EN: Isometric 45° high angle view, gray gradient backdrop, soft lighting |
| 三视图（正/侧/背） | 同一光位呈现正面、侧面、背面，信息完整 | 前视图/侧面图/后视图 Front/Side/Back view | 中：统一灯光的正侧背三视图排版，灰白背景<br>EN: Consistent lighting front/side/back views in a clean layout, light gray background |
| 细节材质（质感卖点） | 纹理、缝线、按键、接口等 | 微距拍摄 Macro shot + 极端特写 Extreme closeup + 放大倍数 Magnification | 中：材质微距特写，极端特写，1.5×放大，景深浅，虚化<br>EN: Macro detail, extreme close-up, 1.5× magnification, shallow depth of field, bokeh |
| 功能信息/接口说明 | 标出功能区、按钮、端口 | 顶视图 Top view 或 等距视图 isometric view + 长焦镜头 Telephoto Lens（压缩透视） | 中：等距视图功能标注图，长焦镜头压缩透视，清晰指示线与标签<br>EN: Isometric feature callout, telephoto compression, clean leader lines and labels |
| 开箱&全配件（In the box） | 产品+配件一字排开，便于理解清单 | 顶视图 Top view + 全景图 Panorama（横幅排版） | 中：顶视图开箱平铺，全配件整齐排列，柔和阴影。画面中只包含下列配件：[商品区域]所有物品整齐对齐排布，灰色背景，无其他任何物品。<br>EN: Top-view unboxing flat lay, all accessories neatly aligned, soft shadows. The image must include only the following items: [商品区域]All items neatly aligned on a gray background, no additional objects.|
| 尺寸比例（上手/情景比例） | 手持、桌面、背包旁等做参照 | 侧面图 Side view 或 低角度视图 Low angle view + 虚化 Bokeh（突出主体） | 中：真实场景上手图，低角度视图，背景虚化突出主体<br>EN: In-hand lifestyle, low angle view, background bokeh to emphasize product |
| 生活方式（卖点落地） | 在真实使用环境，强调人群与场景 | 广视角 Wide view / 超广角 Ultrawide shot（谨慎避免变形） + 高/低角度 High/Low angle | 中：厨房台面生活方式场景，广视角，高角度视图，自然光<br>EN: Lifestyle in kitchen countertop, wide view, high angle, natural light |
| 360°旋转/多角合集 | 多角度一屏呈现或旋转序列 | 360全景图 360 Panorama + 顶视/前视 Top/Front view | 中：360°多角度合集，白底，统一光位与间隔<br>EN: 360° angle collage on white background, consistent lighting and spacing |
| 对比/前后变化（清洁类/美妆） | 功效展示或旧款对比 | 前视图 Front view + 长焦镜头 Telephoto（减少变形） | 中：前后对比图，正面同角度同光位，长焦镜头，标注差异<br>EN: Before/after comparison, identical front view and lighting, telephoto lens, clear annotations |


⸻

服饰&穿戴类补充（模特与角度）
	•	全身 Full body / 半身 Waist shot / 肖像 Portrait / 侧身像 Profile / 后视图 Back view / 头部特写 Headshot
	•	建议：主图用正面全身或半身；详页补充侧/背/细节（领口、面料、走线）；户外生活方式图用低角度 Low angle略显比例更好，背景Bokeh突出服装层次。

示例Prompt（服饰）
	•	中：女款风衣，城市街景生活方式，低角度视图，半身，Bokeh，DSLR拍摄
	•	EN: Women's trench coat, urban lifestyle scene, low angle view, waist shot, bokeh, shot by DSLR

⸻

快速布光与镜头小贴士
	•	主图/三视图：双侧柔光 + 顶补光，长焦或标准焦（避免超广角变形）。
	•	微距细节：小光圈（加景深）或焦点堆栈，避免镜面高光炸点。
	•	生活方式：主光45°侧前上，环境光做氛围，背景保持2–3级更暗或虚化。
	•	避免失真：家具/箱包尽量用Telephoto Lens；空间展示可用Wide view，谨慎Ultrawide shot。


---

## 5) 小贴士

- **强调主色对比**：写入 `high contrast between subject and background`；若产品色接近背景，改用 `complementary background hue`。
- **电商规范**：如平台要求白底，依 2.1 模板仅保留 `#FFFFFF` 系列

