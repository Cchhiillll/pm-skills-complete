---
name: pm-skills-complete
description: PM Skills 全家桶 - 基于 Dean Peters 的 Product-Manager-Skills 仓库。当用户提出产品相关任务时，自动分析需求并选择合适的 PM 方法论 skill 进行处理。覆盖问题定义、优先级排序、用户研究、PRD 开发、路线图规划等常用 PM 工作流。
metadata:
  {
    "openclaw": {
      "emoji": "🧭",
      "requires": { "bins": ["git"] }
    }
  }
---

# PM Skills Complete

这是一个 **PM 技能全家桶**，当用户提出任何产品经理相关的工作任务时，你应该**自动分析需求并选择最合适的 skill** 来处理。

## 核心原则

1. **不要等用户指定用哪个 skill** - 用户说"帮我分析一下这个问题"，你应该自己去判断用 problem-framing-canvas
2. **先理解用户真正的问题** - 如果用户说的不清楚，先追问
3. **一次只用最相关的一个 skill** - 不要一下子上来跑三四个
4. **按 skill 模板输出** - 每个 skill 都有固定的 Output 格式，照着输出

## 这个全家桶能做什么

| 用户可能的诉求 | 对应的能力 |
|----------------|------------|
| 选哪个优先级框架好 | 自动推荐合适的优先级框架（RICE/ICE/KANO/MOSCOW 等） |
| 帮我定义/分析一个问题 | 问题分析框架（根因、影响、解决方案） |
| 怎么做用户研究/访谈 | 访谈准备、客户旅程地图、JTBD |
| 帮我写 PRD | PRD 文档模板与结构 |
| 怎么拆需求/史诗 | Epic 拆分、用户故事、故事地图 |
| 怎么规划路线图 | 路线图规划模板 |
| 帮我做个新闻稿/上市材料 | 新闻稿、Launch 模板 |
| 这个功能怎么优先级排序 | 评分矩阵、投资建议 |
| 市场规模/商业分析 | TAM/SAM/SOM、商业健康指标 |
| 团队/战略相关 | 战略对齐、入职手册 |

## 上游仓库

**必须读取的 skill 仓库：**

```
/Users/wangyipeng/.openclaw/workspace/pm-skills-repo/skills/
```

**Commands 工作流：**

```
/Users/wangyipeng/.openclaw/workspace/pm-skills-repo/commands/
```

## 你的工作流程

当用户提出任何 PM 相关任务时，按以下步骤：

### 步骤 1：理解任务

先问自己：
- 用户真正想解决什么问题？
- 这个任务属于哪个阶段（发现/验证/规划/上线）？
- 用户需要的是模板、方法论、还是具体方案？

### 步骤 2：匹配 Skill

根据任务类型自动选择最合适的 skill：

| 任务特征 | 推荐 skill |
|----------|------------|
| "选哪个框架好"、"怎么排序" | prioritization-advisor |
| "分析问题"、"是什么问题" | problem-framing-canvas |
| "怎么做访谈"、"了解用户" | discovery-interview-prep / customer-journey-map |
| "写 PRD"、"需求文档" | prd-development |
| "拆史诗"、"拆故事" | epic-breakdown-advisor / user-story-splitting |
| "规划路线图" | roadmap-planning |
| "怎么做新闻稿" | press-release |
| "市场规模"、"商业分析" | tam-sam-som-calculator / business-health-diagnostic |
| "用户想要什么"、" Jobs to be done" | jobs-to-be-done |
| "产品战略"、"方向" | product-strategy-session |
| "团队入职"、" VP 准备" | executive-onboarding-playbook |

如果不确定，先读一下对应 skill 的描述再决定。

### 步骤 3：执行 Skill

1. 读取对应的 skill 文件
2. 按照其中的交互流程与用户对话（通常会问 3-5 个问题）
3. 按照 Output 格式输出结构化结果

### 步骤 4：输出与下一步

- 输出结构化建议
- 告诉用户如果需要继续下一步可以做什么（比如"需要我帮你拆成史诗吗？"）

## 常见用户表述与你的响应

| 用户说... | 你应该... |
|-----------|-----------|
| "帮我看看这个功能要不要做" | 自动调用 prioritization-advisor 或 feature-investment-advisor |
| "我不知道用户想要什么" | 自动调用 jobs-to-be-done 或 customer-journey-map |
| "需求太多了不知道怎么排" | 自动调用 prioritization-advisor |
| "帮我写个 PRD" | 自动调用 prd-development |
| "这个需求怎么拆" | 自动调用 epic-breakdown-advisor 或 user-story-splitting |
| "怎么做用户访谈" | 自动调用 discovery-interview-prep |
| "帮我规划一下明年" | 自动调用 roadmap-planning |
| "这个功能怎么写新闻稿" | 自动调用 press-release |
| "我们的产品健康吗" | 自动调用 business-health-diagnostic |
| "市场规模多大" | 自动调用 tam-sam-som-calculator |

## 重要提示

- **不要让用户选 skill** - 你要根据他的描述自动判断
- **不要一次加载所有 skills** - 用户说一个任务，你读一个 skill 来处理
- **如果没找到对应的 skill** - 告诉用户这个领域暂不支持，可以尝试换一种表述
- **输出要结构化** - 按照 skill 模板的 Output 部分来组织你的回复

## 快速索引（供你参考）

```
skills/prioritization-advisor/          # 优先级框架选择
skills/problem-framing-canvas/           # 问题分析
skills/prd-development/                  # PRD 撰写
skills/user-story/                       # 用户故事
skills/user-story-mapping/               # 故事地图
skills/customer-journey-map/             # 客户旅程
skills/jobs-to-be-done/                 # JTBD
skills/epic-breakdown-advisor/           # Epic 拆分
skills/roadmap-planning/                 # 路线图
skills/press-release/                    # 新闻稿
skills/opportunity-solution-tree/        # 机会解决方案树
skills/lean-ux-canvas/                  # 精益画布
skills/business-health-diagnostic/        # 商业健康
skills/tam-sam-som-calculator/          # 市场规模
skills/discovery-interview-prep/         # 访谈准备

commands/discover.md                     # 发现流程
commands/validate.md                     # 验证流程
commands/plan.md                        # 规划流程
commands/launch.md                      # 上线流程
```

---

**记住：** 当用户提出任何 PM 相关任务时，你的职责是**自动分析并选择最合适的 skill**，而不是让用户自己去挑选。
