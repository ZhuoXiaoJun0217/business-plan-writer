# StyleKit 风格速查表（离线用）

当无法访问 stylekit.top API 时使用此文件。在线环境下请优先使用 API 获取最新数据和完整 Token。

---

## 风格分类与推荐

### Modern / Tech（现代科技）

| Slug | 名称 | 最适合 | 关键词 |
|------|------|--------|--------|
| `glassmorphism` | Glassmorphism | SaaS、AI产品 | 毛玻璃、透明、模糊、层次感 |
| `liquid-glass` | Liquid Glass | 高端SaaS | 液态玻璃、流体感 |
| `neumorphism` | Neumorphism | 健康、冥想App | 软阴影、微妙深度、极简 |
| `bento-grid` | Bento Grid | 仪表盘、数据展示 | 不对称网格、卡片、Apple风格 |
| `fluent-design` | Fluent Design | Windows生态、企业软件 | 微软风格、亚克力材质 |
| `material-design` | Material Design 3 | Android生态、通用产品 | Google标准、层次阴影 |
| `linear-style` | Linear Style | 开发者工具、项目管理 | 极简、暗色、线条感 |

### Brutalist（粗野主义）

| Slug | 名称 | 最适合 | 关键词 |
|------|------|--------|--------|
| `neo-brutalist` | Neo-Brutalist | 创意作品集、独立品牌 | 粗边框、高对比、原始感 |
| `neo-brutalist-playful` | Neo-Brutalist Playful | 社交App、Z世代产品 | 粗野+活泼色彩 |
| `neo-brutalist-soft` | Neo-Brutalist Soft | 创意SaaS | 粗野主义柔化版 |
| `anti-design` | Anti-Design | 艺术项目 | 反设计、打破规则 |

### Brand-Inspired（品牌灵感）

| Slug | 名称 | 最适合 |
|------|------|--------|
| `apple-style` | Apple Style | 高端消费产品 |
| `stripe-style` | Stripe Style | 支付/金融科技 |
| `notion-style` | Notion Style | 生产力工具 |
| `github-style` | GitHub Style | 开发者平台 |
| `shopify-clean` | Shopify Clean | 电商平台 |

### Cyberpunk / Sci-Fi（赛博朋克/科幻）

| Slug | 名称 | 最适合 | 关键词 |
|------|------|--------|--------|
| `cyberpunk-neon` | Cyberpunk Neon | 游戏、Web3 | 霓虹灯、暗色背景、故障效果 |
| `neon-tokyo` | Neon Tokyo | 娱乐App | 东京夜景、霓虹 |
| `sci-fi-hud` | Sci-Fi HUD | AR/VR、军事科技 | 全息界面、扫描线 |
| `mecha` | Mecha | 机器人、工业 | 机甲风格 |
| `holographic` | Holographic | 未来概念 | 全息投影效果 |

### Japanese / Anime（日系/动漫）

| Slug | 名称 | 最适合 |
|------|------|--------|
| `ghibli-style` | Ghibli Style | 温馨内容平台 |
| `ukiyo-e` | Ukiyo-e | 文化创意 |
| `cyber-anime` | Cyber Anime | 二次元社区 |
| `pixel-anime` | Pixel Anime | 独立游戏 |

### Artistic（艺术风格）

| Slug | 名称 | 最适合 |
|------|------|--------|
| `watercolor` | Watercolor | 手工艺品牌 |
| `pop-art` | Pop Art | 潮流品牌 |
| `ink-wash` | Ink Wash | 文化/茶品牌 |
| `collage-art` | Collage Art | 创意工作室 |

### Retro / Vintage（复古）

| Slug | 名称 | 最适合 |
|------|------|--------|
| `art-deco` | Art Deco | 奢华品牌 |
| `vaporwave` | Vaporwave | 音乐/艺术 |
| `y2k` | Y2K | 千禧品牌 |
| `frutiger-aero` | Frutiger Aero | 怀旧项目 |

### Nature / Cozy（自然/舒适）

| Slug | 名称 | 最适合 |
|------|------|--------|
| `natural-organic` | Natural Organic | 环保/可持续 |
| `scandinavian` | Scandinavian | 生活方式品牌 |
| `wabi-sabi` | Wabi-Sabi | 高端设计品牌 |
| `solarpunk` | Solarpunk | 新能源/绿色科技 |
| `cottagecore` | Cottagecore | 手作/乡村品牌 |
| `zen-garden` | Zen Garden | 冥想/健康 |

### Cultural / Regional（文化/地域）

| Slug | 名称 | 最适合 |
|------|------|--------|
| `cyber-chinese` | Cyber Chinese | 国潮品牌 |
| `korean-minimal` | Korean Minimal | 时尚/美妆 |
| `islamic-geometric` | Islamic Geometric | 文化项目 |
| `dark-academia` | Dark Academia | 知识/教育 |

---

## 布局原型

| Slug | 名称 | 用途 |
|------|------|------|
| `magazine-grid` | Magazine Grid | 内容密集型 |
| `masonry-flow` | Masonry Flow | 图片展示 |
| `split-screen` | Split Screen | 双面板 |
| `parallax` | Parallax | 叙事型页面 |
| `dashboard-layout` | Dashboard Layout | 数据面板 |
| `holy-grail` | Holy Grail | 经典三栏 |
| `f-pattern` | F-Pattern | 阅读型页面 |
| `z-pattern` | Z-Pattern | 着陆页 |

---

## Token 结构速查

完整 Token 包通过 API 获取，以下是标准结构：

```json
{
  "tokens": {
    "colors": {
      "primary": {"50": "...", "500": "...", "900": "..."},
      "secondary": {},
      "accent": {},
      "neutral": {},
      "semantic": {"success": "", "warning": "", "error": "", "info": ""}
    },
    "typography": {
      "heading": {"family": "", "weight": "", "size": {}},
      "body": {"family": "", "weight": "", "size": {}}
    },
    "spacing": {"xs": "", "sm": "", "md": "", "lg": "", "xl": ""},
    "shadows": {"sm": "", "md": "", "lg": ""},
    "borders": {"radius": {"sm": "", "md": "", "lg": ""}}
  },
  "rules": {
    "do": ["...", "..."],
    "dont": ["...", "..."]
  }
}
```

## 快速项目类型映射

```
B2B SaaS      → corporate-clean / minimalist-flat
消费App       → soft-ui / glassmorphism
教育          → editorial / minimal-flat
AI/科技       → glassmorphism / cyberpunk-neon
电商          → shopify-clean / modern-gradient
社交          → neo-brutalist-playful / bento-grid
健康          → natural-organic / soft-ui
金融          → corporate-clean / dark-mode
游戏          → cyberpunk-neon / vaporwave
创意          → neo-brutalist / art-deco
环保          → natural-organic / solarpunk
文化/国潮     → cyber-chinese / ukiyo-e
```
