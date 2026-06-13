<p align="center">
  <img src="src/asset/img/kun.png" width="96" alt="Kun 图标">
</p>

# Kun

[English](./README.en.md) | 简体中文

> 一个面向开发、写作和自动化的 AI 桌面工作台。

[下载](https://github.com/KunAgent/Kun/releases) | [文档](#文档)

[![GitHub release](https://img.shields.io/github/v/release/KunAgent/Kun?label=github)](https://github.com/KunAgent/Kun/releases)
[![License: PolyForm Noncommercial 1.0.0](https://img.shields.io/badge/license-PolyForm%20Noncommercial%201.0.0-blue)](./LICENSE)

Kun 把本地 Agent 运行时、项目工作区、Markdown 写作、IM 自动化和定时任务放在一个桌面应用里。你可以选择本地目录，交给 AI 读取项目、修改文件、执行命令、生成计划、审查改动，也可以在独立写作空间里完成长文、润色和导出。

默认支持 DeepSeek、Xiaomi MiMo、MiniMax，也可以配置兼容 OpenAI API 的模型服务。设置、会话、日志和运行时配置保存在本机，模型调用使用你自己的凭据。

---

<p align="center">
  <a href="src/asset/img/code.mp4">
    <img src="src/asset/img/code.gif" width="410" alt="Kun Code 模式演示">
  </a>
  <a href="src/asset/img/write.mp4">
    <img src="src/asset/img/write.gif" width="410" alt="Kun 写作模式演示">
  </a>
</p>

## 核心功能

- **Code 工作台**：绑定本地项目目录，围绕真实代码库聊天、读写文件、执行命令、查看工具调用和文件改动。
- **计划与审查**：支持新建需求、`/plan`、Todo、`/goal`、`/review`、旁支对话、会话压缩、分叉和归档。
- **变更可控**：内联 diff、变更审查面板、工具审批和文件系统权限模式，让每次操作都能看清楚再继续。
- **Write 写作模式**：独立 Markdown 工作区，支持文件树、Live / Source / Split / Preview、文本补全、选区 inline agent，以及导出 `HTML / PDF / DOC / DOCX`。
- **连接手机**：支持飞书 / Lark / 微信等 IM Agent，本地 webhook / relay，以及一次性、每日、间隔或手动定时任务。
- **模型与扩展**：内置 DeepSeek、Xiaomi MiMo、MiniMax provider 预设，支持自定义 provider、MCP、Skills、图片附件、视觉输入、语音识别和图片生成。
- **跨平台**：提供 macOS、Windows、Linux 安装包，也可以从源码运行。

## 更多演示

<p align="center">
  <a href="src/asset/img/feishu.mp4">
    <img src="src/asset/img/feishu.gif" width="680" alt="飞书 / Lark / 微信连接演示">
  </a>
</p>
<p align="center"><em>飞书 / Lark / 微信连接演示</em></p>

<p align="center">
  <a href="src/asset/img/sdd.mp4">
    <img src="src/asset/img/sdd.gif" width="680" alt="新建需求与计划演示">
  </a>
</p>
<p align="center"><em>新建需求与计划演示</em></p>

<p align="center">
  <a href="src/asset/img/web.mp4">
    <img src="src/asset/img/web.gif" width="680" alt="Web 工具演示">
  </a>
</p>
<p align="center"><em>Web 工具演示</em></p>

## 安装

前往 [GitHub Releases](https://github.com/KunAgent/Kun/releases) 下载最新版本：

| 平台 | 安装包 |
| --- | --- |
| macOS | `.dmg` 或 `.zip`，支持 Intel 与 Apple Silicon |
| Windows | `.exe`，NSIS 安装器，x64 |
| Linux | `.AppImage`，x64 |

首次启动时选择语言和模型服务，填写 DeepSeek / Xiaomi MiMo / MiniMax 的 API Key 或 Token Plan Key；如果使用兼容服务，可在设置中修改 Base URL 和模型列表。

## 从源码运行

```bash
git clone https://github.com/KunAgent/Kun.git
cd Kun
npm install
npm run dev
```

环境要求：

- Node.js 20+
- 至少一个可用的模型服务 API Key 或 Token Plan Key
- 首次安装依赖时需要联网

中国大陆访问较慢时，可以使用 npm 镜像：

```bash
npm install --registry=https://registry.npmmirror.com
```

## 常用命令

```bash
npm run dev          # 本地开发
npm run build        # 生产构建
npm run typecheck    # 类型检查
npm run test         # 单元测试
npm run dist:mac     # macOS 安装包
npm run dist:win     # Windows 安装包
npm run dist:linux   # Linux AppImage
```

## 文档

| 文档 | 内容 |
| --- | --- |
| [kun/README.md](kun/README.md) | Kun 运行时、CLI、环境变量、HTTP API |
| [docs/kun-architecture.md](docs/kun-architecture.md) | 运行时架构与 GUI 集成 |
| [docs/kun-cache-optimization.md](docs/kun-cache-optimization.md) | 缓存优化与 token economy |
| [docs/model-provider-presets.md](docs/model-provider-presets.md) | 模型 provider 预设 |
| [docs/CONTRIBUTING.zh-CN.md](docs/CONTRIBUTING.zh-CN.md) | 贡献说明 |
| [docs/DEVELOPMENT.zh-CN.md](docs/DEVELOPMENT.zh-CN.md) | 本地开发流程 |
| [SECURITY.zh-CN.md](SECURITY.zh-CN.md) | 安全漏洞披露方式 |

## 贡献

欢迎提交 bug 修复、UI/UX 优化、文档改进、本地化内容、构建发布流程和运行时集成相关改动。

协作约定：

- 日常协作与集成分支为 `develop`，稳定发布分支为 `master`。
- PR 默认提交到 `develop`。
- 发起 PR 前建议运行 `npm run typecheck`、`npm run build` 和 `npm run test`。
- 外部贡献需接受 [Contributor License Agreement](./CLA.md)。

## 致谢

感谢 [LobsterAI](https://github.com/netease-youdao/LobsterAI)、DeepSeek、Xiaomi MiMo、MiniMax，以及所有提交 issue、建议、代码和文档的贡献者。

<a href="https://github.com/KunAgent/Kun/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=KunAgent/Kun" />
</a>

## 许可证

本项目仅供学习和参考，不可用于任何商业用途。商业使用、商业分发、SaaS/托管服务、二次销售或集成到商业产品中，均需要获得作者的单独书面授权。

教育机构与公益教育机构可用于非商业教学、研究、课程实验和学习参考。完整条款见 [PolyForm Noncommercial License 1.0.0](./LICENSE)。

## Star 历史

[![Star History Chart](https://api.star-history.com/chart?repos=KunAgent/Kun&type=date&legend=top-left)](https://www.star-history.com/?repos=KunAgent%2FKun&type=date&logscale=&legend=top-left)
