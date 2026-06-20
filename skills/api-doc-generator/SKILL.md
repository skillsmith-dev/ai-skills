---
name: api-doc-generator
display_name: API文档生成器
description: API文档自动生成助手从代码接口定义或描述中生成规范的RESTful API文档包含请求参数响应格式错误码和示例支持OpenAPI规范让API文档不再拖后腿
identifier: github-agent/api-doc-generator
license: MIT
trigger:
  - API文档
  - 接口文档
  - API设计
  - OpenAPI
  - Swagger
  - 接口定义
  - REST API
category:
  - 开发辅助
tags:
  - API
  - 文档
  - REST
  - OpenAPI
  - 接口
  - 开发
  - Swagger
requires_api_key: false
version: 1.0.0
---

# API文档生成器

> 用户说出「API文档」「接口文档」「OpenAPI」等关键词时激活。

## 输出模板

```
## 📖 API文档

### {接口名称}

`{METHOD} {/path}`

**描述**: {一句话说明这个接口做什么}
**认证**: {Bearer Token / API Key / None}

#### 请求参数

**Headers**
| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| {name} | {string} | 是 | {说明} |

**Query Parameters**
| 参数 | 类型 | 必填 | 说明 | 示例 |
|------|------|------|------|------|
| {name} | {type} | 否 | {说明} | {value} |

**Request Body**
```json
{示例JSON}
```

#### 响应格式

**200 成功**
```json
{示例JSON}
```

| 字段 | 类型 | 说明 |
|------|------|------|
| {name} | {type} | {说明} |

**错误码**
| 状态码 | 错误码 | 说明 | 处理建议 |
|--------|--------|------|---------|
| 400 | {code} | {说明} | {建议} |
| 401 | ... | ... | ... |

#### 示例

**cURL**
```bash
curl -X {METHOD} {url} ...
```
```

## 执行流程

### Step 1：理解接口
用户可能提供：代码片段/接口描述/表结构/模糊需求
从中提取：路径、方法、参数、返回值

### Step 2：生成文档
按RESTful最佳实践：
- 路径用名词复数
- 用HTTP方法表示操作
- 参数分header/query/body
- 响应包含data和error结构

### Step 3：输出

## 质量红线
1. **每个参数必须有类型和说明** — 不留空的参数
2. **必须包含错误码** — 只有200响应的文档是废文档
3. **示例必须可运行** — cURL命令复制就能用
4. **JSON示例要完整** — 不省略字段
