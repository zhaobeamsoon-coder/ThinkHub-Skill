# ThinkHub Struct Coach ✦

**把模糊的产品想法锻造成 AI 可执行的结构化上下文**

给它一个想法（再模糊都行），它用苏格拉底式追问帮你想清楚，最后给你一段可以直接粘贴到 Claude / Cursor 的 Context Token。

---

## 它能做什么

| 能力 | 说明 |
|------|------|
| 结构提取 | 从模糊描述推断产品结构，不需要你填表 |
| Socratic 追问 | 找漏洞、压测、暴露矛盾——不迎合，只追问 |
| 多轮深化 | 每轮对话让结构更精确、更经得起推敲 |
| Context Token | 输出紧凑的 AI 可识别格式，立刻让 AI 理解产品背景 |
| 系统提示词 | 同时输出 Markdown 版，适合 Claude Project / Cursor Rules |

## 核心理念：9 个产品结构维度（对用户不可见）

这 9 个维度是内部思维引擎，不展示给用户，但直接影响 Context Token 的质量：

1. **problem** — 核心问题（具体到"谁在什么情况下遇到了什么"）
2. **target_user** — 目标用户（含场景和特征，越具体越好）
3. **goal** — 产品目标（可量化或可验证）
4. **constraints** — 外部限制（时间、人力、技术选型）
5. **non_goals** — 明确不做什么（防止 AI 过度设计）
6. **core_modules** — 核心功能模块（至少 3 个）
7. **user_flow** — 用户使用流程
8. **logic_rules** — 系统行为规则（内部约束）
9. **output_target** — 期望产出形态

## 安装

```bash
git clone https://github.com/your-repo/ThinkHub-Skill.git
cp -r ThinkHub-Skill ~/.claude/skills/ThinkHub
```

## 使用方式（在 Claude Code 中）

```
我想做一个帮程序员整理思路的工具
帮我梳理这个产品：一个让独立开发者和 AI 协作更高效的平台
我有个想法，一个专注于 XX 的 App
```

## 输出格式

**Context Token（紧凑版）**
```
<product-ctx title="...">
problem=...|user=...|goal=...|constraints=...|non_goals=...|modules=...|flow=...|rules=...|output=...
</product-ctx>
```

**系统提示词（Markdown 完整版）**
适合粘贴到 Claude Project Instructions 或 Cursor `.cursorrules`

## 与普通 AI 对话的区别

| | 普通 AI | ThinkHub Skill |
|--|--------|---------------|
| 对模糊想法的态度 | 迎合并扩展 | 找漏洞，逼你想清楚 |
| 输出 | 建议列表 | 可执行的结构化上下文 |
| 多轮对话目的 | 聊更多 | 让结构更精确 |
| 完成标志 | 没有 | 9 个字段全部经得起追问 |

## License: MIT
