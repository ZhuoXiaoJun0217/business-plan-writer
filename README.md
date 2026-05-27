# CUPL-business-plan-writer

中国政法大学学生专用创业计划书撰写 Skill —— 端到端引导完成一份专业、学术规范的创业计划书。

## v2.0 架构

```
Pre-flight → 软依赖自动检测与安装
Step 0    → 加载规范文件（或双标杆模板）
Step 1    → 项目定位 + 头脑风暴（superpowers:brainstorming）
Step 1.5  → 设计风格选择（StyleKit 120+ 风格）
Step 2    → 产品打磨 + 数据调研（分析即调研，AI 维护调研记忆）
Step 3    → 技术方案（三引擎协作：superpowers + gstack + mattpocock）
Step 4    → 撰写输出（对标学习 → 逐章撰写 → HTML 生成 → 去AI痕迹）
Step 5    → 质量检查（答题板核查 + 深度审计 + 评分量规）
Step 6    → 路演答辩（PPT大纲 + 答辩陈词 + 常见问题预演）
```

## 核心特性

- **分析即调研：** 数据搜索嵌入每个分析模块，分析同时产出数据存入 AI 维护的调研记忆系统（[数据点]/[学术文献]/[产品决策] 三区）
- **双标杆体系：** 路演对标（YC Pitch Deck）+ 完整计划书对标（SEC S-1 + 中国互联网企业上市文件）
- **对标学习机制：** Step 4.0 要求 AI 撰写前搜索精读 3+ 标杆，写完后对标检查
- **六步结构化工作流：** 从定位到答辩，每步有数据闸门和检查点
- **20+ pm-skills 集成：** JTBD、TAM/SAM/SOM、PESTEL、用户画像、竞争分析、定价策略、获客渠道、路线图规划等
- **三引擎协作：** superpowers（流程管控）+ gstack（工程评审）+ mattpocock（代码品质）
- **Step Pre-flight：** 一次性检测并安装 7 类软依赖技能
- **GB/T 7714 学术引用：** 支持顺序编码制和脚注制（法大格式）
- **StyleKit 设计风格：** 120+ 风格可选，生成带品牌 Token 的 HTML 计划书
- **中文去 AI 痕迹：** humanizer-zh + 12 条专项规则——破折号限制、水词删除、句式多样化、段落结构变化、语调分章节校准
- **打印友好 HTML：** A4 纸张、页眉页脚、图表编号、目录锚点、响应式设计

## 质量标杆

全部公开可检索、可逐章学习，不引用无法验证的竞赛案例：

**SEC S-1 招股书（YC 投资组合 + 科技巨头）：**
Airbnb (YC W09) · DoorDash (YC S13) · Alibaba · Google · Uber

**中国互联网企业上市文件：**
美团 2018 香港 IPO · 京东 2014 NASDAQ · 拼多多 2018 NASDAQ · 小米 2018 港交所

## 安装

### 方式一：通过插件市场

```bash
claude /plugin add-marketplace https://github.com/ZhuoXiaoJun0217/business-plan-writer
claude /plugin install business-plan-writer@business-plan-writer-marketplace
```

### 方式二：手动安装

在 `~/.claude/settings.json` 的 `extraKnownMarketplaces` 中添加：

```json
{
  "extraKnownMarketplaces": {
    "business-plan-writer-marketplace": {
      "source": {
        "source": "url",
        "url": "https://github.com/ZhuoXiaoJun0217/business-plan-writer.git"
      }
    }
  }
}
```

## 使用

```
帮我写一份创业计划书，我的项目是"xxx"
```

Skill 自动激活，引导完成 Pre-flight → Step 6 完整流程。

## 文件结构

```
CUPL-business-plan-writer/
├── SKILL.md                           # 主文件（1371行）
├── references/
│   ├── product-analysis-playbook.md   # 20+技能调用表、定价/获客内置框架
│   ├── three-engine-workflow.md       # 三引擎五阶段详细流程 + 安全门禁
│   ├── deai-rules.md                  # 12条中文去AI痕迹规则 + 质量检查表
│   ├── pitch-guide.md                 # 路演PPT结构、答辩陈词、常见问题预演
│   ├── stylekit-styles.md             # 120+ 设计风格速查表
│   ├── gbt7714-format.md              # GB/T 7714 引用格式及示例
│   └── cupl-thesis-format.md          # 中国政法大学论文格式规范
└── README.md
```

## 软依赖

| 技能 | 用途 | 安装方式 |
|------|------|---------|
| pm-skills | 产品分析与市场调研（~20个技能） | `npm install -g pm-skills` |
| gstack | 架构评审、浏览器测试、CEO审查 | `git clone` + `./setup` |
| superpowers | 脑暴、TDD、验证、并行调度 | `npm install -g superpowers-cli` |
| mattpocock-skills | 原型、TDD、架构、诊断 | `git clone` |
| stylekit | 120+设计风格库 | WebFetch stylekit.top |
| ui-ux-pro-max | HTML视觉品质提升 | `git clone` |
| humanizer-zh | 中文去AI痕迹 | 随 superpowers 安装 |

所有软依赖缺失时均有内置降级方案，不阻塞工作流。

## 许可证

MIT
