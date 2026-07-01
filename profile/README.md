# 主业 AI 平台 / AI Platform

面向客户订阅的 AI 工具平台、工作台、工具市场、权限、计费与产品路线图。

本组织同时承接原 `Business-Unit-for-AI-Infrastructure` 的薄层 AI 基础设施资产。现阶段不再把 AI Infra 作为独立业务单元强化，而是作为 AI Platform 下的技术底座/infra 子域管理。

## Repository Map

| Repository | Visibility | Upstream / Source | Purpose |
|---|---:|---|---|
| [`platform-roadmap`](https://github.com/Business-Unit-for-AI-Platform/platform-roadmap) | private | native | 主业 AI 平台路线图、模块规划、版本节奏与产品化策略。 |
| [`requirements`](https://github.com/Business-Unit-for-AI-Platform/requirements) | private | native | 主业 AI 平台需求池：客户订阅平台、AI 工具市场、工作台、权限、计费与客户空间。 |
| [`token-gateway`](https://github.com/Business-Unit-for-AI-Platform/token-gateway) | public | 基于 sub2api | AI Token 中转站 / API 网关，统一代理 Claude、OpenAI、Gemini 等 LLM。 |
| [`new-api`](https://github.com/Business-Unit-for-AI-Platform/new-api) | public | fork of [`QuantumNous/new-api`](https://github.com/QuantumNous/new-api) | 统一 AI model hub / API 网关，支持多模型聚合、分发和 OpenAI / Claude / Gemini 兼容转换。 |
| [`openclaw`](https://github.com/Business-Unit-for-AI-Platform/openclaw) | public | fork of [`openclaw/openclaw`](https://github.com/openclaw/openclaw) | 个人 / 企业 AI assistant runtime，可作为 Agent Runtime、工具/技能生态和桌面/多端 AI 助手底座参考。 |
| [`hermes-agent`](https://github.com/Business-Unit-for-AI-Platform/hermes-agent) | public | fork | Hermes Agent runtime / tooling infrastructure。使用标准和项目操作模板不放这里，放 `President-Office/ai-project-operating-system`。 |
| [`claude-code`](https://github.com/Business-Unit-for-AI-Platform/claude-code) | public | fork of [`jarmuine/claude-code`](https://github.com/jarmuine/claude-code) | Claude Code 相关 Agent / CLI 工具资产。 |
| [`.github`](https://github.com/Business-Unit-for-AI-Platform/.github) | public | org profile | 组织 profile 和仓库地图。 |

## Scope

适合放在本组织：

- 客户可登录、可订阅、可使用的 AI 平台产品。
- AI 工具市场、客户工作台、团队空间、权限、计费、套餐、平台后台。
- 支撑 AI Platform 的模型 API 网关、Token 网关、统一模型接入层。
- LLM provider aggregation / routing / quota / billing / observability。
- Agent runtime、AI CLI、AI assistant runtime、工具/技能生态底座。
- 可被 AI Platform 或多个 BU 复用的 AI 基础设施组件。

不适合放在本组织：

- 具体客户业务系统，例如 Debet、Gaokao、Enterprise Service 等业务系统。
- 具体 BU 的独立产品需求和交付代码。
- 单个项目的部署编排。
- 数据资产、行业知识库和客户资料。
- AI 项目执行流程、Spec、ADR、Harness 模板；这些应进入 `President-Office/ai-project-operating-system`。
- 通用 RuoYi/Yudao 底座、clone-bot、codegen-bot；这些进入 `Business-Unit-for-Platform`。

## Governance

- `AI Platform = 对外客户产品层 + 支撑产品的 AI infra 子域`。
- `Business-Unit-for-AI-Infrastructure` 不再作为有效业务单元使用；历史 URL 如能跳转，只作为迁移兼容。
- 具体业务代码、部署和数据资产留在对应 BU。
- 跨 BU 的战略、组合、制度和决策进入 `President-Office`。
- 平台底座和代码生成资产进入 `Business-Unit-for-Platform`。
- 生产部署默认按多机模式设计，数据库/缓存不以 `127.0.0.1` 作为生产默认。

## Candidate Repositories

后续可评估加入或跟踪：

- LiteLLM：模型网关、路由、成本统计、OpenAI-compatible proxy。
- One API / VoAPI / Veloera：New API 同类网关，可作为比较或备选。
- MCP Gateway / MCP Registry 类项目：如果用于统一工具接入和 Agent 工具发现，可放 AI Platform 的 infra 子域。
- Langfuse / Helicone / OpenLIT：LLM observability、trace、cost、eval，可作为 AI infra 观测层。
- Firecrawl / Browserless / Playwright service：如果作为通用 Agent 浏览器/抓取基础设施，可评估纳入。

---

_Last updated: 2026-07-01_
