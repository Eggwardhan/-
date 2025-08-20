<div align="center">

# 🎨 文生图模型场景提示词清单（2025 版）

**基于实践的完整提示词参考指南**

</div>

---

## 📋 使用说明

> **🎯 目的**：基础的色调，构图修改操作，**仅供参考！！！实际场景需灵活调整**。  
> **📚 进阶指南**：接触过文生图的可查看进阶的 2)配色、3)镜头角度、4)构图

---
## 🚀 快速开始

<details>
<summary><strong>📖 点击展开：通用文本生成图像模板</strong></summary>

### 0️⃣ 通用文本生成图像模板

#### 🌐 语言选择
- **主提示用英文更稳**，必要时附 HEX（如 `#F5F7FA`）

#### 🏗️ 结构框架（重要度递减）
1. **Subject** - 产品是什么、角度
2. **Color & Mood** - 配色方案 + 情绪
3. **Lighting** - 光型/对比
4. **Background & Material** - 背景材质/肌理
5. **Composition** - 构图留白/焦段/景深
6. **Render Style** - 真实/写实/CG/影棚
7. **Parameters** - 纵横比、风格化等

#### 🎨 配色落地技巧
- 用 `palette:` 或 `color palette:` 明示色板
- 用 `dominant`, `secondary`, `accent` 指定 **60–30–10** 比例
- **示例**：`color palette: dominant #F5F7FA, secondary #DDE1E6, accent #111827`

---

### 1️⃣ 通用 Prompt 模板

#### 📝 英文模板框架
> 📋 **使用说明**：复制以下模板，替换 `[变量]` 部分即可使用

```markdown
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

## 🎨 配色方案库

> 📦 **包含要素**：关键词（中英）/ 背景材质 / 灯光 / 色板 / Prompt 片段 / Negative 要点

<div align="center">

**选择适合您项目的配色方案 👇**

</div>

### 2.1 ⚪ 纯白高键（High‑key White, Clean E‑commerce）

<table>
<tr>
<td><strong>🎨 色板</strong></td>
<td><code style="background:#FFFFFF;border:1px solid #ddd">#FFFFFF</code> <code style="background:#F5F7FA;border:1px solid #ddd">#F5F7FA</code> <code style="background:#DDE1E6;border:1px solid #ddd">#DDE1E6</code></td>
</tr>
<tr>
<td><strong>🏷️ 关键词</strong></td>
<td>clean, high‑key, seamless paper, soft shadows, airy, clinical</td>
</tr>
<tr>
<td><strong>🖼️ 背景/材质</strong></td>
<td>white seamless sweep / soft gradient mist</td>
</tr>
<tr>
<td><strong>💡 灯光</strong></td>
<td>large softbox top + fill，subtle rim，high key</td>
</tr>
</table>

**📝 Prompt 片段**：
```text
color palette: dominant #FFFFFF, secondary #F5F7FA, accent #DDE1E6;
lighting: high-key, large softbox, soft shadows; background: white seamless paper, airy gradient
```

**❌ Negative**：gray cast, strong texture, colored background

### 2.2 🔘 高级灰单色（Premium Monochrome Grey, Minimal）

<table>
<tr>
<td><strong>🎨 色板</strong></td>
<td><code style="background:#111827;color:white;border:1px solid #ddd">#111827</code> <code style="background:#6B7280;color:white;border:1px solid #ddd">#6B7280</code> <code style="background:#E5E7EB;border:1px solid #ddd">#E5E7EB</code></td>
</tr>
<tr>
<td><strong>🏷️ 关键词</strong></td>
<td>monochrome, slate, minimal, sculptural, tonal contrast</td>
</tr>
<tr>
<td><strong>🖼️ 背景/材质</strong></td>
<td>matte concrete / plaster / fog gradient</td>
</tr>
<tr>
<td><strong>💡 灯光</strong></td>
<td>directional key + soft fill，medium contrast</td>
</tr>
</table>

**📝 Prompt 片段**：
```text
color palette: dominant #111827, secondary #6B7280, accent #E5E7EB; background: matte concrete; lighting: directional key, soft fill; mood: minimal, sculptural
```

**❌ Negative**：colorful accents, warm color cast

### 2.3 🤎 暖中性家居（Warm Neutrals, Lifestyle）

<table>
<tr>
<td><strong>🎨 色板</strong></td>
<td><code style="background:#EDE7DD;border:1px solid #ddd">#EDE7DD</code> <code style="background:#CBB7A1;border:1px solid #ddd">#CBB7A1</code> <code style="background:#8B6B52;color:white;border:1px solid #ddd">#8B6B52</code></td>
</tr>
<tr>
<td><strong>🏷️ 关键词</strong></td>
<td>cozy, warm neutral, homey, wood grain, linen</td>
</tr>
<tr>
<td><strong>🖼️ 背景/材质</strong></td>
<td>oak wood / linen fabric / plaster wall</td>
</tr>
<tr>
<td><strong>💡 灯光</strong></td>
<td>soft window light，warm bounce（~3200–4000K）</td>
</tr>
</table>

**📝 Prompt 片段**：
```text
color palette: dominant #EDE7DD, secondary #CBB7A1, accent #8B6B52; background: oak wood and linen; lighting: soft window light, warm bounce; mood: cozy lifestyle
```

**❌ Negative**：overly saturated colors, glossy plastic feel

### 2.4 💙 冷中性科技（Cool Tech, Rational）

<table>
<tr>
<td><strong>🎨 色板</strong></td>
<td><code style="background:#0F172A;color:white;border:1px solid #ddd">#0F172A</code> <code style="background:#334155;color:white;border:1px solid #ddd">#334155</code> <code style="background:#93C5FD;border:1px solid #ddd">#93C5FD</code></td>
</tr>
<tr>
<td><strong>🏷️ 关键词</strong></td>
<td>cool, tech, rational, slate blue, glass, steel</td>
</tr>
<tr>
<td><strong>🖼️ 背景/材质</strong></td>
<td>brushed metal / dark glass / grid light</td>
</tr>
<tr>
<td><strong>💡 灯光</strong></td>
<td>cool rim + top‑down spot，specular highlights</td>
</tr>
</table>

**📝 Prompt 片段**：
```text
color palette: dominant #0F172A, secondary #334155, accent #93C5FD; materials: brushed metal, dark glass; lighting: cool rim light, top-down spot; mood: tech, precise
```

**❌ Negative**：warm yellow cast, wood textures

### 2.5 🌸 柔雾奶油（Soft Mist & Cream, Beauty）

<table>
<tr>
<td><strong>🎨 色板</strong></td>
<td><code style="background:#F7E6E8;border:1px solid #ddd">#F7E6E8</code> <code style="background:#F3D5CE;border:1px solid #ddd">#F3D5CE</code> <code style="background:#D7B7A3;border:1px solid #ddd">#D7B7A3</code></td>
</tr>
<tr>
<td><strong>🏷️ 关键词</strong></td>
<td>soft, creamy, blush, hazy, powdery, gentle</td>
</tr>
<tr>
<td><strong>🖼️ 背景/材质</strong></td>
<td>pastel gradient fog / satin cloth / cloud dust</td>
</tr>
<tr>
<td><strong>💡 灯光</strong></td>
<td>large diffused key，low contrast bloom</td>
</tr>
</table>

**📝 Prompt 片段**：
```text
color palette: dominant #F7E6E8, secondary #F3D5CE, accent #D7B7A3; background: pastel gradient fog, satin; lighting: diffused, soft bloom; mood: delicate, beauty
```

**❌ Negative**：hard shadows, sharp textures

### 2.6 🌿 大地自然（Earthy Nature, Organic）

<table>
<tr>
<td><strong>🎨 色板</strong></td>
<td><code style="background:#5B7553;color:white;border:1px solid #ddd">#5B7553</code> <code style="background:#A3B18A;border:1px solid #ddd">#A3B18A</code> <code style="background:#DAD7CD;border:1px solid #ddd">#DAD7CD</code> <code style="background:#6C584C;color:white;border:1px solid #ddd">#6C584C</code></td>
</tr>
<tr>
<td><strong>🏷️ 关键词</strong></td>
<td>earthy, organic, foliage, stone, moss</td>
</tr>
<tr>
<td><strong>🖼️ 背景/材质</strong></td>
<td>moss stone / clay / foliage bokeh</td>
</tr>
<tr>
<td><strong>💡 灯光</strong></td>
<td>soft daylight + ambient occlusion，subtle haze</td>
</tr>
</table>

**📝 Prompt 片段**：
```text
color palette: #5B7553 #A3B18A #DAD7CD #6C584C; materials: stone, clay, moss; lighting: soft daylight, subtle haze; mood: organic, grounded
```

**❌ Negative**：neon accents, chrome reflections

### 2.7 🌊 海滩阳光（Sunny Beach, Refreshing）

<table>
<tr>
<td><strong>🎨 色板</strong></td>
<td><code style="background:#00A3C4;color:white;border:1px solid #ddd">#00A3C4</code> <code style="background:#FFE08C;border:1px solid #ddd">#FFE08C</code> <code style="background:#FF6B35;color:white;border:1px solid #ddd">#FF6B35</code></td>
</tr>
<tr>
<td><strong>🏷️ 关键词</strong></td>
<td>sunny, tropical, splash, summer, fresh</td>
</tr>
<tr>
<td><strong>🖼️ 背景/材质</strong></td>
<td>turquoise water / sand / splash particles</td>
</tr>
<tr>
<td><strong>💡 灯光</strong></td>
<td>backlit sunshine + sparkle highlights，high contrast</td>
</tr>
</table>

**📝 Prompt 片段**：
```text
color palette: dominant #00A3C4, secondary #FFE08C, accent #FF6B35; background: turquoise water and sand; lighting: bright backlit sunshine, sparkle highlights; mood: energetic, refreshing
```

**❌ Negative**：overcast, dull tones, muddy water

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

## 📷 镜头角度指南

<div align="center">

**专业摄影角度选择参考**

</div>

### 🎯 核心常用角度（主图/详情页最常见）

| 角度类型 | 英文术语 | 适用场景 | 特点描述 |
|---------|---------|----------|----------|
| 正面视图 | Front view | 主图展示 | 直观展示产品主体外观 |
| 侧面图 | Side view | 服装、鞋子、包类 | 展示产品不同角度细节 |
| 后视图 | Back view | 服装、包类 | 完整展示产品信息 |
| 全景图 | Panorama / Wide view | 家具、家电 | 强调整体感和尺寸 |
| 特写 | Close up / Extreme closeup | 珠宝、手表、布料 | 突出细节、材质、质感 |
| 胸部以上 | Waist shot | 服饰展示 | 展示穿搭效果和比例 |
| 全身 | Full body | 模特穿搭 | 完整展示造型效果 |

### ⚡ 细节与氛围增强角度

| 角度类型 | 英文术语 | 适用场景 | 效果描述 |
|---------|---------|----------|----------|
| 微距拍摄 | Macro shot | 首饰、化妆品、电子元件 | 展示精细细节 |
| 虚化 | Bokeh | 美妆、奢侈品 | 背景模糊，突出主体 |
| 高角度视图 | High angle view | 桌面小物件、餐饮 | 营造干净构图 |
| 低角度视图 | Low angle view / Look up | 鞋子、汽车、运动用品 | 增强气势感 |

### 🚀 特殊场景角度

| 角度类型 | 英文术语 | 适用场景 | 营销效果 |
|---------|---------|----------|----------|
| 航拍视角 | Aerial view / Bird view / Top view | 餐饮、美妆套装、桌面布置 | 整体协调感 |
| 等距视图 | Isometric view | 3C数码产品 | 均衡展示结构与细节 |
| 长焦镜头 | Telephoto lens | 产品氛围展示 | 压缩空间感 |
| 超广角拍摄 | Ultrawide shot | 家具、室内装饰 | 突出空间感 |

### 📝 常用提示词速查表

| 🇨🇳 中文提示词 | 🇺🇸 英文提示词 | 📝 适用场景 |
|------------------|--------------------------|-------------|
| 航拍视角 | Aerial view | 俯瞰全景，大场面 |
| DSLR拍摄 | Shot by DSLR | 专业品质，主图 |
| 360全景图 | 360 Panorama | 产品展示，VR |
| 全景图 | Panorama | 宽幅场景 |
| 长焦镜头 | Telephoto Lens | 压缩空间，突出主体 |
| 微距拍摄 | Macro shot | 细节展示 |
| 显微镜 | Microscopy | 超微细节 |
| 放大倍数 | Magnification | 放大展示 |
| 特写 | Close up | 重点突出 |
| 全身 | Full body | 完整展示 |
| 肖像 | Portrait | 人像拍摄 |
| 侧身像 | Profile | 侧面轮廓 |
| 针孔镜头 | Pinhole Lens | 艺术效果 |
| 广视角 | Wide view | 场景感强 |
| 望远镜镜头 | Telescope Lens | 远距离拍摄 |
| 卫星图像 | Satellite lmagery | 超高视角 |
| 头部特写 | Headshot | 头部聚焦 |
| 极端特写 | Extreme closeup | 超近距离 |
| 超广角拍摄 | Ultrawide shot | 空间感强 |
| 鸟瞰图 | Bird view | 高处俯视 |
| 顶视图 | Top view | 正上方视角 |
| 前视图 | Front view | 正面展示 |
| 侧面图 | Side view | 侧面细节 |
| 后视图 | Back view | 背面展示 |
| 脸部特写 | Face shot | 面部聚焦 |
| 胸部以上 | Waist shot | 上半身 |
| 长距拍摄 | Extra long shot | 远景拍摄 |
| 仰视 | look up | 仰角拍摄 |
| 等距视图 | isometric view | 立体展示 |
| 高角度视图 | High angle view | 俯拍视角 |
| 低角度视图 | Low angle view | 仰拍视角 |
| 虚化 | Bokeh | 背景模糊 |

---

## 🖼️ 构图方案库

<div align="center">

**专业构图与场景应用指南**

</div>

### 📐 构图方案总览

<div align="center">

**🎯 专业构图场景应用指南**

*⚠️ 重要提示：本prompt仅作为构图参考，如需保持一致性请添加额外提示词！*

</div>

---

#### 🏷️ **电商核心场景**

<table>
<tr>
<th width="15%">🎯 场景用途</th>
<th width="20%">📝 场景描述与布置</th>
<th width="15%">📷 推荐角度/镜头</th>
<th width="50%">💬 Prompt 示例</th>
</tr>
<tr>
<td><strong>🔍 图中图</strong></td>
<td>图像中插入细节展示块</td>
<td>根据具体情况决定</td>
<td><strong>🇨🇳</strong> 插入圆形细节框，展示[商品部分区域]，放大细节标注，带引导线和极细轮廓线<br><strong>🇺🇸</strong> inset circular detail to show the [商品部分区域], magnified detail callout, leader line, hairline outline</td>
</tr>
<tr>
<td><strong>📏 产品图</strong></td>
<td>标注尺寸+白底图，标题</td>
<td>前视图 + 长焦镜头</td>
<td><strong>🇨🇳</strong> 纯白#FFFFFF背景产品图，正面视图，长宽高尺寸标注，清晰无干扰<br><strong>🇺🇸</strong> change the background to #FFFFFF pure white, front view, telephoto lens, clear width/height/depth dimension annotations</td>
</tr>
<tr>
<td><strong>🖼️ 主图（白底Packshot）</strong></td>
<td>纯白背景、主体居中、无阴影干扰</td>
<td>前视图 + DSLR拍摄</td>
<td><strong>🇨🇳</strong> 纯白背景主图，正面视图，DSLR拍摄，产品占画面85%，高质感<br><strong>🇺🇸</strong> Main product on #FFFFFF	background, front view, shot by DSLR, product fills 85% of frame, high fidelity</td>
</tr>
<tr>
<td><strong>📐 45°三分之四视角</strong></td>
<td>轻微俯拍，更显体积与层次</td>
<td>高角度视图 + 等距视图</td>
<td><strong>🇨🇳</strong> 等距视图45°高角度，灰渐变背景，柔光<br><strong>🇺🇸</strong> Isometric 45° high angle view, gray gradient backdrop, soft lighting</td>
</tr>
<tr>
<td><strong>🔄 三视图（正/侧/背）</strong></td>
<td>同一光位呈现正面、侧面、背面</td>
<td>前视图/侧面图/后视图</td>
<td><strong>🇨🇳</strong> 统一灯光的正侧背三视图排版，灰白背景<br><strong>🇺🇸</strong> Consistent lighting front/side/back views in a clean layout, light gray background</td>
</tr>
</table>

---

#### 🔍 **细节展示场景**

<table>
<tr>
<th width="15%">🎯 场景用途</th>
<th width="20%">📝 场景描述与布置</th>
<th width="15%">📷 推荐角度/镜头</th>
<th width="50%">💬 Prompt 示例</th>
</tr>
<tr>
<td><strong>🔬 细节材质</strong></td>
<td>纹理、缝线、按键、接口等</td>
<td>微距拍摄 + 极端特写 + 放大倍数</td>
<td><strong>🇨🇳</strong> 材质微距特写，极端特写，1.5×放大，景深浅，虚化<br><strong>🇺🇸</strong> Macro detail, extreme close-up, 1.5× magnification, shallow depth of field, bokeh</td>
</tr>
<tr>
<td><strong>⚙️ 功能信息/接口说明</strong></td>
<td>标出功能区、按钮、端口</td>
<td>顶视图 或 等距视图 + 长焦镜头</td>
<td><strong>🇨🇳</strong> 等距视图功能标注图，长焦镜头压缩透视，清晰指示线与标签<br><strong>🇺🇸</strong> Isometric feature callout, telephoto compression, clean leader lines and labels</td>
</tr>
<tr>
<td><strong>📦 开箱&全配件</strong></td>
<td>产品+配件一字排开，便于理解清单</td>
<td>顶视图 + 全景图（横幅排版）</td>
<td><strong>🇨🇳</strong> 顶视图开箱平铺，全配件整齐排列，柔和阴影。画面中只包含下列配件：[商品区域]所有物品整齐对齐排布，灰色背景，无其他任何物品。<br><strong>🇺🇸</strong> Top-view unboxing flat lay, all accessories neatly aligned, soft shadows. The image must include only the following items: [商品区域]All items neatly aligned on a gray background, no additional objects.</td>
</tr>
</table>

---

#### 🌟 **营销展示场景**

<table>
<tr>
<th width="15%">🎯 场景用途</th>
<th width="20%">📝 场景描述与布置</th>
<th width="15%">📷 推荐角度/镜头</th>
<th width="50%">💬 Prompt 示例</th>
</tr>
<tr>
<td><strong>📏 尺寸比例</strong></td>
<td>手持、桌面、背包旁等做参照</td>
<td>侧面图 或 低角度视图 + 虚化</td>
<td><strong>🇨🇳</strong> 真实场景上手图，低角度视图，背景虚化突出主体<br><strong>🇺🇸</strong> In-hand lifestyle, low angle view, background bokeh to emphasize product</td>
</tr>
<tr>
<td><strong>🏠 生活方式</strong></td>
<td>在真实使用环境，强调人群与场景</td>
<td>广视角 / 超广角 + 高/低角度</td>
<td><strong>🇨🇳</strong> 厨房台面生活方式场景，广视角，高角度视图，自然光<br><strong>🇺🇸</strong> Lifestyle in kitchen countertop, wide view, high angle, natural light</td>
</tr>
<tr>
<td><strong>🔄 360°旋转/多角合集</strong></td>
<td>多角度一屏呈现或旋转序列</td>
<td>360全景图 + 顶视/前视</td>
<td><strong>🇨🇳</strong> 360°多角度合集，白底，统一光位与间隔<br><strong>🇺🇸</strong> 360° angle collage on white background, consistent lighting and spacing</td>
</tr>
<tr>
<td><strong>⚖️ 对比/前后变化</strong></td>
<td>功效展示或旧款对比</td>
<td>前视图 + 长焦镜头（减少变形）</td>
<td><strong>🇨🇳</strong> 前后对比图，正面同角度同光位，长焦镜头，标注差异<br><strong>🇺🇸</strong> Before/after comparison, identical front view and lighting, telephoto lens, clear annotations</td>
</tr>
</table>


---

#### 👗 **服饰穿戴类补充**

<div align="center">

**🎭 模特与角度专业指南**

</div>

<table>
<tr>
<th width="20%">📸 拍摄角度</th>
<th width="30%">🎯 适用场景</th>
<th width="50%">💡 专业建议</th>
</tr>
<tr>
<td><strong>👤 全身 Full body</strong></td>
<td>主图展示、整体造型</td>
<td>适合展示完整穿搭效果，建议正面或45°角度</td>
</tr>
<tr>
<td><strong>🖼️ 半身 Waist shot</strong></td>
<td>主图、详情页</td>
<td>突出上半身设计，适合展示领口、袖口细节</td>
</tr>
<tr>
<td><strong>🎭 肖像 Portrait</strong></td>
<td>面部特写、妆容展示</td>
<td>配合美妆产品，突出面部细节</td>
</tr>
<tr>
<td><strong>👥 侧身像 Profile</strong></td>
<td>侧面轮廓、剪裁展示</td>
<td>展示服装侧面线条和剪裁工艺</td>
</tr>
<tr>
<td><strong>🔙 后视图 Back view</strong></td>
<td>背面设计、细节展示</td>
<td>展示背面设计元素、拉链、装饰等</td>
</tr>
<tr>
<td><strong>👤 头部特写 Headshot</strong></td>
<td>配饰、妆容展示</td>
<td>突出帽子、耳环、项链等配饰细节</td>
</tr>
</table>

**📝 服饰拍摄建议**：
- **主图**：使用正面全身或半身
- **详情页**：补充侧/背/细节（领口、面料、走线）
- **户外生活方式**：低角度 Low angle 显比例更好，背景 Bokeh 突出服装层次

**💬 示例Prompt（服饰）**：
- **🇨🇳** 女款风衣，城市街景生活方式，低角度视图，半身，Bokeh，DSLR拍摄
- **🇺🇸** Women's trench coat, urban lifestyle scene, low angle view, waist shot, bokeh, shot by DSLR

---

#### 💡 **快速布光与镜头小贴士**

<div align="center">

**🎬 专业摄影技术要点**

</div>

<table>
<tr>
<th width="25%">🎯 拍摄类型</th>
<th width="40%">💡 布光方案</th>
<th width="35%">📷 镜头选择</th>
</tr>
<tr>
<td><strong>🖼️ 主图/三视图</strong></td>
<td>双侧柔光 + 顶补光</td>
<td>长焦或标准焦（避免超广角变形）</td>
</tr>
<tr>
<td><strong>🔬 微距细节</strong></td>
<td>小光圈（加景深）或焦点堆栈</td>
<td>避免镜面高光炸点</td>
</tr>
<tr>
<td><strong>🏠 生活方式</strong></td>
<td>主光45°侧前上，环境光做氛围</td>
<td>背景保持2–3级更暗或虚化</td>
</tr>
<tr>
<td><strong>🪑 家具/箱包</strong></td>
<td>避免失真</td>
<td>尽量用Telephoto Lens；空间展示可用Wide view，谨慎Ultrawide shot</td>
</tr>
</table>

**⚡ 快速检查清单**：
- ✅ 主光角度是否合适（45°侧前上）
- ✅ 背景是否虚化或保持暗调
- ✅ 镜头是否避免变形
- ✅ 高光是否控制在合理范围


---

## 💡 实用小贴士

### 🎨 色彩处理技巧
- **强调主色对比**：写入 `high contrast between subject and background`
- **颜色冲突处理**：若产品色接近背景，改用 `complementary background hue`
- **电商规范**：平台要求白底时，依 2.1 模板仅保留 `#FFFFFF` 系列

### 📸 拍摄质量提升
- **主图优化**：使用 DSLR 关键词提升专业感
- **细节展示**：善用微距和特写突出产品特色
- **氛围营造**：通过灯光和背景材质创造情绪

### ⚡ 效率优化建议
- **模板复用**：建立个人常用模板库
- **批量处理**：相似产品可复用相同参数
- **A/B测试**：对比不同参数效果选择最优方案

---

<div align="center">

**🎉 感谢使用本指南！祝您创作愉快！**

*如有问题或建议，欢迎反馈交流*

</div>

