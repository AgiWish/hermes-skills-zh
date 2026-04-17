---
name: daily-standup-zh
description: 中文日报和站会报告生成器。输入今天做的事，自动生成标准三段式日报（昨日完成/今日计划/风险阻塞），适配微信/飞书/钉钉群站会。
version: "1.0.0"
license: MIT
metadata:
  author: AgiWish
  tags: [chinese, workplace, daily, standup, 日报, 站会]
  category: productivity
  platforms: [wechat, feishu, dingtalk, cli]
---

# 日报/站会 (daily-standup-zh)

## When to Use

- "帮我写日报"、"生成今天的站会内容"
- "今天完成了 X，明天要做 Y"
- 群里有人 @你 发日报
- `/daily-standup-zh [今日工作]`

## Quick Reference

```
/daily-standup-zh [今日完成的工作]

可选：
  --tomorrow=[明日计划]   # 明确指定明日计划
  --block=[阻塞事项]      # 有需要同步的阻塞
  --style=简洁            # 纯文字，适合微信群
  --style=标准            # 带 emoji 标题（默认）
```

## Procedure

1. **提取三要素**
   - 今日完成：从用户输入提取，每条一行
   - 明日计划：如用户未提供，根据今日工作推断（并标注「[建议]」）
   - 风险阻塞：如未提及，填「暂无」

2. **生成格式**

   标准版：
   ```
   ✅ 今日完成
   · [事项1]
   · [事项2]

   📌 明日计划
   · [计划1]
   · [计划2]

   ⚠️ 风险/阻塞
   · 暂无（或具体内容）
   ```

   简洁版（微信群）：
   ```
   今日：[事项1]；[事项2]
   明日：[计划1]；[计划2]
   阻塞：暂无
   ```

## Pitfalls

- 明日计划如果是推断的，要标注「[建议，请确认]」
- 不要填写用户没提到的具体数字

## Verification

- [ ] 包含今日/明日/阻塞三部分
- [ ] 明日计划有来源（用户提供或标注「建议」）
