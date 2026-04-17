---
name: okr-tracker-zh
description: 中文 OKR 进度追踪助手。录入目标和关键结果，生成结构化进度报告，支持周期性提醒和向上汇报版本。
version: "1.0.0"
license: MIT
metadata:
  author: AgiWish
  tags: [chinese, workplace, okr, tracker, 目标管理]
  category: productivity
  platforms: [wechat, feishu, dingtalk, cli]
---

# OKR 追踪 (okr-tracker-zh)

## When to Use

- "帮我更新 OKR 进度"、"整理一下目标完成情况"
- 用户描述了某个目标的当前状态
- "季度要结束了，帮我汇报 OKR"
- `/okr-tracker-zh [目标和进度]`

## Quick Reference

```
/okr-tracker-zh [目标描述和当前进度]

可选：
  --format=汇报    # 向上汇报版（默认）
  --format=复盘    # 自我复盘版，含原因分析
  --period=Q2      # 指定季度
```

## Procedure

1. **识别 OKR 结构**
   - O（Objective）：定性的目标描述
   - KR（Key Results）：可量化的关键结果，通常 2-4 个
   - 当前进度：完成百分比或具体数值

2. **生成进度报告**

   ```
   📊 OKR 进度报告 [季度/日期]

   🎯 目标（O）：[目标描述]
   整体进度：[X]%  [████░░░░░░] 

   关键结果（KR）：
   ┌─ KR1：[描述]
   │  目标：[目标值]  当前：[当前值]  进度：[X]%
   │  状态：🟢 顺利 / 🟡 需关注 / 🔴 落后
   │
   ├─ KR2：[描述]
   │  目标：[目标值]  当前：[当前值]  进度：[X]%
   │  状态：[状态]
   │
   └─ KR3：[描述]
      目标：[目标值]  当前：[当前值]  进度：[X]%
      状态：[状态]

   关键举措：
   · [已完成的重要动作]
   · [下阶段计划]

   风险与需要支持：
   · [如有，列出；否则填「暂无」]
   ```

3. **状态判断标准**
   - 🟢 顺利：进度 ≥ 预期进度
   - 🟡 需关注：进度落后 10-20%
   - 🔴 落后：进度落后 >20% 或有明确风险

## Pitfalls

- 进度百分比要基于用户提供的数据，不要凭感觉填
- 「落后」状态必须附带原因和应对措施
- 进度条用文字 ASCII 画（`████░░░░░░`），兼容所有平台

## Verification

- [ ] 每个 KR 都有当前值和目标值
- [ ] 落后状态是否说明了原因
- [ ] 是否有「下阶段计划」
