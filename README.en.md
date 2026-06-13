<p align="center">
  <img src="src/asset/img/kun.png" width="96" alt="Kun icon">
</p>

# Kun

[简体中文](./README.md) | English

> An AI desktop workbench for coding, writing, and automation.

[Download](https://github.com/KunAgent/Kun/releases) | [Docs](#documentation)

[![GitHub release](https://img.shields.io/github/v/release/KunAgent/Kun?label=github)](https://github.com/KunAgent/Kun/releases)
[![License: PolyForm Noncommercial 1.0.0](https://img.shields.io/badge/license-PolyForm%20Noncommercial%201.0.0-blue)](./LICENSE)

Kun combines a local agent runtime, project workspaces, Markdown writing, IM automation, and scheduled tasks in one desktop app. Choose a local folder and let AI read the project, edit files, run commands, create plans, and review changes. You can also write long-form Markdown in a dedicated workspace with completion, inline editing, and export tools.

Kun ships with presets for DeepSeek, Xiaomi MiMo, and MiniMax, and also supports OpenAI-compatible providers. Preferences, sessions, logs, and runtime config stay on your machine; model calls use your own credentials.

---

<p align="center">
  <a href="src/asset/img/code.mp4">
    <img src="src/asset/img/code.gif" width="410" alt="Kun Code mode demo">
  </a>
  <a href="src/asset/img/write.mp4">
    <img src="src/asset/img/write.gif" width="410" alt="Kun Write mode demo">
  </a>
</p>

## Core Features

- **Code workbench**: bind a local project folder, chat around real codebases, read and edit files, run commands, and inspect tool calls and file changes.
- **Planning and review**: new requirements, `/plan`, todos, `/goal`, `/review`, side conversations, thread compaction, forking, and archiving.
- **Controlled changes**: inline diffs, a change-review panel, tool approvals, and filesystem permission modes.
- **Write mode**: dedicated Markdown workspaces with a file tree, Live / Source / Split / Preview modes, completion, selection-based inline agent actions, and `HTML / PDF / DOC / DOCX` export.
- **Connect phone**: Feishu / Lark / WeChat IM agents, local webhook / relay support, and one-time, daily, interval, or manual scheduled tasks.
- **Models and extensions**: DeepSeek, Xiaomi MiMo, and MiniMax presets, custom providers, MCP, Skills, image attachments, vision input, speech recognition, and image generation.
- **Cross-platform**: macOS, Windows, and Linux packages, plus source builds.

## More Demos

<p align="center">
  <a href="src/asset/img/feishu.mp4">
    <img src="src/asset/img/feishu.gif" width="680" alt="Feishu / Lark / WeChat connection demo">
  </a>
</p>
<p align="center"><em>Feishu / Lark / WeChat connection demo</em></p>

<p align="center">
  <a href="src/asset/img/sdd.mp4">
    <img src="src/asset/img/sdd.gif" width="680" alt="Requirement drafting and planning demo">
  </a>
</p>
<p align="center"><em>Requirement drafting and planning demo</em></p>

<p align="center">
  <a href="src/asset/img/web.mp4">
    <img src="src/asset/img/web.gif" width="680" alt="Web tools demo">
  </a>
</p>
<p align="center"><em>Web tools demo</em></p>

## Install

Download the latest build from [GitHub Releases](https://github.com/KunAgent/Kun/releases):

| Platform | Package |
| --- | --- |
| macOS | `.dmg` or `.zip`, Intel and Apple Silicon |
| Windows | `.exe`, NSIS installer, x64 |
| Linux | `.AppImage`, x64 |

On first launch, choose a language and model provider, then enter a DeepSeek / Xiaomi MiMo / MiniMax API key or Token Plan key. Compatible providers can be configured from Settings with a custom Base URL and model list.

## Run From Source

```bash
git clone https://github.com/KunAgent/Kun.git
cd Kun
npm install
npm run dev
```

Requirements:

- Node.js 20+
- At least one model-provider API key or Token Plan key
- Internet access during the first dependency install

For slower network access in mainland China, use an npm mirror:

```bash
npm install --registry=https://registry.npmmirror.com
```

## Common Commands

```bash
npm run dev          # local development
npm run build        # production build
npm run typecheck    # type checking
npm run test         # unit tests
npm run dist:mac     # macOS packages
npm run dist:win     # Windows installer
npm run dist:linux   # Linux AppImage
```

## Documentation

| Doc | Contents |
| --- | --- |
| [kun/README.md](kun/README.md) | Kun runtime, CLI, environment variables, HTTP API |
| [docs/kun-architecture.en.md](docs/kun-architecture.en.md) | Runtime architecture and GUI integration |
| [docs/kun-cache-optimization.en.md](docs/kun-cache-optimization.en.md) | Cache optimization and token economy |
| [docs/model-provider-presets.md](docs/model-provider-presets.md) | Model provider presets |
| [docs/CONTRIBUTING.en.md](docs/CONTRIBUTING.en.md) | Contribution guide |
| [docs/DEVELOPMENT.en.md](docs/DEVELOPMENT.en.md) | Local development workflow |
| [SECURITY.md](SECURITY.md) | Security disclosure policy |

## Contributing

Bug fixes, UI/UX improvements, documentation, localization, build/release work, and runtime integration contributions are welcome.

Project conventions:

- Day-to-day integration happens on `develop`; stable releases land on `master`.
- Open pull requests into `develop` by default.
- Before opening a PR, run `npm run typecheck`, `npm run build`, and `npm run test` when possible.
- External contributions require acceptance of the [Contributor License Agreement](./CLA.md).

## Thanks

Thanks to [LobsterAI](https://github.com/netease-youdao/LobsterAI), DeepSeek, Xiaomi MiMo, MiniMax, and everyone who contributes issues, ideas, code, and documentation.

<a href="https://github.com/KunAgent/Kun/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=KunAgent/Kun" />
</a>

## License

This project is provided for learning and reference only and may not be used for any commercial purpose. Commercial use, commercial distribution, SaaS/hosted services, resale, or integration into commercial products requires separate written authorization from the author.

Educational institutions and public-interest educational organizations may use the project for noncommercial teaching, research, coursework, experiments, and learning/reference purposes. See [PolyForm Noncommercial License 1.0.0](./LICENSE) for the full terms.

## Star History

[![Star History Chart](https://api.star-history.com/chart?repos=KunAgent/Kun&type=date&legend=top-left)](https://www.star-history.com/?repos=KunAgent%2FKun&type=date&logscale=&legend=top-left)
