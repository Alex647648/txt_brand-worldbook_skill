---
name: txt_brand-worldbook_skill
description: 用于生成品牌世界观手册、品牌视觉系统、多页品牌 deck、brand book、visual guideline、art direction deck 的主 skill。只要用户提到品牌视觉手册、品牌世界观、品牌提案、品牌视觉系统、品牌设计 deck、future-facing brand、playful tech brand、创意科技品牌、多页品牌图片、brand universe、visual language exploration，就应该触发此 skill。它负责把抽象品牌定位转成统一的视觉语法、多页结构和可直接用于图像模型或设计协作的 prompts，而不是只写一段空泛风格词。
---

# 品牌世界观手册主 Skill

## 目标
把用户提供的品牌信息、产品方向、风格倾向与参考气质，转成一套**统一、可分页、可执行**的品牌世界观手册输出。

这类任务的重点不是单张图，也不是一句 slogan，而是建立一个完整的品牌宇宙：
- 品牌气质清晰
- 视觉语法统一
- 页面分工明确
- 跨触点表达一致
- 输出能直接用于图像生成、设计 brief 或提案 deck

## 适用任务
当用户要的是以下任一内容时，直接使用本 skill：
- 品牌视觉手册 / brand book / brand world / brand universe
- 多页品牌 deck / 多页品牌图像方案
- 品牌视觉系统 / visual language / art direction deck
- 创意科技品牌、时尚科技品牌、新消费品牌的世界观提案
- 要把抽象品牌定位转成多页统一视觉 prompts

如果用户要的是单张海报、单个 logo、单支剧情广告或纯文案命名，不要优先使用本 skill。

## 先做任务判断
先判断当前任务更偏哪类，再决定读哪些 reference：

1. **Brand worldbook**：完整品牌世界观手册。默认路径。
2. **Visual system exploration**：偏色彩、图形、字体、版式实验。
3. **Application deck**：偏包装、摄影、零售、跨平台应用。
4. **Brand proposal brief**：偏策略和呈现结构，而不是直接生图。

若任务以“多页、统一、世界观、视觉系统”为核心，就走 worldbook 主路径。

## 固定工作流

### Step 1：抽取输入槽
先从用户输入中提炼以下变量：
- 品牌名
- 行业 / 赛道
- 产品 / 服务类型
- 核心受众
- 价格带
- 关键词 3–5 个
- 希望的整体气质
- 页数需求（6 / 8 / 10 / 12）
- 输出形式（总 prompt / 分页 prompt / brief / 中英双语）
- 触点重点（产品 / 包装 / 摄影 / 零售 / 数字应用）

信息不全时可以合理补齐，但不要乱扩世界观。补齐逻辑应服务于统一性。

### Step 2：先定义品牌张力对
在动手写任何视觉描述前，先写出品牌的**张力对**。
格式尽量简洁，例如：
- playful ↔ premium
- future ↔ human
- artistic ↔ approachable
- experimental ↔ commercial

再写一句总锚点：
> This brand lives between X and Y.

这一步很关键，因为高级品牌通常靠两极平衡成立，而不是单一风格词堆叠。

### Step 3：建立视觉语法表
在分页之前，先定义一份简洁的视觉语法表。至少包括：
- Primary colors
- Accent colors
- Shape language
- Typography mood
- Layout rhythm
- Image treatment
- Texture / material language
- Motion / spatial feeling（如果任务涉及动态或空间）

如果视觉语法表不清晰，后续所有页面都容易漂移。

### Step 4：选择分页结构
按任务复杂度选择分页模板：
- 6 页：快速提案
- 8 页：标准版，默认优先
- 10 页：完整品牌 deck
- 12 页：重世界观、大提案、强触点覆盖

分页模板见 `references/page-structures.md`。

### Step 5：选择风格分支
根据品牌类型读取 `references/style-branches.md` 中最贴近的分支。当前默认支持：
- playful-future-consumer-tech
- luxury-creative-tech
- editorial-fashion-tech
- brutalist-digital-system
- soft-tactile-lifestyle

如果用户需求落在两个分支之间，可以混合，但必须明确主次，不要平均发力。

### Step 6：分配触点权重
品牌不是只活在 logo 上。优先判断哪些触点应被强化：
- product obsession
- visual experimentation
- packaging exploration
- editorial photography
- immersive retail
- cross-platform application

不同品牌重点不同，但默认至少覆盖其中 3 类；完整手册建议覆盖 4–6 类。

### Step 7：逐页生成
写每一页之前，先用一句话定义：
> This page exists to show ______.

然后再写这一页的 prompt / brief。这样能防止每页都变成空泛 moodboard。

### Step 8：做一致性检查
生成完成后，对照 `references/consistency-rules.md` 自查：
- 是否属于同一个品牌宇宙
- 主色与强调色是否稳定
- 图形语法是否一致
- 字体气质是否一致
- 页面间是否“变化但不跑偏”
- 是否真正可用于图像模型或设计协作

## 输出模式
默认支持四种输出：
1. **总 prompt**：一段完整 worldbook prompt
2. **分页 prompts**：多页逐页生成
3. **设计 brief**：给设计师/团队看的结构化说明
4. **中英双语版**：中文策略概述 + 英文生成 prompt

具体格式见 `references/output-formats.md`。

## 高级机制（必须内化）

### 1. 品牌张力对引擎
先定义品牌活在哪两个极之间。没有张力对，世界观容易扁平。

### 2. 视觉语法表
把抽象气质变成可视化控制项。不要只写“高级、年轻、未来感”，要落到颜色、图形、排版、摄影、材质。

### 3. 分页职责锁定
每页先定义存在理由，再写内容。这样页面才有结构，不会互相重复。

### 4. 变化-稳定比
把变量分成两类：
- **稳定的**：品牌世界观、主色逻辑、图形语法、字体语气、总体 art direction
- **变化的**：构图、场景、应用触点、物体、信息密度

目标不是所有页长得一样，而是看起来像同一个世界的不同切面。

## 何时读 reference
- 需要抽象品牌人格 / 张力对时 → 读 `references/foundations.md`
- 需要选择页数结构时 → 读 `references/page-structures.md`
- 需要风格路由时 → 读 `references/style-branches.md`
- 需要做统一性 QA 时 → 读 `references/consistency-rules.md`
- 需要确定输出模版时 → 读 `references/output-formats.md`

## 默认原则
- 先统一世界观，再写页面
- 先定义视觉语法，再写风格形容词
- 先判断触点重点，再分配页面比重
- 先保证一致性，再追求花样
- 抽象词必须落地为视觉控制项

## 不要这样做
- 不要把品牌世界观手册写成单张海报 prompt
- 不要所有页面都只重复“高级、未来、创意”这种空词
- 不要前几页 playful，后几页突然变成冷硬工业系统而无过渡
- 不要只顾 moodboard，不顾应用触点
- 不要让页面职责混乱或大面积重复

## 最终交付的最低标准
输出至少要满足：
1. 品牌核心气质可一句话概括
2. 张力对清晰
3. 视觉语法表完整
4. 页面结构明确
5. 触点覆盖合理
6. 整体看起来像同一个品牌宇宙

如果做不到这 6 条，就继续收紧，而不是继续堆词。
