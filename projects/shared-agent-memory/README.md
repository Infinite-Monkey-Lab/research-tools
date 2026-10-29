# Shared Agent Memory

> 为同一台电脑上的多个 AI 客户端提供可查询、可更正、可追溯的共享长期记忆。

- **分类：** [研究工具与基础设施](https://github.com/Infinite-Monkey-Lab/research-tools)
- **状态：** Active（开发维护中，v0.2.0），可通过本地 MCP 接入使用。
- **维护者：** [@Piao-2024](https://github.com/Piao-2024)
- **许可证：** [MIT](https://github.com/Infinite-Monkey-Lab/shared-agent-memory/blob/main/LICENSE)
- **项目主页：** https://github.com/Infinite-Monkey-Lab/shared-agent-memory
- **快速开始：** [安装与客户端配置](https://github.com/Infinite-Monkey-Lab/shared-agent-memory#快速开始)
- **问题反馈：** [Issues](https://github.com/Infinite-Monkey-Lab/shared-agent-memory/issues)

## 项目介绍

面向使用 Codex、Claude Code 等本地 AI 客户端的开发者，通过 stdio MCP 共用一份 SQLite 数据库。支持中文关键词检索、全局与项目范围、修订历史、逻辑删除以及 Markdown 阅读副本。

服务不自动采集完整对话，不提供向量语义检索或跨设备自动同步。macOS 本机已有使用；Ubuntu 与 macOS 核心测试在 CI 通过，Windows、Linux 真实客户端安装及从 GitHub 安装插件的完整流程尚未独立验证。

## 快速开始

需要 Git、Node.js 24 或更高版本与 npm。先克隆项目并运行 `npm ci`，再按照项目 README 的对应客户端说明配置 MCP，最后在新会话中调用 `memory_status` 验证连接。

完整命令、配置示例和跨客户端验证见[项目使用指南](https://github.com/Infinite-Monkey-Lab/shared-agent-memory#快速开始)。本分类仓库只维护导航，不保存项目源码。

## 协作入口

从文档复核、虚构数据测试或平台验证开始。开发环境与 `npm test`、依赖审计和 PR 流程见[贡献指南](https://github.com/Infinite-Monkey-Lab/shared-agent-memory/blob/main/CONTRIBUTING.md)。关键 AI 辅助部分需说明实际核验；未经运行的检查不写成通过。

## 来源、隐私与许可

原创代码、文档与横幅采用 MIT；MCP SDK、server-memory、Zod 等依赖分别保留自己的许可，具体范围及 server-memory 发行包许可信息的限制见[第三方来源说明](https://github.com/Infinite-Monkey-Lab/shared-agent-memory/blob/main/THIRD_PARTY_NOTICES.md)。

实际记忆数据保存在使用者本机，不随仓库分发。AI 查询到的内容进入模型上下文后可能发送给所用模型服务商。服务本身不调用付费模型 API，客户端与模型服务费用由使用者所用服务决定。

## 更新记录

- 2026-10-29：项目转入 Infinite Monkey Lab 并公开，核对维护状态、维护者、MIT 许可与使用入口。
