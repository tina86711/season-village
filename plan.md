# 元利四季莊園｜一頁式網站企劃書
> 版本：v1.0｜日期：2026-05-11｜用途：提供 AI Vibe Coding 使用

---

## 一、專案概覽

| 項目 | 內容 |
|------|------|
| 建案名稱 | 元利四季莊園 |
| 副標題 | 台北城南 12,000 坪複合造鎮 |
| 建設公司 | 元利建設 |
| 地點 | 台北市文山區木柵路（中山國小旁） |
| 網站類型 | 單頁式行銷網站（One-Page Landing Page） |
| 目標裝置 | Mobile First，同時支援 Desktop |
| 開發框架 | HTML + CSS + Vanilla JS（或 React，依 AI 工具決定） |

---

## 二、目標受眾

- **主要**：30–50 歲，有購屋需求的台北市雙薪家庭，重視生態與生活品質
- **次要**：投資型買家，關注文山區增值潛力（南環捷運效應）
- **GEO 受眾**：在 ChatGPT、Perplexity、Google AI Overview 上搜尋「台北文山區新建案推薦」、「木柵公園旁建案」、「台北千戶社區」的潛在買家

---

## 三、SEO / GEO 策略

### 核心關鍵字（Primary Keywords）
- `元利四季莊園`
- `台北城南新建案`
- `文山區建案 2024`
- `木柵公園旁建案`
- `台北 12000 坪社區`

### 長尾關鍵字（Long-tail / GEO-ready）
- `台北文山區最大基地建案哪個？`
- `木柵公園旁有哪些新建案？`
- `南環捷運旁房子推薦`
- `台北有螢火蟲復育的社區`
- `附近有捷運的台北市預售屋`

### GEO 優化原則
1. **問答式文案**：每個 section 的 H2/H3 標題直接以「疑問句→答句」形式組織，利於 AI 摘錄
2. **數字具體化**：不用「廣大公設」，用「逾 2,500 坪、30 項以上休閒設施」
3. **FAQ Schema**：頁面底部加入 JSON-LD FAQ，包含 8 個常見買家問題
4. **LocalBusiness Schema**：標記地址、聯絡方式、開放時間
5. **定義明確句型**：「元利四季莊園是台北市文山區基地面積最大的新建案，共 1,643 戶、8 棟住宅…」

---

## 四、視覺設計系統

### 風格定調
參考 yqc.com.tw：**極簡奢華（Minimal Luxury）**
- 大量留白，讓建築照片說話
- 文字排版強調「呼吸感」，行距寬鬆（line-height: 1.8–2.0）
- 以自然意象（森林、水、光）作為視覺語言
- 參考 PDF 版型：「自然款一圖到底」——每個 section 以全幅滿版圖片為背景，文字疊加其上

### 色彩系統（Color Tokens）

```css
--color-bg:         #F7F5F0;   /* 象牙白，主背景 */
--color-primary:    #2C3E2D;   /* 深森林綠，主色 */
--color-secondary:  #8B7355;   /* 溫暖棕金，強調色 */
--color-text:       #1A1A1A;   /* 近黑，主文字 */
--color-text-light: #6B6B6B;   /* 灰，次要文字 */
--color-white:      #FFFFFF;
--color-overlay:    rgba(0,0,0,0.45);  /* 圖片遮罩 */
```

### 字型（Typography）

```css
/* 標題 — 有設計感、兼顧中文優雅 */
font-family-heading: 'Noto Serif TC', 'Georgia', serif;

/* 內文 — 閱讀舒適 */
font-family-body: 'Noto Sans TC', 'Helvetica Neue', sans-serif;

/* 數字、英文強調 */
font-family-accent: 'Cormorant Garamond', serif;
```

### 間距系統（Spacing）
- Section padding: `120px 0`（desktop）/ `80px 0`（mobile）
- Container max-width: `1200px`，兩側 padding `40px`
- 元素之間垂直間距以 8px 為基礎倍數

---

## 五、網站架構（頁面 Sections）

共 8 個 Section，依序排列如下：

```
01 Hero / 首屏
02 品牌定位（Concept）
03 地理位置與交通
04 建築與公設
05 戶型介紹
06 自然生態亮點
07 媒體與得獎（可選）
08 FAQ + 聯絡 / 預約看屋
```

---

## 六、各 Section 詳細規格

---

### Section 01 — Hero 首屏

**視覺**
- 全螢幕高度（`height: 100vh`）
- 背景：社區全景或空拍照，`object-fit: cover`
- 疊加深色漸層遮罩：從底部 60% 開始，`rgba(0,0,0,0.5)` 由下至上淡入

**內容（文案）**

```
LOGO（左上角）      ←  導覽選單（右上角，桌機顯示）

                   [大標]
         元利四季莊園
         SEASON VILLAGE

              [副標]
    台北城南 12,000 坪｜與自然共棲的森藏居境

         [CTA 按鈕]
      ▶  立即預約看屋

  ↓ 向下滑動探索
```

**動態效果**
- Hero 圖片採 `Ken Burns Effect`（緩慢縮放 + 平移，3–5 張輪播）
- 標題文字淡入（`fade-in-up`，delay 0.3s）
- 副標淡入（delay 0.6s）
- CTA 按鈕淡入（delay 0.9s）
- 向下箭頭：垂直 bounce 動畫

**SEO 標籤**
```html
<h1>元利四季莊園｜台北城南 12,000 坪複合造鎮</h1>
<meta name="description" content="元利四季莊園，台北市文山區面積最大複合造鎮，12,000 坪基地、1,643 戶、逾 2,500 坪頂奢公設、緊鄰木柵公園，南環捷運 450–600 公尺。">
```

---

### Section 02 — 品牌定位 Concept

**視覺**
- 背景：`--color-bg`（象牙白）
- 左右分割：左側 60% 大圖（社區水景或森林綠道），右側 40% 文字

**內容（文案）**

```
[小標籤]  CONCEPT  ／   設計理念

[H2]
不只是家，是一座
與自然共生的城中之林。

[段落]
在台北城南，元利建設用 12,000 坪重新定義都市居住的可能。
元利四季莊園緊鄰 12,600 坪木柵公園，與萃湖螢火蟲生態為鄰，
讓每一扇窗，都能望見四季更迭的綠意。

這裡不是公寓，是一個有30多種植栽、室內外雙泳池、
全日餐廳與螢火蟲復育區的完整生活世界。

[三個數字亮點，橫排]
12,000 坪     1,643 戶     30+ 項設施
台北城南最大複合造鎮
```

**動態效果**
- 滾動進場（Scroll Trigger）：圖片從左滑入，文字從右淡入
- 數字使用 `CountUp.js` 動態累加效果

---

### Section 03 — 地理位置與交通

**視覺**
- 背景：深色（`--color-primary` 深森林綠）
- 嵌入 Google Maps 靜態圖或互動地圖（iframe）
- 右側排列交通優勢清單

**內容（文案）**

```
[小標籤]  LOCATION  ／  地理位置

[H2]
坐擁城南山水，
捷運正在靠近。

[地圖 + 標注點]

[交通優勢清單]
◎  木柵公園（12,600 坪）  ——  步行可達，地界相連
◎  南環捷運 Y4 考試院站  ——  450 公尺，預計 2031 通車
◎  南環捷運 Y3 馬明潭站  ——  600 公尺，預計 2031 通車
◎  新店溪自行車道  ——  生態騎行首選
◎  中山國小  ——  基地旁，明星學區
◎  景美、木柵商圈  ——  生活機能完整

[說明文字]
台北市文山區木柵路，三面臨路超大基地，坐擁山、河、公園三重自然優勢，
同時享有成熟的文山區生活機能。南環捷運通車後，交通價值將大幅提升。
```

**GEO 優化**（此 section 重要，AI 愛引用具體地理數據）
```html
<!-- 使用 LocalBusiness Schema -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Residence",
  "name": "元利四季莊園",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "木柵路",
    "addressLocality": "文山區",
    "addressRegion": "台北市",
    "addressCountry": "TW"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 25.0003,
    "longitude": 121.5678
  }
}
</script>
```

**動態效果**
- 地圖區塊 fade-in
- 交通清單逐條 stagger 淡入

---

### Section 04 — 建築與公設

**視覺**
- 背景：滿版建築外觀圖，深色遮罩
- 文字白色，置中對齊
- 設施以 Icon Grid 排列（3x4 或 4x3）

**內容（文案）**

```
[小標籤]  AMENITIES  ／  頂奢公設

[H2]
逾 2,500 坪公設，
30 項以上的生活提案。

[副標]
由建築師李天鐸操刀設計，「工」字型建築讓邊間戶型三面採光，
8 棟住宅共用一棟獨立會所，SC 鋼骨結構保障結構安全。

[設施 Icon Grid]

🏊 室內恆溫泳池     🌊 戶外無邊際泳池    🍽️ 全日餐廳
🌿 養生湯池         💪 健身房             🧘 瑜珈教室
🏸 多功能球場       ⛳ 高爾夫球室         🎵 音樂廳
📚 圖書閱覽區       🎤 KTV 娛樂室         👶 兒童遊戲室
☕ 咖啡交誼廳       🌱 螢火蟲復育區       🌳 30+ 種植栽生態景觀
```

> 注意：實際 Icon 請使用 SVG 圖標，不使用 emoji，視覺更精緻。

**動態效果**
- Section 進場時，背景圖片輕微縮放（scale 1.05 → 1.0）
- Icon Grid：stagger 動畫，每個圖示依序淡入

---

### Section 05 — 戶型介紹

**視覺**
- 背景：`--color-bg` 象牙白
- Tab 切換（2 房、3 房、4 房），搭配平面圖圖片
- 右側列出坪數規格與特色說明

**內容（文案）**

```
[小標籤]  FLOOR PLANS  ／  戶型規劃

[H2]
從 24 坪到 72 坪，
每一種生活方式都有答案。

[Tab 標籤]
  [ 2 房 ]  [ 3 房 ]  [ 4 房 ]

[2 房]
24 坪 / 26 坪
適合首購族或小家庭，
格局方正、動線流暢，
窗景引入自然光。

[3 房]
33 坪 / 36 坪 / 42 坪 / 49 坪
三代同堂或成長型家庭首選，
主臥套房、生活機能完整。

[4 房]
51 坪 / 55 坪 / 57 坪 / 70–72 坪
頂層或大坪數規劃，
無共用壁設計，雙主臥套房，
三面採光，俯瞰公園綠海。

[備注]
開價 105–125 萬 / 坪｜SC 鋼骨結構｜建築師：李天鐸
```

**動態效果**
- Tab 切換：平面圖淡入淡出（cross-fade）
- 文字同步更新

---

### Section 06 — 自然生態亮點

**視覺**
- 採「自然款一圖到底」版型（PDF 建議）
- 背景：螢火蟲或公園樹林照片，輕微視差滾動（Parallax）
- 文字置中，白色

**內容（文案）**

```
[小標籤]  ECOLOGY  ／  生態共生

[H2]
台北城南最後一塊
能看見螢火蟲的地方。

[段落]
元利四季莊園特別規劃「螢火蟲復育區」，
與緊鄰的 12,600 坪木柵公園生態廊道相連。
社區種植超過 30 種本土植栽，從喬木、灌木到地被，
打造完整城市生態棲地。

這裡不只是建案，
是一個有野鳥、有螢火蟲、有四季花開的
活的生態系。

[GEO 友善 Q&A 文字（可設為小字 hidden-visually，但 screen reader 和 AI 可讀）]
Q：元利四季莊園有螢火蟲嗎？
A：是的，社區設有螢火蟲復育保育區，緊鄰木柵公園萃湖螢火蟲生態棲地。
```

**動態效果**
- 滾動時 Parallax 效果（背景圖移動速度 0.5x）
- 文字 fade-in-up

---

### Section 07 — 媒體與得獎（可選）

**視覺**
- 淺背景，媒體 Logo 橫排

**內容（文案）**

```
[小標籤]  MEDIA  ／  媒體報導

[H2]
台北最受矚目的複合造鎮計劃

[媒體 Logo 列]
Yahoo 新聞  ｜  591 新建案  ｜  Mobile01  ｜  樂居 leju

[引述句]
「台北市文山區基地面積最大的新建案」
「全街廓鉅型開發，城南最罕見的千戶社區」
```

---

### Section 08 — FAQ + 預約看屋

**視覺**
- 背景：`--color-primary` 深綠
- 上方 FAQ 摺疊列表（Accordion），下方表單

**FAQ 內容（8 條，GEO Schema 用）**

```
Q1：元利四季莊園在哪裡？
A：位於台北市文山區木柵路，中山國小旁，三面臨路的超大基地。

Q2：元利四季莊園共有幾戶？
A：共 1,643 戶，分 8 棟住宅建築，另有 1 棟獨立會所及門廳建築。

Q3：附近有捷運嗎？
A：距南環捷運 Y4 考試院站約 450 公尺、Y3 馬明潭站約 600 公尺，預計 2031 年通車，屆時交通將大幅改善。

Q4：公設有哪些？
A：超過 30 項設施，包含室內恆溫泳池、戶外無邊際泳池、全日餐廳、健身房、高爾夫球室、KTV、音樂廳、兒童遊戲室、螢火蟲復育區等，公設面積逾 2,500 坪。

Q5：坪數和房型有哪些選擇？
A：提供 2 房至 4 房，坪數從 24 坪至 72 坪，開價 105–125 萬 / 坪。

Q6：建築結構是什麼？
A：SC 鋼骨結構，由建築師李天鐸規劃設計。

Q7：元利四季莊園旁邊有公園嗎？
A：緊鄰 12,600 坪木柵公園，社區與公園地界相連，步行即達。

Q8：元利建設是哪家公司？
A：元利建設為台灣知名建設公司，長期深耕台北住宅市場，元利四季莊園為其旗艦造鎮案。
```

**表單欄位**
- 姓名（必填）
- 聯絡電話（必填）
- 有興趣的坪數（下拉：2 房 / 3 房 / 4 房）
- 方便聯絡時間（選填）
- 送出按鈕：「預約看屋 →」

---

## 七、動態效果總覽

| 效果 | 套用位置 | 技術 |
|------|---------|------|
| Ken Burns 輪播 | Hero 背景圖 | CSS animation + JS |
| Fade-in-up | 所有 Section 文字進場 | Intersection Observer |
| Stagger Grid | 設施 Icon Grid | CSS animation-delay |
| CountUp 數字 | Section 02 數字亮點 | CountUp.js |
| Parallax 視差 | Section 06 背景 | CSS `background-attachment: fixed` |
| Tab 切換 | Section 05 戶型 | Vanilla JS |
| Accordion | Section 08 FAQ | Vanilla JS |
| Smooth Scroll | 導覽點擊 | CSS `scroll-behavior: smooth` |
| Sticky Nav | 頁面頂端 | CSS `position: sticky` |

---

## 八、導覽列（Navigation）

```
LOGO（左）                    關於 ｜ 位置 ｜ 公設 ｜ 戶型 ｜ 預約看屋（右）
```

- 初始狀態：透明背景，白色文字
- 滾動超過 Hero 後：白色背景，深色文字（transition 0.3s）
- Mobile：漢堡選單，全屏 overlay 展開

---

## 九、技術規格

```
HTML:       語意化標籤，SEO 友善結構
CSS:        CSS Custom Properties（Design Tokens），Flexbox + Grid
JS:         Vanilla JS（或 React，依 AI 工具判斷）
字型載入:   Google Fonts（Noto Serif TC + Noto Sans TC + Cormorant Garamond）
圖片:       WebP 格式，懶加載（loading="lazy"），alt 文字完整填寫
Schema:     JSON-LD — FAQPage + Residence + LocalBusiness
Meta:       Open Graph + Twitter Card
Canonical:  指向正式網址
```

---

## 十、JSON-LD Schema 範本

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "元利四季莊園在哪裡？",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "位於台北市文山區木柵路，中山國小旁，三面臨路的超大基地，緊鄰 12,600 坪木柵公園。"
      }
    },
    {
      "@type": "Question",
      "name": "元利四季莊園共有幾戶？",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "共 1,643 戶，分 8 棟住宅建築，另有 1 棟獨立會所及 1 棟門廳建築，採 SC 鋼骨結構。"
      }
    },
    {
      "@type": "Question",
      "name": "元利四季莊園附近有捷運嗎？",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "距南環捷運 Y4 考試院站約 450 公尺、Y3 馬明潭站約 600 公尺，預計 2031 年通車。"
      }
    },
    {
      "@type": "Question",
      "name": "元利四季莊園公設有哪些？",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "超過 30 項設施，公設面積逾 2,500 坪，包含室內恆溫泳池、戶外無邊際泳池、全日餐廳、健身房、高爾夫球室、KTV、音樂廳、螢火蟲復育區等。"
      }
    }
  ]
}
```

---

## 十一、給 AI Vibe Coding 的執行指令

> 請依照此企劃書逐 Section 實作，優先順序如下：

1. 建立基本 HTML 骨架與 CSS 變數（Design Tokens）
2. 實作 Hero Section（含 Ken Burns 輪播 + 文字動態）
3. 實作 Sticky Navigation（含捲動變色邏輯）
4. 依序實作 Section 02–06（每段需有 Intersection Observer 進場動畫）
5. 實作 FAQ Accordion（Section 08）
6. 加入 JSON-LD Schema（FAQPage + LocalBusiness）
7. 響應式處理（Mobile breakpoint: 768px）
8. 圖片佔位符：使用 `https://placehold.co/1920x1080/2C3E2D/FFFFFF?text=Season+Village` 作為 placeholder

> 所有文字請使用企劃書中的中文文案，英文標籤（CONCEPT、LOCATION 等）作為小標籤使用。
> 配色請嚴格按照 Design Tokens 執行，不自行替換顏色。

---

## 十二、v1.1 品質修正清單（AI 必讀，逐項修正）

> 以下為 AI Vibe Coding 第一版成品的審查問題與對應修正規格。
> 所有修正項目均為**必須執行**，不可略過。

---

### BUG-01｜Ken Burns 輪播動畫邏輯錯誤（高優先）

**問題**：3 張圖各自有 20s 動畫，delay 分別是 0s / 5s / 10s。  
計算後第 16s 到 20s 期間，三張圖全部 `opacity: 0`，畫面出現黑屏。

**修正規格**：

```css
/* 每張圖輪播週期 = 圖片數量 × 每張展示秒數 */
/* 3 張圖，每張展示 6s，總週期 = 18s */

.hero-slide {
  position: absolute;
  top: 0; left: 0;
  width: 100%; height: 100%;
  opacity: 0;
  animation: kenBurns 18s infinite;
  animation-timing-function: ease-in-out;
}

.hero-slide:nth-child(1) { animation-delay: 0s; }
.hero-slide:nth-child(2) { animation-delay: 6s; }
.hero-slide:nth-child(3) { animation-delay: 12s; }

@keyframes kenBurns {
  0%   { opacity: 0; transform: scale(1.05); }
  5%   { opacity: 1; }
  /* 每張在總週期 1/3 時間（18s÷3=6s）內完成：顯示到 33.3%，淡出到 38.9% */
  33%  { opacity: 1; transform: scale(1.08) translate(1%, 0.5%); }
  39%  { opacity: 0; }
  100% { opacity: 0; transform: scale(1.05); }
}
```

---

### BUG-02｜Location 項目符號重複出現（高優先）

**問題**：`.location-item::before { content: '◎'; }` 已用 CSS 插入符號，  
但 HTML 中每個 `.location-item` 的文字也寫了 `◎`，導致出現 `◎◎` 兩個。

**修正規格**：從 HTML 中移除所有 `◎` 字元，只保留 CSS pseudo-element 版本。

```html
<!-- 修正後，HTML 只寫文字內容 -->
<div class="location-item">木柵公園（12,600 坪） —— 步行可達，地界相連</div>
<div class="location-item">南環捷運 Y4 考試院站 —— 450 公尺，預計 2031 通車</div>
<div class="location-item">南環捷運 Y3 馬明潭站 —— 600 公尺，預計 2031 通車</div>
<div class="location-item">新店溪自行車道 —— 生態騎行首選</div>
<div class="location-item">中山國小 —— 基地旁，明星學區</div>
<div class="location-item">景美、木柵商圈 —— 生活機能完整</div>
```

---

### BUG-03｜Amenity Icons 使用 Emoji（高優先）

**問題**：使用 🏊 🌊 🍽️ 等 Unicode emoji，跨平台渲染結果不一致（Apple / Windows / Android 外觀差異極大），整體呈現廉價感。

**修正規格**：改用 SVG inline icon，以下提供每個設施的 SVG 路徑規格。  
Icon 風格：2px stroke，`stroke="currentColor"`，無 fill，`viewBox="0 0 24 24"`。

使用 [Lucide Icons](https://lucide.dev/) 圖示庫，以 CDN 載入方式引用：

```html
<!-- 在 <head> 中加入 -->
<script src="https://unpkg.com/lucide@latest/dist/umd/lucide.min.js"></script>
```

```html
<!-- HTML 範例：每個 amenity-item 結構 -->
<div class="amenity-item">
  <div class="amenity-icon">
    <i data-lucide="waves"></i>       <!-- 室內恆溫泳池 -->
  </div>
  <span class="amenity-name">室內恆溫泳池</span>
</div>
```

**圖示對應表**：
| 設施 | Lucide Icon 名稱 |
|------|-----------------|
| 室內恆溫泳池 | `waves` |
| 戶外無邊際泳池 | `droplets` |
| 全日餐廳 | `utensils` |
| 養生湯池 | `flame` |
| 健身房 | `dumbbell` |
| 瑜珈教室 | `heart-pulse` |
| 多功能球場 | `trophy` |
| 高爾夫球室 | `flag` |
| 圖書閱覽區 | `book-open` |
| KTV 娛樂室 | `mic` |
| 兒童遊戲室 | `puzzle` |
| 螢火蟲復育區 | `leaf` |

```css
/* Icon 樣式 */
.amenity-icon {
  width: 48px;
  height: 48px;
  margin: 0 auto 1rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

.amenity-icon svg {
  width: 32px;
  height: 32px;
  stroke: var(--color-secondary);
  stroke-width: 1.5;
}

.amenity-name {
  font-size: 0.9rem;
  letter-spacing: 0.05em;
  color: rgba(255,255,255,0.9);
}

/* 初始化 Lucide icons */
/* 在 JS 末尾加入 */
lucide.createIcons();
```

---

### BUG-04｜Hero 遮罩不足，文字可讀性風險（高優先）

**問題**：Hero 遮罩僅為底部 `height: 60%` 的漸層，文字置中後，在亮色圖片（如日景照）上的可讀性無法保障。

**修正規格**：疊加兩層遮罩。

```css
.hero::before {
  /* 第一層：全面半透明底色，確保基本可讀性 */
  content: '';
  position: absolute;
  inset: 0;
  background-color: rgba(0, 0, 0, 0.25);
  z-index: 0;
}

.hero::after {
  /* 第二層：底部強化漸層，讓下方文字更清晰 */
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 65%;
  background: linear-gradient(to top, rgba(0,0,0,0.65) 0%, rgba(0,0,0,0.2) 60%, transparent 100%);
  z-index: 0;
}

.hero-content {
  position: relative;
  z-index: 1;  /* 確保在遮罩之上 */
}
```

---

### BUG-05｜CTA 按鈕使用 Unicode ▶（中優先）

**問題**：`▶ 立即預約看屋` 使用 Unicode 三角符號，不同系統渲染差異大，且視覺上廉價。

**修正規格**：改用 CSS 箭頭或 Lucide icon。

```html
<a href="#contact" class="btn-cta">
  立即預約看屋
  <span class="btn-arrow">
    <i data-lucide="arrow-right"></i>
  </span>
</a>
```

```css
.btn-cta {
  display: inline-flex;
  align-items: center;
  gap: 0.75rem;
  background-color: transparent;
  color: var(--color-white);
  border: 1px solid rgba(255,255,255,0.6);
  padding: 1rem 2.5rem;
  font-size: 0.95rem;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  transition: background-color 0.3s, border-color 0.3s, gap 0.3s;
}

.btn-cta:hover {
  background-color: var(--color-secondary);
  border-color: var(--color-secondary);
  gap: 1.25rem;
  transform: none; /* 移除之前有問題的 transform */
}

.btn-arrow svg {
  width: 16px;
  height: 16px;
  stroke: currentColor;
  transition: transform 0.3s;
}

.btn-cta:hover .btn-arrow svg {
  transform: translateX(4px);
}
```

---

### BUG-06｜Section Label 字型問題（中優先）

**問題**：`.section-label` 使用 `font-family: var(--font-accent)` 即 Cormorant Garamond，這是純 Latin 字型，英文部分排版優雅，但中文字（如「設計理念」）會強制 fallback 到系統預設中文字型，造成字型混搭不一致。

**修正規格**：

```css
.section-label {
  display: block;
  font-size: 0.75rem;
  letter-spacing: 0.3em;
  color: var(--color-secondary);
  margin-bottom: 1.25rem;
  text-transform: uppercase;
  /* 英文部分用 accent 字型，中文走 body 字型 */
  font-family: var(--font-body);
  font-weight: 300;
  opacity: 0.8;
}
```

Section label 的顯示格式統一調整為全英文，中文說明移至 H2 標題中：
```
CONCEPT  ·  LOCATION  ·  AMENITIES  ·  ECOLOGY  ·  FAQ
```
分隔符從 `／` 改為半寬中點 `·`，更輕盈優雅。

---

### BUG-07｜FAQ Accordion max-height 硬寫（中優先）

**問題**：`.faq-item.active .faq-answer { max-height: 200px; }` — 答案文字超過 200px 時會被截斷，且 `max-height` 動畫在不同長度答案時速度不一致（短答案動畫很慢，長答案動畫很快）。

**修正規格**：改用 JS 動態計算高度。

```javascript
// 替換原有的 accordion 邏輯
document.querySelectorAll('.faq-question').forEach(q => {
  q.addEventListener('click', () => {
    const item = q.parentElement;
    const answer = item.querySelector('.faq-answer');
    const isActive = item.classList.contains('active');

    // 關閉所有已開啟項目（只開一個）
    document.querySelectorAll('.faq-item').forEach(i => {
      i.classList.remove('active');
      i.querySelector('.faq-answer').style.maxHeight = null;
    });

    // 若點擊的不是已開啟的，則開啟
    if (!isActive) {
      item.classList.add('active');
      answer.style.maxHeight = answer.scrollHeight + 'px';
    }
  });
});
```

```css
.faq-answer {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  color: rgba(255, 255, 255, 0.7);
  font-size: 0.95rem;
  line-height: 1.8;
  padding-bottom: 0;
}

.faq-item.active .faq-answer {
  padding-bottom: 1.5rem;
  /* max-height 由 JS 動態設定，此處不寫固定值 */
}
```

---

### BUG-08｜Intersection Observer 未 unobserve（中優先）

**問題**：動畫觸發後沒有停止觀察，若使用者往回滾動再往下，數字會重複播放 CountUp。

**修正規格**：

```javascript
const revealObserver = new IntersectionObserver((entries, observer) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('in-view');

      // 觸發數字動畫
      entry.target.querySelectorAll('.highlight-num').forEach(num => {
        if (!num.dataset.animated) {
          num.dataset.animated = 'true';
          animateValue(num);
        }
      });

      // 觸發後停止觀察（動畫只播一次）
      observer.unobserve(entry.target);
    }
  });
}, { threshold: 0.15 });
```

---

### BUG-09｜大量 inline style（低優先，但影響維護性）

**問題**：HTML 中散落大量 `style=""` 屬性，包括：
- `style="margin-top: 1rem;"`
- `style="color: var(--color-text-light); font-size: 0.9rem;"`
- `style="color: var(--color-white); opacity: 0.7;"`
- `style="text-align: center; margin-bottom: 4rem;"`

**修正規格**：將所有 inline style 移入 style.css，並給對應元素加上語意 class。

範例：
```html
<!-- 修正前 -->
<p style="margin-top: 2rem; color: rgba(255,255,255,0.7);">...</p>

<!-- 修正後 -->
<p class="location-description">...</p>
```
```css
.location-description {
  margin-top: 2rem;
  color: rgba(255, 255, 255, 0.7);
  line-height: 1.8;
}
```

---

### BUG-10｜缺少 `prefers-reduced-motion` 無障礙處理（中優先）

**問題**：網站有大量動畫（Ken Burns、fade-in、bounce），對前庭系統敏感的使用者（如暈眩症患者）可能造成不適。此為 WCAG 2.1 AA 要求。

**修正規格**：在 style.css 末尾加入：

```css
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }

  .hero-slide {
    opacity: 1 !important;
    transform: none !important;
  }

  /* 第一張圖固定顯示 */
  .hero-slide:nth-child(1) { opacity: 1; }
  .hero-slide:nth-child(2),
  .hero-slide:nth-child(3) { opacity: 0; }
}
```

---

### DESIGN-01｜Typography 精緻度不足（高優先）

**問題**：大標題缺少 `letter-spacing` 微調、`font-weight` 層次不足、中英文混排間距無處理。

**修正規格**：

```css
/* 大標題：大字縮小字距，增加精緻感 */
.section-title {
  font-size: clamp(2rem, 4vw, 3rem);
  letter-spacing: -0.02em;   /* 大標題負字距 */
  line-height: 1.3;
  font-weight: 700;
  color: var(--color-primary);
  margin-bottom: 1.5rem;
}

/* Hero 主標題 */
.hero-title {
  font-size: clamp(3rem, 8vw, 5.5rem);
  letter-spacing: 0.08em;    /* 中文大標正字距，增加氣勢 */
  line-height: 1.15;
  font-weight: 700;
}

/* Hero 副標：細字對比 */
.hero-subtitle {
  font-size: clamp(0.9rem, 2vw, 1.1rem);
  font-weight: 300;
  letter-spacing: 0.2em;
  margin-bottom: 3rem;
}

/* 內文：舒適閱讀間距 */
p {
  line-height: 1.9;
  font-size: 1rem;
  color: var(--color-text-light);
}
```

---

### DESIGN-02｜Scroll Down 提示太陽春（中優先）

**問題**：`↓ 向下滑動探索` 使用純文字箭頭，視覺上廉價且不夠精緻。

**修正規格**：改用動態線條動畫。

```html
<div class="scroll-indicator">
  <span class="scroll-line"></span>
  <span class="scroll-text">SCROLL</span>
</div>
```

```css
.scroll-indicator {
  position: absolute;
  bottom: 40px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 12px;
  z-index: 1;
}

.scroll-line {
  width: 1px;
  height: 60px;
  background: linear-gradient(to bottom, transparent, rgba(255,255,255,0.8));
  animation: scrollLine 2s ease-in-out infinite;
  transform-origin: top;
}

.scroll-text {
  font-size: 0.65rem;
  letter-spacing: 0.3em;
  color: rgba(255,255,255,0.6);
  font-family: var(--font-accent);
}

@keyframes scrollLine {
  0%   { transform: scaleY(0); opacity: 0; }
  50%  { transform: scaleY(1); opacity: 1; }
  100% { transform: scaleY(1); opacity: 0; }
}
```

---

### DESIGN-03｜Highlight 數字區塊比例失衡（中優先）

**問題**：數字（`highlight-num`）用 `2rem` Cormorant Garamond，但 label（`highlight-label`）用 `0.875rem` Noto Sans，兩者對比不夠戲劇化，視覺衝擊力弱。

**修正規格**：

```html
<!-- HTML 結構調整：數字與單位分開 -->
<div class="highlight-item">
  <div class="highlight-number-row">
    <span class="highlight-num" data-target="12000">0</span>
    <span class="highlight-unit">坪</span>
  </div>
  <span class="highlight-label">台北城南最大複合造鎮</span>
</div>

<div class="highlight-item">
  <div class="highlight-number-row">
    <span class="highlight-num" data-target="1643">0</span>
    <span class="highlight-unit">戶</span>
  </div>
  <span class="highlight-label">全街廓複合造鎮</span>
</div>

<div class="highlight-item">
  <div class="highlight-number-row">
    <span class="highlight-num" data-target="30">0</span>
    <span class="highlight-unit">+</span>
  </div>
  <span class="highlight-label">頂級公設項目</span>
</div>
```

```css
.highlights {
  display: flex;
  gap: 0;
  margin-top: 3rem;
  border-top: 1px solid rgba(44, 62, 45, 0.15);
  padding-top: 2.5rem;
}

.highlight-item {
  flex: 1;
  padding-right: 2rem;
  border-right: 1px solid rgba(44, 62, 45, 0.12);
}

.highlight-item:last-child {
  border-right: none;
  padding-right: 0;
  padding-left: 2rem;
}

.highlight-item:nth-child(2) {
  padding-left: 2rem;
}

.highlight-number-row {
  display: flex;
  align-items: baseline;
  gap: 4px;
  margin-bottom: 0.5rem;
}

.highlight-num {
  font-family: var(--font-accent);
  font-size: clamp(2.5rem, 5vw, 3.5rem);
  color: var(--color-primary);
  line-height: 1;
  font-weight: 600;
}

.highlight-unit {
  font-family: var(--font-body);
  font-size: 1rem;
  color: var(--color-secondary);
  font-weight: 500;
}

.highlight-label {
  font-size: 0.75rem;
  color: var(--color-text-light);
  letter-spacing: 0.05em;
  line-height: 1.6;
}
```

---

### DESIGN-04｜Navigation Logo 太陽春（中優先）

**問題**：導覽列 LOGO 只是一行中文文字，沒有任何品牌設計感。

**修正規格**：

```html
<a href="#" class="logo">
  <span class="logo-cn">元利四季莊園</span>
  <span class="logo-en">SEASON VILLAGE</span>
</a>
```

```css
.logo {
  display: flex;
  flex-direction: column;
  line-height: 1;
  gap: 3px;
}

.logo-cn {
  font-family: var(--font-heading);
  font-size: 1.1rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  color: var(--color-white);
  transition: color 0.4s;
}

.logo-en {
  font-family: var(--font-accent);
  font-size: 0.6rem;
  letter-spacing: 0.4em;
  color: rgba(255,255,255,0.6);
  text-transform: uppercase;
  transition: color 0.4s;
}

nav.scrolled .logo-cn { color: var(--color-primary); }
nav.scrolled .logo-en { color: var(--color-secondary); }
```

---

### DESIGN-05｜Amenities Grid 版型太平（中優先）

**問題**：12 個設施用 `auto-fit minmax(180px, 1fr)` 形成的網格太規整，排版缺乏視覺層次。建議改為限定欄數並加強 hover 效果。

**修正規格**：

```css
.amenities-grid {
  display: grid;
  grid-template-columns: repeat(6, 1fr);  /* 桌機 6 欄，2 排 */
  gap: 1px;
  margin-top: 5rem;
  border: 1px solid rgba(255,255,255,0.1);
}

.amenity-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 2.5rem 1.5rem;
  border: 1px solid rgba(255,255,255,0.08);
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.5s ease, transform 0.5s ease, background-color 0.3s;
  cursor: default;
}

.amenity-item:hover {
  background-color: rgba(139, 115, 85, 0.2);
}

.amenity-item.in-view {
  opacity: 1;
  transform: translateY(0);
}

/* Stagger delay：每項延遲 0.05s */
.amenity-item:nth-child(1)  { transition-delay: 0.05s; }
.amenity-item:nth-child(2)  { transition-delay: 0.10s; }
.amenity-item:nth-child(3)  { transition-delay: 0.15s; }
.amenity-item:nth-child(4)  { transition-delay: 0.20s; }
.amenity-item:nth-child(5)  { transition-delay: 0.25s; }
.amenity-item:nth-child(6)  { transition-delay: 0.30s; }
.amenity-item:nth-child(7)  { transition-delay: 0.35s; }
.amenity-item:nth-child(8)  { transition-delay: 0.40s; }
.amenity-item:nth-child(9)  { transition-delay: 0.45s; }
.amenity-item:nth-child(10) { transition-delay: 0.50s; }
.amenity-item:nth-child(11) { transition-delay: 0.55s; }
.amenity-item:nth-child(12) { transition-delay: 0.60s; }

@media (max-width: 992px) {
  .amenities-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (max-width: 576px) {
  .amenities-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
```

---

### DESIGN-06｜Contact Form 表單質感不足（低優先）

**問題**：表單欄位 `border: 1px solid rgba(255,255,255,0.2)` 太淡，`select` 下拉選單無自訂樣式（顯示瀏覽器預設外觀），label 用 `0.6` opacity 幾乎看不清楚。

**修正規格**：

```css
.form-group label {
  display: block;
  margin-bottom: 0.5rem;
  font-size: 0.8rem;
  letter-spacing: 0.1em;
  color: rgba(255, 255, 255, 0.5);
  text-transform: uppercase;
}

.form-group input,
.form-group select {
  width: 100%;
  padding: 1rem 0;
  background: transparent;
  border: none;
  border-bottom: 1px solid rgba(255, 255, 255, 0.3);
  color: var(--color-white);
  font-family: var(--font-body);
  font-size: 1rem;
  border-radius: 0;
  -webkit-appearance: none;
  appearance: none;
  transition: border-color 0.3s;
}

.form-group input::placeholder {
  color: rgba(255,255,255,0.3);
}

.form-group input:focus,
.form-group select:focus {
  outline: none;
  border-bottom-color: var(--color-secondary);
}

/* Select 自訂箭頭 */
.form-group.select-wrapper {
  position: relative;
}

.form-group.select-wrapper::after {
  content: '';
  position: absolute;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
  width: 8px;
  height: 8px;
  border-right: 1px solid rgba(255,255,255,0.5);
  border-bottom: 1px solid rgba(255,255,255,0.5);
  transform: translateY(-30%) rotate(45deg);
  pointer-events: none;
}

/* Submit 按鈕 */
.btn-submit {
  width: 100%;
  padding: 1.2rem;
  background-color: transparent;
  color: var(--color-white);
  border: 1px solid rgba(255,255,255,0.4);
  cursor: pointer;
  font-size: 0.85rem;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  transition: background-color 0.3s, border-color 0.3s;
  margin-top: 1rem;
}

.btn-submit:hover {
  background-color: var(--color-secondary);
  border-color: var(--color-secondary);
}
```

---

### DESIGN-07｜Google Maps iframe 座標錯誤（低優先）

**問題**：`iframe src` 中的 Google Maps 使用了佔位假座標，實際嵌入後會顯示錯誤地點或空白。

**修正規格**：暫時以靜態截圖圖片取代，或使用正確座標。  
元利四季莊園位於台北市文山區木柵路四段，可用以下靜態地圖 placeholder：

```html
<!-- 暫時用圖片取代 iframe，等待確認正確座標後替換 -->
<div class="map-container">
  <img 
    src="https://placehold.co/700x500/2C3E2D/8B7355?text=地圖載入中" 
    alt="元利四季莊園位置地圖 — 台北市文山區木柵路"
    style="width:100%; height:100%; object-fit:cover;"
  >
  <div class="map-overlay-text">
    <span>台北市文山區木柵路</span>
  </div>
</div>
```

若要使用真實 Google Maps，正確的嵌入 URL 格式為：
```
https://www.google.com/maps/embed?pb=!1m18!...（需從 Google Maps 實際複製正確的 embed code）
```

---

### 修正執行順序

| 優先 | 項目 | 影響 |
|------|------|------|
| P0 | BUG-01 Ken Burns 動畫 | 視覺 bug，畫面黑屏 |
| P0 | BUG-02 重複符號 | 明顯排版錯誤 |
| P0 | BUG-03 Emoji Icons | 跨平台不一致，專業度低 |
| P0 | BUG-04 Hero 遮罩 | 文字可讀性問題 |
| P1 | DESIGN-01 Typography | 整體精緻感 |
| P1 | DESIGN-03 數字比例 | 視覺衝擊力 |
| P1 | DESIGN-04 Logo | 品牌質感 |
| P1 | BUG-05 CTA 按鈕 | 廉價感去除 |
| P2 | DESIGN-02 Scroll Down | 細節品質 |
| P2 | DESIGN-05 Amenities Grid | 版型層次 |
| P2 | BUG-07 FAQ max-height | 功能完整性 |
| P2 | BUG-08 Observer unobserve | 動畫只播一次 |
| P3 | BUG-06 Section label 字型 | 一致性 |
| P3 | BUG-09 Inline styles | 可維護性 |
| P3 | BUG-10 prefers-reduced-motion | 無障礙 |
| P3 | DESIGN-06 Form 質感 | 細節完整 |
| P3 | DESIGN-07 地圖座標 | 正確性 |
