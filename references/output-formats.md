# Output Formats

默认支持 4 类输出。根据用户需求选一种或组合。

## 1. 总 prompt
适合快速探索。

### 结构
1. 一句话概述
2. 品牌张力对
3. 视觉语法表（简版）
4. 多页整体描述
5. 风格锚点

---

## 2. 分页 prompts
适合真正做多页生成。

### 建议格式
- Page 1 — [title]
  - This page exists to show ...
  - Prompt: ...

- Page 2 — [title]
  - This page exists to show ...
  - Prompt: ...

每页 prompt 应继承同一个品牌世界观，不要各写各的。

---

## 3. 设计 brief
适合给设计师、团队或提案流程使用。

### 建议结构
- Project summary
- Brand tension pair
- Visual language
- Priority touchpoints
- Recommended page structure
- Art direction notes
- Risks to avoid

---

## 4. 中英双语版
适合中文策略 + 英文生图并行。

### 建议结构
- 中文：品牌概述、张力对、视觉系统、分页思路
- 英文：可直接投喂的总 prompt 或分页 prompt

---

## 输出优先级建议
- 用户说“先给我一版能喂模型的” → 总 prompt 或分页 prompts
- 用户说“帮我梳理整套方案” → 设计 brief 或中英双语版
- 用户说“我要做多张品牌手册图” → 分页 prompts

---

## 最低质量要求
无论选哪种格式，输出里都应至少出现：
- 品牌张力对
- 视觉语法
- 明确结构
- 一致性控制意识
