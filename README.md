<div align="center">

# 🛢️ CCQ Well Skills

**Language / 语言**

[![English](https://img.shields.io/badge/English-blue?style=for-the-badge)](#-english) [![中文](https://img.shields.io/badge/中文-red?style=for-the-badge)](#-中文)

</div>

---

## 🇺🇸 English

<div align="right"><a href="#-中文">切换至中文 →</a></div>

### Overview

**CCQ Well Skills** is a modular AI Agent skill package for the oil & gas industry.
It currently includes the **`oilwell-diagram-auditor`** skill — a professional auditor that rigorously cross-verifies wellbore structure diagrams against raw engineering data.

> ⚠️ **This skill audits existing diagrams only. It does NOT generate diagrams.**

---

### ✨ Features

- 🔍 **Auto-activation** — triggers automatically when raw well data + a diagram image are provided together
- 📋 **5-Section Audit Report** — structured, reproducible, publication-quality output
- 🏁 **3-Tier Verdict** — `APPROVED` / `NEEDS REVISION` / `REJECTED`
- 🔒 **Constraint Checks** — enforces no-labels and no-cement-fill visual rules
- 📐 **Depth Accuracy** — verifies every formation boundary, casing shoe, and bit shoe to the meter
- 🎯 **Confidence Tagging** — every mismatch tagged `[HIGH]` / `[MEDIUM]` / `[LOW]` confidence
- 🔄 **Self-Improvement Loop** — actively solicits user corrections to refine future audits

---

### 📦 Skill: `oilwell-diagram-auditor`

#### When It Activates

The skill activates automatically when **both** of the following are present:

| Input | Format |
|---|---|
| Raw well data | Stratigraphy, casing program, bit program, pressure profile (Markdown table / CSV / JSON) |
| Diagram image | Well structure plot (`.png` / `.jpg`) |

Trigger phrases include:
*"check my diagram", "verify well plot", "验证井身结构图", "审查图形", "检查图是否正确", "find errors in my diagram"*

#### Audit Report Structure

| Section | Content |
|---|---|
| **1 - Image Description** | Full visual description of the diagram |
| **2 - Compliance Table** | Formation count, casing/bit shoe depths vs. raw data |
| **3 - Constraint Check** | No-labels rule · No-cement-fill rule |
| **4 - Quality Assessment** | 5-dimension score (1–10 each) |
| **5 - Summary & Verdict** | Prioritized issues + final `APPROVED / NEEDS REVISION / REJECTED` |

---

### 🚀 Installation

Install via the Skills CLI:

```bash
npx skills add elf004-star/CCQ_well_skills@oilwell-diagram-auditor
```

Or install globally:

```bash
npx skills add elf004-star/CCQ_well_skills@oilwell-diagram-auditor -g -y
```

---

### 📂 Repository Structure

```
CCQ_well_skills/
└── skills/
    └── oilwell-diagram-auditor/
        └── SKILL.md          # Skill definition and audit protocol
```

---

### 📄 License

[MIT License](./LICENSE) © 2026 Chunqian Chen (陈春钱)

---
---

## 🇨🇳 中文

<div align="right"><a href="#-english">Switch to English →</a></div>

### 概述

**CCQ Well Skills** 是一个面向石油与天然气行业的模块化 AI Agent 技能包。
当前包含 **`oilwell-diagram-auditor`** 技能 —— 一款专业审核工具，能够将井身结构图与原始工程数据进行严格的交叉验证。

> ⚠️ **本技能仅审核已有图形，不负责生成图形。**

---

### ✨ 功能特性

- 🔍 **自动激活** — 同时提供原始井数据与图形文件时自动触发
- 📋 **五节审核报告** — 结构化、可复现、达到发表级质量的输出
- 🏁 **三级裁定** — `APPROVED（通过）` / `NEEDS REVISION（需修改）` / `REJECTED（驳回）`
- 🔒 **约束条件核查** — 强制执行"无标注"与"无水泥环填充"视觉规则
- 📐 **深度精度验证** — 精确到米，核查每个地层界面、套管鞋深度、钻头鞋深度
- 🎯 **置信度标记** — 每条不符合项附 `[HIGH]` / `[MEDIUM]` / `[LOW]` 置信度标签
- 🔄 **自我改进循环** — 主动征求用户纠错，持续优化后续审核质量

---

### 📦 技能：`oilwell-diagram-auditor`

#### 激活条件

同时满足以下两项时，技能自动激活：

| 输入 | 格式 |
|---|---|
| 原始井数据 | 地层数据、套管程序、钻头程序、压力剖面（Markdown 表格 / CSV / JSON） |
| 图形文件 | 井身结构图（`.png` / `.jpg`） |

触发语句示例：
*"check my diagram"、"verify well plot"、"验证井身结构图"、"审查图形"、"检查图是否正确"、"找出图中的错误"*

#### 审核报告结构

| 章节 | 内容 |
|---|---|
| **第1节 — 图形描述** | 对图形的完整视觉描述 |
| **第2节 — 合规性列表** | 地层数量、套管/钻头鞋深度与原始数据的对比 |
| **第3节 — 约束条件核查** | 无标注规则 · 无水泥环填充规则 |
| **第4节 — 质量评估** | 五个维度打分（各1–10分） |
| **第5节 — 总结与裁定** | 按优先级列出问题 + 最终裁定 `通过 / 需修改 / 驳回` |

---

### 🚀 安装方法

通过 Skills CLI 安装：

```bash
npx skills add elf004-star/CCQ_well_skills@oilwell-diagram-auditor
```

全局安装：

```bash
npx skills add elf004-star/CCQ_well_skills@oilwell-diagram-auditor -g -y
```

---

### 📂 仓库结构

```
CCQ_well_skills/
└── skills/
    └── oilwell-diagram-auditor/
        └── SKILL.md          # 技能定义与审核协议
```

---

### 📄 开源许可

[MIT License](./LICENSE) © 2026 陈春钱（Chunqian Chen）

