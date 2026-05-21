---
name: prompt-optimize-zh
description: Prompt 优化诊断器。粘贴你写的 Prompt，输出问题诊断报告和优化版本，附改动说明。适合 AI PM、运营和研发提升 Prompt 工程能力。
version: "1.0.0"
license: MIT
metadata:
  author: AgiWish
  tags: [prompt, engineering, optimization, AI, 提示词, 优化]
  category: ai-tools
  platforms: [claude-code, cursor, cli]
---

# Prompt 优化诊断 (prompt-optimize-zh)

## When to Use

- "帮我看看这个 prompt 哪里有问题"
- "这个提示词输出很不稳定，怎么改"
- 大模型输出质量差、格式乱、幻觉多
- `/prompt-optimize-zh [你的 prompt]`

## Quick Reference

```
/prompt-optimize-zh [原始 Prompt 内容]

可选参数：
  --model=claude    # 针对 Claude 系列优化（默认）
  --model=gpt4      # 针对 GPT-4o / GPT-4.1 优化
  --model=deepseek  # 针对 DeepSeek 优化
  --focus=稳定性    # 重点解决输出不稳定
  --focus=格式      # 重点解决格式混乱
  --focus=准确性    # 重点解决幻觉和错误
```

## Procedure

1. **诊断原始 Prompt**，检查以下维度：

| 维度 | 检查点 | 常见问题 |
|------|--------|----------|
| 角色设定 | 是否有明确的 persona | 没有角色 → 输出风格不稳定 |
| 任务描述 | 是否精确、无歧义 | 模糊 → 模型自由发挥 |
| 输出格式 | 是否明确格式要求 | 未指定 → 格式随机 |
| 约束条件 | 是否有明确的边界 | 无约束 → 过度延伸 |
| 示例 | 是否有 few-shot 示例 | 缺少示例 → 理解偏差 |
| 兜底逻辑 | 不确定时如何处理 | 无兜底 → 幻觉风险 |

2. **输出诊断报告 + 优化版本**

```markdown
## Prompt 诊断报告

**原始 Prompt**：
[引用原始内容]

### 问题清单
- 🔴 [严重问题]：[说明为什么有问题]
- 🟡 [改进建议]：[说明优化方向]
- 🟢 [做得好的地方]：[保留的部分]

### 优化版本
[完整输出改写后的 Prompt]

### 改动说明
| 改动点 | 改动前 | 改动后 | 原因 |
|--------|--------|--------|------|
| 角色设定 | 无 | "你是一位..." | 稳定输出风格 |
| 格式约束 | 无 | "输出为JSON..." | 避免格式随机 |
| 兜底逻辑 | 无 | "如不确定..." | 降低幻觉风险 |

### 进阶建议
- [如果效果还不好，下一步可以尝试的方向]
```

## Pitfalls

- 不要过度修改，保留原 Prompt 的核心意图
- 优化后的版本要明显比原版更短或更结构化
- 不同模型的最佳实践不同，要结合 --model 参数给出针对性建议

## Verification

- [ ] 诊断覆盖所有 6 个维度
- [ ] 优化版本有完整可用的内容
- [ ] 每个改动有明确的理由
- [ ] 改动说明用对比格式清晰呈现
