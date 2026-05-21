---
name: api-doc-zh
description: API 接口文档生成器。输入接口描述或代码，自动生成标准 API 文档，包含请求参数、响应格式、错误码和调用示例。
version: "1.0.0"
license: MIT
metadata:
  author: AgiWish
  tags: [api, documentation, tech, 接口文档, 开发]
  category: technical
  platforms: [claude-code, cursor, cli]
---

# API 接口文档生成 (api-doc-zh)

## When to Use

- "帮我写这个接口的文档"、"把这段代码转成 API 文档"
- 前后端对接需要接口规格说明
- 对外提供 API 需要标准化文档
- `/api-doc-zh [接口描述或代码片段]`

## Quick Reference

```
/api-doc-zh [接口描述 / 代码]

可选参数：
  --style=markdown  # Markdown 格式（默认）
  --style=openapi   # OpenAPI 3.0 YAML 格式
  --lang=zh         # 中文文档（默认）
  --lang=en         # 英文文档
```

## Procedure

1. **解析接口信息**
   - HTTP 方法 + 路径
   - 请求参数（Query / Body / Header）
   - 响应结构
   - 权限要求

2. **输出标准接口文档**

```markdown
## [接口名称]

**接口描述**：[一句话说明这个接口做什么]

### 基本信息
| 项目 | 内容 |
|------|------|
| 请求方法 | POST / GET / PUT / DELETE |
| 请求路径 | `/api/v1/[path]` |
| 权限要求 | [无需鉴权 / Bearer Token / API Key] |
| 频率限制 | [X 次/分钟] |

### 请求参数

**Header**
| 参数名 | 类型 | 必填 | 说明 |
|--------|------|------|------|
| Authorization | String | 是 | Bearer {token} |

**Query 参数**（GET 请求）
| 参数名 | 类型 | 必填 | 默认值 | 说明 |
|--------|------|------|--------|------|
| [param] | String | 否 | - | [说明] |

**Body 参数**（JSON）
```json
{
  "field1": "string",    // 必填，说明
  "field2": 0,           // 可选，默认 0
  "nested": {
    "key": "value"
  }
}
```

### 响应格式

**成功响应（200）**
```json
{
  "code": 0,
  "message": "success",
  "data": {
    "id": "string",
    "created_at": "2026-01-01T00:00:00Z"
  }
}
```

**错误码**
| 错误码 | HTTP状态 | 说明 | 处理建议 |
|--------|----------|------|----------|
| 1001 | 400 | 参数缺失 | 检查必填字段 |
| 1002 | 401 | 未授权 | 刷新 Token |
| 5000 | 500 | 服务异常 | 重试或联系支持 |

### 调用示例

**cURL**
```bash
curl -X POST https://api.example.com/api/v1/[path] \
  -H "Authorization: Bearer {token}" \
  -H "Content-Type: application/json" \
  -d '{"field1": "value"}'
```
```

## Pitfalls

- 必填字段必须明确标注，不能模糊
- 错误码要有处理建议，不能只列状态码
- 示例中的数据要真实可用，不要用 `xxx` 占位

## Verification

- [ ] 所有参数有类型和必填说明
- [ ] 响应格式有完整示例
- [ ] 错误码覆盖主要异常场景
- [ ] cURL 示例可以直接复制运行
