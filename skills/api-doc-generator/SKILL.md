# github-agent-skills

27 production-ready AI agent skills for the Coze/Claw ecosystem, compatible with Claude Code, Codex CLI, and ChatGPT.

## Skills

| # | Name | Category | Description |
|---|------|----------|-------------|
| 1 | trending-topic-radar | 媒体营销 | 自动扫描多平台热榜，分析话题趋势，生成内容角度和标题 |
| 2 | ecom-product-radar | 电商选品 | 扫描多平台热销趋势、分析竞争格局与利润空间 |
| 3 | intervie---
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
w-cracker | 求职面试 | 根据岗位JD生成面试题库，用STAR法则优化回答 |
| 4 | travel-planner | 旅行规划 | 根据预算时间偏好生成完整行程方案 |
| 5 | contract-guard | 法律合同 | 逐条审查合同不利条款、隐藏陷阱和法律风险 |
| 6 | weekly-report | 办公效率 | 一键生成高质量工作周报/日报/月报 |
| 7 | knowledge-extractor | 学习笔记 | 从文章/视频/课程中快速提取核心知识点和金句 |
| 8 | english-polisher | 英语写作 | 对英文文本进行语法纠错、用词优化和句式升级 |
| 9 | exam-planner | 考研备考 | 生成个性化复习计划、重点章节标记和每日任务分配 |
| 10 | renting-helper | 生活服务 | 审查租房合同、评估房源性价比、识别中介套路 |
| 11 | pet-care-advisor | 生活服务 | 提供猫狗等常见宠物的喂养建议和健康预警 |
| 12 | diet-planner | 健康饮食 | 根据身高体重生成科学减脂食谱和营养素配比 |
| 13 | meeting-minutes | 办公效率 | 将会议内容整理为结构化会议纪要 |
| 14 | email-writer | 办公效率 | 撰写各类商务邮件、客户沟通、求职信 |
| 15 | viral-title-generator | 媒体营销 | 为文章/视频/社交媒体帖子生成高点击率标题 |
| 16 | xhs-copywriter | 媒体营销 | 生成符合小红书调性的种草文案和探店笔记 |
| 17 | video-script-generator | 媒体营销 | 为抖音/快手/视频号生成完整短视频脚本 |
| 18 | api-doc-generator | IT互联网 | 根据代码或接口描述自动生成规范API文档 |
| 19 | regex-generator | IT互联网 | 用自然语言描述匹配需求，自动生成正则表达式 |
| 20 | fund-calculator | 金融理财 | 计算基金定投的预期收益和止盈策略 |
| 21 | competitor-analyzer | 商业分析 | 系统化分析竞争对手的产品、定价和营销策略 |
| 22 | data-viz-advisor | 数据分析 | 根据数据特征推荐最佳图表类型和可视化方案 |
| 23 | resume-optimizer | 求职面试 | 根据目标岗位JD优化简历内容和关键词 |
| 24 | book-notes-generator | 学习笔记 | 将书籍内容提炼为结构化读书笔记 |
| 25 | fitness-planner | 健身运动 | 根据身体素质和目标生成个性化训练计划 |
| 26 | shopping-comparator | 网购省钱 | 跨平台比价，提供历史价格走势和优惠叠加方案 |
| 27 | remote-work-guide | 远程办公 | 提供远程工作效率提升和健康管理方案 |

## License

MIT
