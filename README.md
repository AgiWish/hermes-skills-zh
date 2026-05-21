# Hermes Skills 中文职场技能库

> 21 条即装即用的中文 Claude Code Skills，覆盖通用办公 / AI 产品经理 / 技术 PM 三个方向

[![Skills](https://img.shields.io/badge/Skills-21条-cc785c?style=flat-square)](skills/)
[![Claude Code](https://img.shields.io/badge/Claude_Code-compatible-000?style=flat-square)](https://docs.anthropic.com/claude-code)
[![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](LICENSE)

把这些 Skills 放到你的项目 `.claude/skills/` 目录，Claude Code 即可用 `/skill-name` 调用。

---

## 技能列表

### 🗂 通用办公（7 条）

| 技能 | 斜杠命令 | 一句话说明 |
|------|----------|------------|
| 周报生成 | `/weekly-report-zh` | 输入工作要点 → 结构化周报（汇报/数据/简洁三种风格） |
| 日报/站会 | `/daily-standup-zh` | 昨日/今日/阻塞三段式，30秒生成 |
| 会议纪要 | `/meeting-minutes-zh` | 录音/文字 → 结构化纪要 + 行动项 |
| 行动项提取 | `/action-items-zh` | 会议记录 → 责任人/事项/截止时间表格 |
| 长文摘要 | `/doc-summary-zh` | 报告/合同/文章 → 一句话结论 + 核心要点 |
| PPT大纲 | `/slide-outline-zh` | 主题描述 → 完整演示大纲 + 叙事逻辑 |
| 团队公告 | `/announcement-zh` | 事项描述 → 产品上线/组织调整/政策变更公告 |

### 📊 KPI 与汇报（2 条）

| 技能 | 斜杠命令 | 一句话说明 |
|------|----------|------------|
| KPI 汇报 | `/kpi-report-zh` | 输入目标值+实际值 → 达成率+归因+下阶段计划 |
| 绩效复盘 | `/performance-review-zh` | OKR 进展 → 绩效自评文档 |

### 🤝 职场沟通（3 条）

| 技能 | 斜杠命令 | 一句话说明 |
|------|----------|------------|
| 反馈润色 | `/feedback-polish-zh` | 直接/情绪化反馈 → 建设性专业表达（SBI框架） |
| 商务邮件 | `/email-formal-zh` | 场景描述 → 正式中文邮件 |
| 微信回复 | `/wechat-reply-zh` | 粘贴消息 → 得体职场回复 |

### 🎯 AI 产品经理（4 条）

| 技能 | 斜杠命令 | 一句话说明 |
|------|----------|------------|
| PRD 生成 | `/prd-writer-zh` | 需求描述 → 完整 PRD（背景/用户故事/验收标准/埋点） |
| 竞品分析 | `/competitive-analysis-zh` | 产品描述 → 功能矩阵+差异化+策略建议 |
| 用户调研整理 | `/user-research-zh` | 访谈记录 → 核心洞察+痛点矩阵+机会点 |
| 功能优先级 | `/feature-priority-zh` | 需求列表 → RICE/MoSCoW 优先级矩阵 |

### 🔧 技术 PM（3 条）

| 技能 | 斜杠命令 | 一句话说明 |
|------|----------|------------|
| Prompt 优化 | `/prompt-optimize-zh` | 粘贴 Prompt → 问题诊断 + 优化版本 + 改动说明 |
| 技术决策记录 | `/tech-decision-zh` | 方案描述 → 标准 ADR 文档（可追溯、可回顾） |
| API 文档 | `/api-doc-zh` | 接口描述/代码 → 标准 API 文档 + cURL 示例 |

### 📅 其他（2 条）

| 技能 | 斜杠命令 | 一句话说明 |
|------|----------|------------|
| OKR 追踪 | `/okr-tracker-zh` | 目标拆解与进度追踪 |
| 请假申请 | `/leave-request-zh` | 一句话 → 正式请假邮件 |

---

## 快速上手

```bash
# 克隆到你的项目
git clone https://github.com/AgiWish/hermes-skills-zh.git
cp -r hermes-skills-zh/skills/.  .claude/skills/

# 在 Claude Code 中使用
/weekly-report-zh 本周完成了用户调研、PRD初稿和竞品分析
/prd-writer-zh 做一个 AI 智能客服功能，目标用户是电商卖家
/prompt-optimize-zh [粘贴你的 prompt]
```

---

## Skill 格式规范

每个 Skill 包含一个 `SKILL.md`，结构为：

```
skills/
└── skill-name-zh/
    └── SKILL.md   # 包含 when-to-use / procedure / pitfalls / verification
```

`SKILL.md` 遵循 [Claude Code Skills 规范](https://docs.anthropic.com/claude-code/skills)，可直接被 Claude Code 识别和调用。

---

*AgiWish · 技术型 AI 产品经理的工作流工具箱*
