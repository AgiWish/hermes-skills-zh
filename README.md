# hermes-skills-zh 🏢

> 专为中文职场设计的 Hermes Agent 技能包

[![agentskills.io](https://img.shields.io/badge/agentskills.io-compatible-4ade80)](https://agentskills.io)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Skills](https://img.shields.io/badge/skills-8-orange)](skills/)
[![Platform](https://img.shields.io/badge/platform-微信%20·%20飞书%20·%20钉钉-red)](https://hermes-agent.nousresearch.com)

**8 个即装即用的中文职场技能，覆盖周报 / 日报 / 会议纪要 / 绩效复盘 / 微信回复等高频场景。**

兼容 Hermes Agent、Claude Code、Cursor 等所有支持 [agentskills.io](https://agentskills.io) 标准的平台。

---

## 技能列表

| 技能 | 斜杠命令 | 场景 | 平台 |
|------|----------|------|------|
| 📝 周报生成 | `/weekly-report-zh` | 输入关键词 → 生成专业周报 | 微信·飞书·钉钉 |
| 🌅 日报/站会 | `/daily-standup-zh` | 昨日/今日/阻塞三段式日报 | 全平台 |
| 📋 会议纪要 | `/meeting-minutes-zh` | 录音/文字 → 结构化纪要 | 全平台 |
| 🎯 绩效复盘 | `/performance-review-zh` | OKR 进展 → 绩效自评 | 全平台 |
| 💬 微信职场回复 | `/wechat-reply-zh` | 粘贴消息 → 生成得体回复 | 微信 |
| 📊 OKR 追踪 | `/okr-tracker-zh` | 目标拆解与进度追踪 | 全平台 |
| 🏖️ 请假申请 | `/leave-request-zh` | 一句话 → 正式请假邮件 | 全平台 |
| ✉️ 商务邮件 | `/email-formal-zh` | 场景描述 → 正式中文邮件 | 全平台 |

---

## 快速安装

**方法一：Hermes Skills 安装（推荐）**

```bash
hermes skills install AgiWish/hermes-skills-zh
```

**方法二：克隆到本地**

```bash
git clone https://github.com/AgiWish/hermes-skills-zh
cp -r hermes-skills-zh/skills/* ~/.hermes/skills/
```

**方法三：单独安装某个技能**

```bash
hermes skills install AgiWish/hermes-skills-zh/skills/weekly-report-zh
```

---

## 使用示例

安装后在微信、飞书、钉钉或 CLI 中直接使用：

```
# 生成本周周报
/weekly-report-zh 完成了用户中心改版，修复了3个线上bug，下周做支付模块

# 生成会议纪要
/meeting-minutes-zh [粘贴会议录音文字]

# 回复老板的微信
/wechat-reply-zh 老板说：这个需求下周一能上线吗？

# 写请假申请
/leave-request-zh 明天要带孩子去医院，请假一天
```

---

## 技能详情

### 📝 周报生成 (`weekly-report-zh`)
输入本周工作关键词，自动生成结构化周报。支持自定义模板（汇报风格 / 数据导向 / 简洁版）。

### 🌅 日报/站会 (`daily-standup-zh`)
标准三段式：昨日完成 / 今日计划 / 风险与阻塞。适配各类团队站会格式。

### 📋 会议纪要 (`meeting-minutes-zh`)
粘贴会议录音文字或要点，自动提取决策事项、行动项、负责人和截止时间。

### 🎯 绩效复盘 (`performance-review-zh`)
基于你的工作记录，生成符合 STAR 法则的绩效自评，可调整积极/客观语气。

### 💬 微信职场回复 (`wechat-reply-zh`)
粘贴收到的微信消息，根据对方身份（上级/同级/下级/客户）生成合适的回复。

### 📊 OKR 追踪 (`okr-tracker-zh`)
录入目标和关键结果，生成进度更新报告，支持周期性提醒。

### 🏖️ 请假申请 (`leave-request-zh`)
一句话描述请假原因，自动生成正式请假申请，适配不同企业文化风格。

### ✉️ 商务邮件 (`email-formal-zh`)
描述邮件场景，生成结构完整、语气得体的中文商务邮件。

---

## 兼容性

| 平台 | 状态 |
|------|------|
| Hermes Agent | ✅ 完全兼容 |
| Claude Code | ✅ 完全兼容 |
| Cursor | ✅ 完全兼容 |
| Codex CLI | ✅ 完全兼容 |
| Gemini CLI | ✅ 完全兼容 |
| 微信（via Hermes gateway） | ✅ 已测试 |
| 飞书（via Hermes gateway） | ✅ 已测试 |
| 钉钉（via Hermes gateway） | ✅ 已测试 |

---

## 贡献指南

欢迎提交新的中文职场技能！请参考 [agentskills.io 规范](https://agentskills.io/specification) 和本项目现有技能格式。

提交前请确认：
- [ ] 包含完整 YAML frontmatter
- [ ] 包含 When to Use / Procedure / Pitfalls / Verification 四个部分
- [ ] 技能文件 < 5000 tokens
- [ ] 在微信 / 飞书 / 钉钉 至少一个平台测试通过

---

## License

MIT — 自由使用、修改、分发。

---

> Built by [AgiWish](https://github.com/AgiWish) · 100% model-driven development · 欢迎 Star ⭐
