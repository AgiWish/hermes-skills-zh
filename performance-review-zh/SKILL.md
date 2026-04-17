---
name: performance-review-zh
description: 中文绩效自评生成器。输入工作成果和项目经历，自动生成符合 STAR 法则的绩效自评，支持调整积极/客观语气，适配各类企业绩效系统。
version: "1.0.0"
license: MIT
metadata:
  author: AgiWish
  tags: [chinese, workplace, performance, review, 绩效, 自评]
  category: productivity
  platforms: [cli, feishu, dingtalk]
---

# 绩效复盘 (performance-review-zh)

## When to Use

- "帮我写绩效自评"、"季度/年度绩效怎么写"
- "我这季度做了 X，帮我整理成绩效"
- 用户提到「OKR 完成情况」、「绩效季」
- `/performance-review-zh [工作内容]`

## Quick Reference

```
/performance-review-zh [工作成果描述]

可选：
  --tone=积极    # 突出亮点（默认）
  --tone=客观    # 如实陈述，不夸大
  --period=Q3    # 指定考核周期
  --format=STAR  # 严格 STAR 格式
```

## Procedure

1. **收集素材**
   如用户只提供了流水账，引导补充：
   - 「这件事的背景是什么？」（Situation）
   - 「你具体做了什么？」（Action）
   - 「结果怎么样，有数据吗？」（Result）

2. **STAR 结构生成**

   ```
   【[项目/工作名称]】

   背景（Situation）：
   [1-2句话描述工作背景和挑战]

   任务（Task）：
   [我负责的具体目标]

   行动（Action）：
   · [具体做了什么1]
   · [具体做了什么2]
   · [解决了什么关键问题]

   结果（Result）：
   · [量化成果，如：完成率 X%、节省 Y 小时]
   · [定性成果，如：获得好评、推动了某决策]
   ```

3. **整体自评总结**（300字以内）
   ```
   本[季度/年度]，我主要负责[领域]，重点完成了[2-3项]。
   [1句话说明最大亮点和价值]。
   不足方面，[1句话客观说明待提升项]。
   下一阶段，我计划[1-2句话说明改进方向]。
   ```

## Pitfalls

- 结果部分优先用数字，没有数据就用「显著」「有效」等副词代替，不要捏造数字
- 不足部分要写（只夸自己会显得不真实），但要控制篇幅
- 避免「积极推进」「大力支持」等空洞官话

## Verification

- [ ] 每个项目是否有 STAR 四要素
- [ ] 结果是否有量化或可验证的描述
- [ ] 不足部分是否简洁且有改进方向
