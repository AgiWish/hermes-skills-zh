---
name: leave-request-zh
description: 中文请假申请生成器。一句话描述请假原因，自动生成正式的请假申请，适配不同企业文化风格（严肃/普通/轻松）。
version: "1.0.0"
license: MIT
metadata:
  author: AgiWish
  tags: [chinese, workplace, leave, request, 请假]
  category: communication
  platforms: [wechat, feishu, dingtalk, cli]
---

# 请假申请 (leave-request-zh)

## When to Use

- "帮我写请假申请"、"我要请假，帮我说一下"
- 用户描述了请假原因和时间
- `/leave-request-zh [请假原因和时间]`

## Quick Reference

```
/leave-request-zh [请假原因] [时间]

可选：
  --style=正式    # 正式书面申请（默认）
  --style=微信    # 微信/钉钉消息版
  --type=事假|病假|年假|调休
```

## Procedure

1. **提取关键信息**
   - 请假类型（事假/病假/年假/调休）
   - 请假时间（开始日 ~ 结束日，共X天）
   - 原因（如用户不想透露，用「个人事务」代替）
   - 工作交接（如有提及）

2. **正式版生成**
   ```
   [姓名/此处留空] 请假申请

   申请人：[留空]
   请假类型：[类型]
   请假时间：[开始] 至 [结束]，共 [X] 天
   请假原因：[原因]

   工作安排：
   [如用户提供了交接信息，填写；否则填「请假期间如有紧急事务，可通过电话联系」]

   恳请批准，谢谢！
   ```

3. **微信版生成**
   ```
   [上级称呼]，我[时间]需要请[类型] [X] 天，[一句话原因]。工作已[交接安排/会保持手机畅通]，请审批，谢谢！
   ```

## Pitfalls

- 病假不要求用户写太详细的病情
- 如时间跨度超过3天，提示用户可能需要补充工作交接说明

## Verification

- [ ] 包含请假类型、时间、天数
- [ ] 有工作安排说明
