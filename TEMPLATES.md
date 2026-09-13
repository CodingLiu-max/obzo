# Knowledge-base templates

Adapt names to the existing vault. Do not create every optional folder by default.

## Minimal learning system

```text
Topic/
  学习里途.md
  相关论文/
    Model-Year-Venue.md
  推导笔记/
```

Optional only when needed:

```text
  00_主题索引.md
  实践笔记/
  术语与问题.md
  检索记录.md
```

## Minimal engineering system

```text
Project-or-Topic/
  工程路线.md
  相关论文/
  实验记录/
```

Optional only when needed:

```text
  00_工程索引.md
  理论与推导/
  数据与评测.md
  决策记录.md
  检索记录.md
```

## Learning route note

```markdown
---
entity: learning-route
topic: "[topic]"
audience: "[audience]"
goal: "[observable outcome]"
scope_include: []
scope_exclude: []
paper_budget: 12
route_status: active
last_reviewed: YYYY-MM-DD
---

# [Topic] 学习里途

## 完成标准

[What the learner can explain, derive, implement, or evaluate.]

## 路线 1：[Node]

- 为什么学：[motivation]
- 前置知识：[links]
- 核心论文：[[相关论文/Model-Year-Venue|Model（Venue Year）]]：一句话说明该论文在路线中的作用。
- 推导/实践：[[推导笔记/Note]]
- 常见误区：[boundary or confusion]
- 通过标准：[self-check or artifact]

## 分支比较与开放问题

- [comparison]
- [contradiction]
- [open question]

## 可选阅读

[Relevant but non-core papers, with inclusion reason.]
```

## Engineering route note

```markdown
---
entity: engineering-route
goal: "[deliverable]"
constraints: []
datasets: []
metrics: []
route_status: design
---

# [Project] 工程路线

## 问题与验收标准

## 权威依据与最近工作

## 数据、指标和统一协议

## 方法模块与接口

## 实现里程碑

## 基线与消融

## 风险、失败判据和停止条件

## 实验记录
```

## Canonical paper note

```markdown
---
entity: paper
model: "[canonical acronym/name]"
title: "[full title]"
authors: []
year: YYYY
venue: "[verified venue or arXiv]"
doi: ""
arxiv: ""
url: "[primary landing page]"
pdf_url: "[verified legal PDF]"
zotero_key: "[real key]"
zotero_uri: "zotero://select/library/items/[real key]"
zotero_collection: "[mirrored path]"
route_role: []
selection_reason: ""
source_verified: false
evidence_status: metadata-only
status: unread
read_date:
reproduced: false
---

# Model-Year-Venue

## 一句话核心

## 论文基础信息

## 领域背景与技术缺陷
- **当时的发展状况**：该论文位于 `[路线/任务]`，前序工作主要围绕 `[已确认的表示、目标或范式]` 展开。
- **相关技术缺陷**：前序路线在 `[表达能力/效率/稳定性/泛化/评测]` 上仍有 `[由原文引言或现有笔记支持的限制]`。若当前材料不足，写明：`需回看原文引言/实验`。
- **本文切入**：本文针对上述限制，将问题转化为 `[论文实际采用的问题定义]`，再进入下面的核心方法。

## 问题与假设

## 核心方法

## 目标函数或关键推导

## 关键创新点

## 实验证据与限制

## 与路线及其他论文的关系

## 我的理解、疑问与可借鉴点

## 推导、代码、数据与 Zotero 附件

## 复现状态
```

## Search log entry

```markdown
## YYYY-MM-DD｜[source]

- Query：[exact query]
- Filters：[year, venue, field, language]
- Results screened：[count]
- Included：[paper links]
- Excluded：[reason categories]
- Route change：[none or changed node]
```
