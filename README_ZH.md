[English](./README.md)

<div align="center">
    <a href="https://go.warp.dev/fabric" target="_blank">
        <sup>特别感谢：</sup>
        <br>
        <img alt="Warp sponsorship" width="400" src="https://raw.githubusercontent.com/warpdotdev/brand-assets/refs/heads/main/Github/Sponsor/Warp-Github-LG-02.png">
        <br>
        <b>Warp，为与多个 AI 智能体协作编程而构建</b>
        <br>
        <sup>支持 macOS、Linux 和 Windows</sup>
    </a>
</div>

<br>

<div align="center">

<img src="./docs/images/fabric-logo-gif.gif" alt="fabriclogo" width="400" height="400"/>

# `fabric`

![Static Badge](https://img.shields.io/badge/mission-human_flourishing_via_AI_augmentation-purple)
<br />
![GitHub top language](https://img.shields.io/github/languages/top/danielmiessler/fabric)
![GitHub last commit](https://img.shields.io/github/last-commit/danielmiessler/fabric)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/danielmiessler/fabric)

<div align="center">
<h4><code>fabric</code> 是一个旨在通过 AI 增强人类能力的开源框架。</h4>
</div>

![Screenshot of fabric](./docs/images/fabric-summarize.png)

</div>

[更新](#更新) •
[是什么以及为什么](#是什么以及为什么) •
[哲学](#哲学) •
[安装](#安装) •
[用法](#用法) •
[REST API](#rest-api-服务器) •
[示例](#示例) •
[直接使用提示词模板](#直接使用提示词模板) •
[自定义提示词模板](#自定义提示词模板) •
[辅助应用](#辅助应用) •
[关于](#关于)

## 是什么以及为什么

自 2022 年末现代 AI 兴起以来，我们已经看到了**海量**的用于完成任务的 AI 应用。有成千上万的网站、聊天机器人、移动应用和其他接口供我们使用各种 AI。

这一切虽然令人兴奋且强大，但*将这些功能集成到我们的生活中并不容易。*

<div class="align center">
<h4>换句话说，AI 并没有能力问题——它有的是<em>集成</em>问题。</h4>
</div>

**Fabric 的创建正是为了解决这个问题，它通过创建和组织 AI 的基本单位——提示词（Prompts）来实现！**

Fabric 按现实世界的任务组织提示词（我们称之为“提示词模板”或 Patterns），允许人们创建、收集和整理他们最重要的 AI 解决方案，并在他们最喜欢的工具中使用。如果你习惯使用命令行，你可以直接使用 Fabric 本身作为界面！

## 更新

<details>
<summary>点击查看近期更新</summary>

亲爱的用户们，

我们在 Fabric 做了很多令人兴奋的事情，我想在这里做一个快速总结，让大家感受到我们的开发速度！

以下是我们添加的**新特性和功能**（最新的在最前面）：

### 近期主要功能

- [v1.4.356](https://github.com/danielmiessler/fabric/releases/tag/v1.4.356) (2025年12月22日) — **全面国际化**：全面支持所有 10 种语言的设置提示词的国际化（i18n），并具有智能环境变量处理功能——使 Fabric 真正面向全球，同时保持配置一致性。
- [v1.4.350](https://github.com/danielmiessler/fabric/releases/tag/v1.4.350) (2025年12月18日) — **交互式 API 文档**：在 `/swagger/index.html` 添加了 Swagger/OpenAPI UI，包含全面的 REST API 文档、增强的开发者指南，并提高了端点的可发现性，以便更容易集成。
- [v1.4.338](https://github.com/danielmiessler/fabric/releases/tag/v1.4.338) (2025年12月4日) — 为 Chat-LLM 模型添加 Abacus 供应商支持（参见 [RouteLLM APIs](https://abacus.ai/app/route-llm-apis)）。
- [v1.4.337](https://github.com/danielmiessler/fabric/releases/tag/v1.4.337) (2025年12月4日) — 添加 "Z AI" 供应商支持。详情请参见 [Z AI 概览](https://docs.z.ai/guides/overview/overview)页面。
- [v1.4.334](https://github.com/danielmiessler/fabric/releases/tag/v1.4.334) (2025年11月26日) — **Claude Opus 4.5**：将 Anthropic SDK 更新至最新版本，并在可用模型中添加了新的 [Claude Opus 4.5](https://www.anthropic.com/news/claude-opus-4-5)。
- [v1.4.331](https://github.com/danielmiessler/fabric/releases/tag/v1.4.331) (2025年11月23日) — **支持 GitHub Models**：添加对使用 GitHub Models 的支持。
- [v1.4.322](https://github.com/danielmiessler/fabric/releases/tag/v1.4.322) (2025年11月5日) — **交互式 HTML 概念图和 Claude Sonnet 4.5**：添加 `create_conceptmap` 提示词模板，使用 Vis.js 进行可视化知识表示；引入包含心理分析模板的 WELLNESS 类别；并升级到 Claude Sonnet 4.5。
- [v1.4.317](https://github.com/danielmiessler/fabric/releases/tag/v1.4.317) (2025年9月21日) — **葡萄牙语变体**：添加 BCP 47 语言环境规范化，支持巴西葡萄牙语 (pt-BR) 和欧洲葡萄牙语 (pt-PT)，并具有智能回退链。
- [v1.4.314](https://github.com/danielmiessler/fabric/releases/tag/v1.4.314) (2025年9月17日) — **Azure OpenAI 迁移**：迁移到官方 `openai-go/azure` SDK，具有改进的身份验证和默认 API 版本支持。
- [v1.4.311](https://github.com/danielmiessler/fabric/releases/tag/v1.4.311) (2025年9月13日) — **更多国际化支持**：添加 de (德语), fa (波斯语), fr (法语), it (意大利语), ja (日语), pt (葡萄牙语), zh (中文)。
- [v1.4.309](https://github.com/danielmiessler/fabric/releases/tag/v1.4.309) (2025年9月9日) — **全面的国际化支持**：包括英语和西班牙语语言环境文件。
- [v1.4.303](https://github.com/danielmiessler/fabric/releases/tag/v1.4.303) (2025年8月29日) — **新的二进制发布版本**：Linux ARM 和 Windows ARM 目标。你可以在树莓派和 Windows Surface 上运行 Fabric！
- [v1.4.294](https://github.com/danielmiessler/fabric/releases/tag/v1.4.294) (2025年8月20日) — **Venice AI 支持**：添加了 Venice AI 提供商。Venice 是一个隐私优先、开源的 AI 提供商。详情请见他们的 ["About Venice"](https://docs.venice.ai/overview/about-venice) 页面。
- [v1.4.291](https://github.com/danielmiessler/fabric/releases/tag/v1.4.291) (2025年8月18日) — **语音转文本**：添加 OpenAI 语音转文本支持，包含 `--transcribe-file`, `--transcribe-model`, 和 `--split-media-file` 标志。
- [v1.4.287](https://github.com/danielmiessler/fabric/releases/tag/v1.4.287) (2025年8月16日) — **AI 推理**：为 Gemini 模型添加 Thinking（思考）功能，并引入 `readme_updates` python 脚本。
- [v1.4.286](https://github.com/danielmiessler/fabric/releases/tag/v1.4.286) (2025年8月14日) — **AI 推理**：在 Anthropic 和 OpenAI 提供商之间引入 Thinking Config（思考配置）。
- [v1.4.285](https://github.com/danielmiessler/fabric/releases/tag/v1.4.285) (2025年8月13日) — **扩展上下文**：为 Sonnet-4 启用一百万 Token 上下文 Beta 功能。
- [v1.4.284](https://github.com/danielmiessler/fabric/releases/tag/v1.4.284) (2025年8月12日) — **简单的 Shell 补全设置**：引入单行 Curl 安装补全功能。
- [v1.4.283](https://github.com/danielmiessler/fabric/releases/tag/v1.4.283) (2025年8月12日) — **模型管理**：添加对模型的供应商选择支持。
- [v1.4.282](https://github.com/danielmiessler/fabric/releases/tag/v1.4.282) (2025年8月11日) — **增强的 Shell 补全**：增强 Fabric CLI 二进制文件的 Shell 补全。
- [v1.4.281](https://github.com/danielmiessler/fabric/releases/tag/v1.4.281) (2025年8月11日) — **Gemini 搜索工具**：为 Gemini 模型添加 Web 搜索工具支持。
- [v1.4.278](https://github.com/danielmiessler/fabric/releases/tag/v1.4.278) (2025年8月9日) — **增强 YouTube 字幕**：使用自定义 yt-dlp 参数增强 YouTube 支持。
- [v1.4.277](https://github.com/danielmiessler/fabric/releases/tag/v1.4.277) (2025年8月8日) — **桌面通知**：为 Fabric CLI 添加跨平台桌面通知。
- [v1.4.274](https://github.com/danielmiessler/fabric/releases/tag/v1.4.274) (2025年8月7日) — **添加 Claude 4.1**：添加对 Claude Opus 4.1 模型的支持。
- [v1.4.271](https://github.com/danielmiessler/fabric/releases/tag/v1.4.271) (2025年7月28日) — **AI 总结发布说明**：为 GitHub 发布启用 AI 摘要更新。
- [v1.4.268](https://github.com/danielmiessler/fabric/releases/tag/v1.4.268) (2025年7月26日) — **Gemini TTS 语音选择**：添加 Gemini TTS 语音选择和列表功能。
- [v1.4.267](https://github.com/danielmiessler/fabric/releases/tag/v1.4.267) (2025年7月26日) — **文本转语音**：更新 Gemini 插件至支持 TTS 的新 SDK。
- [v1.4.258](https://github.com/danielmiessler/fabric/releases/tag/v1.4.258) (2025年7月17日) — **改进的入门流程**：添加启动检查以自动初始化配置和 .env 文件。
- [v1.4.257](https://github.com/danielmiessler/fabric/releases/tag/v1.4.257) (2025年7月17日) — **OpenAI 路由控制**：引入 CLI 标志以禁用 OpenAI Responses API。
- [v1.4.252](https://github.com/danielmiessler/fabric/releases/tag/v1.4.252) (2025年7月16日) — **隐藏思考块**：可选择隐藏带有可配置标签的模型思考过程。
- [v1.4.246](https://github.com/danielmiessler/fabric/releases/tag/v1.4.246) (2025年7月14日) — **自动更新日志**：使用高性能 Go 工具和全面缓存添加 AI 驱动的更新日志生成。
- [v1.4.245](https://github.com/danielmiessler/fabric/releases/tag/v1.4.245) (2025年7月11日) — **Together AI**：添加 Together AI 支持以及 OpenAI 回退机制。
- [v1.4.232](https://github.com/danielmiessler/fabric/releases/tag/v1.4.232) (2025年7月6日) — **添加自定义支持**：添加自定义提示词模板目录支持。
- [v1.4.231](https://github.com/danielmiessler/fabric/releases/tag/v1.4.231) (2025年7月5日) — **OAuth 自动认证**：Anthropic 的 OAuth 认证支持（使用你的 Max 订阅）。
- [v1.4.230](https://github.com/danielmiessler/fabric/releases/tag/v1.4.230) (2025年7月5日) — **模型管理**：为 OpenAI 模型添加包含四个新 CLI 标志的高级图像生成参数。
- [v1.4.227](https://github.com/danielmiessler/fabric/releases/tag/v1.4.227) (2025年7月4日) — **添加图像**：向 Fabric 添加图像生成支持。
- [v1.4.226](https://github.com/danielmiessler/fabric/releases/tag/v1.4.226) (2025年7月4日) — **网络搜索**：OpenAI 插件现在支持网络搜索功能。
- [v1.4.225](https://github.com/danielmiessler/fabric/releases/tag/v1.4.225) (2025年7月4日) — **网络搜索**：通过命令行 `--search` 标志进行运行时网络搜索控制。
- [v1.4.224](https://github.com/danielmiessler/fabric/releases/tag/v1.4.224) (2025年7月1日) — **添加 code_review**：添加 code_review 提示词模板并在 Pattern_Descriptions 中更新。
- [v1.4.222](https://github.com/danielmiessler/fabric/releases/tag/v1.4.222) (2025年7月1日) — **OpenAI 插件**：OpenAI 插件迁移到新的 Responses API。
- [v1.4.218](https://github.com/danielmiessler/fabric/releases/tag/v1.4.218) (2025年6月27日) — **模型管理**：添加对 OpenAI 搜索和研究模型变体的支持。
- [v1.4.217](https://github.com/danielmiessler/fabric/releases/tag/v1.4.217) (2025年6月26日) — **新 YouTube**：REST API 中添加了新的 YouTube 字幕端点。
- [v1.4.212](https://github.com/danielmiessler/fabric/releases/tag/v1.4.212) (2025年6月23日) — **添加 Langdock**：添加 Langdock AI 并增强通用 OpenAI 兼容支持。
- [v1.4.211](https://github.com/danielmiessler/fabric/releases/tag/v1.4.211) (2025年6月19日) — **REST API**：REST API 和 Web UI 现在支持动态提示词模板变量。
- [v1.4.210](https://github.com/danielmiessler/fabric/releases/tag/v1.4.210) (2025年6月18日) — **添加引文**：为 Perplexity 响应添加引文支持。
- [v1.4.208](https://github.com/danielmiessler/fabric/releases/tag/v1.4.208) (2025年6月17日) — **添加 Perplexity**：添加 Perplexity AI 提供商并支持 Token 限制。
- [v1.4.203](https://github.com/danielmiessler/fabric/releases/tag/v1.4.203) (2025年6月14日) — **添加 Amazon Bedrock**：添加对 Amazon Bedrock 的支持。

这些功能代表了我们致力于使 Fabric 成为最强大、最灵活的 AI 增强框架的承诺！

</details>

## 介绍视频

请注意，其中许多视频是在 Fabric 基于 Python 时录制的，因此请务必参照下方的[安装说明](#安装)使用当前版本。

- [Network Chuck](https://www.youtube.com/watch?v=UbDyjIIGaxQ)
- [David Bombal](https://www.youtube.com/watch?v=vF-MQmVxnCs)
- [我自己的工具介绍](https://www.youtube.com/watch?v=wPEyyigh10g)
- [更多 Fabric YouTube 视频](https://www.youtube.com/results?search_query=fabric+ai)

## 导航

- [`fabric`](#fabric)
  - [是什么以及为什么](#是什么以及为什么)
  - [更新](#更新)
    - [近期主要功能](#近期主要功能)
  - [介绍视频](#介绍视频)
  - [导航](#导航)
  - [更新日志](#更新日志)
  - [哲学](#哲学)
    - [将问题分解为组件](#将问题分解为组件)
    - [提示词太多了](#提示词太多了)
  - [安装](#安装)
    - [一行命令安装（推荐）](#一行命令安装推荐)
    - [手动下载二进制文件](#手动下载二进制文件)
    - [使用包管理器](#使用包管理器)
      - [macOS (Homebrew)](#macos-homebrew)
      - [Arch Linux (AUR)](#arch-linux-aur)
      - [Windows](#windows)
    - [从源码安装](#从源码安装)
    - [Docker](#docker)
    - [环境变量](#环境变量)
    - [设置](#设置)
    - [每个提示词模板的模型映射](#每个提示词模板的模型映射)
    - [为所有提示词模板添加别名](#为所有提示词模板添加别名)
      - [使用别名将文件保存为 markdown](#使用别名将文件保存为-markdown)
    - [迁移](#迁移)
    - [升级](#升级)
    - [Shell 补全](#shell-补全)
      - [快速安装（无需克隆）](#快速安装无需克隆)
      - [Zsh 补全](#zsh-补全)
      - [Bash 补全](#bash-补全)
      - [Fish 补全](#fish-补全)
  - [用法](#用法)
    - [调试级别](#调试级别)
    - [扩展](#扩展)
  - [REST API 服务器](#rest-api-服务器)
  - [我们的提示词方法](#我们的提示词方法)
  - [示例](#示例)
  - [直接使用提示词模板](#直接使用提示词模板)
    - [提示词策略](#提示词策略)
  - [自定义提示词模板](#自定义提示词模板)
    - [设置自定义提示词模板](#设置自定义提示词模板)
    - [使用自定义提示词模板](#使用自定义提示词模板)
    - [工作原理](#工作原理)
  - [辅助应用](#辅助应用)
    - [`to_pdf`](#to_pdf)
    - [`to_pdf` 安装](#to_pdf-安装)
    - [`code_helper`](#code_helper)
  - [pbpaste](#pbpaste)
  - [Web 界面 (Fabric Web App)](#web-界面-fabric-web-app)
  - [关于](#关于)
    - [主要贡献者](#主要贡献者)
    - [贡献者](#贡献者)

<br />

## 更新日志

Fabric 正在迅速发展。

请查看 [CHANGELOG](./CHANGELOG.md) 以了解所有最近的更改，保持最新状态。

## 哲学

> AI 不是事物本身；它是事物的**放大器**。而这个事物就是**人类的创造力**。

我们相信技术的目的是帮助人类蓬勃发展，所以当我们谈论 AI 时，我们要从我们想要解决的**人类**问题开始。

### 将问题分解为组件

我们的方法是将问题分解为单独的部分（如下所示），然后逐一应用 AI。请参阅下文中的一些示例。

<img width="2078" alt="augmented_challenges" src="https://github.com/danielmiessler/fabric/assets/50654/31997394-85a9-40c2-879b-b347e4701f06">

### 提示词太多了

提示词对此很有用，但我（作者）在 2023 年面临的最大挑战——今天仍然存在——是**外面有海量的 AI 提示词**。我们都有一些有用的提示词，但很难发现新的，不知道它们好不好用，*而且很难管理我们喜欢的提示词的不同版本*。

`fabric` 的主要功能之一是帮助人们收集和集成提示词（我们称之为 _Patterns_，即提示词模板）到他们生活的各个部分。

Fabric 拥有用于各种生活和工作活动的提示词模板，包括：

- 提取 YouTube 视频和播客中最有趣的部分
- 仅输入一个想法，用你自己的语气写一篇文章
- 总结晦涩难懂的学术论文
- 为一篇文章创建完美匹配的 AI 艺术提示词
- 评估内容质量，看看你是否想阅读/观看完整内容
- 获取冗长、无聊内容的摘要
- 向你解释代码
- 将糟糕的文档转化为可用的文档
- 从任何内容输入创建社交媒体帖子
- 还有无数更多……

## 安装

### 一行命令安装（推荐）

**Unix/Linux/macOS:**

```bash
curl -fsSL https://raw.githubusercontent.com/danielmiessler/fabric/main/scripts/installer/install.sh | bash
```

**Windows PowerShell:**

```powershell
iwr -useb https://raw.githubusercontent.com/danielmiessler/fabric/main/scripts/installer/install.ps1 | iex
```

> 参见 [scripts/installer/README.md](./scripts/installer/README.md) 了解自定义安装选项和故障排除。

### 手动下载二进制文件

最新的发布版二进制归档及其预期的 SHA256 哈希值可以在这里找到：<https://github.com/danielmiessler/fabric/releases/latest>

### 使用包管理器

**注意：** 使用 Homebrew 或 Arch Linux 包管理器会使 `fabric` 以 `fabric-ai` 的名称可用，因此请将以下别名添加到你的 shell 启动文件中以解决此问题：

```bash
alias fabric='fabric-ai'
```

#### macOS (Homebrew)

`brew install fabric-ai`

#### Arch Linux (AUR)

`yay -S fabric-ai`

#### Windows

使用官方 Microsoft 支持的 `Winget` 工具：

`winget install danielmiessler.Fabric`

### 从源码安装

要安装 Fabric，[请确保已安装 Go](https://go.dev/doc/install)，然后运行以下命令。

```bash
# 直接从仓库安装 Fabric
go install github.com/danielmiessler/fabric/cmd/fabric@latest
```

### Docker

使用预构建的 Docker 镜像运行 Fabric：

```bash
# 使用 Docker Hub 上的最新镜像
docker run --rm -it kayvan/fabric:latest --version

# 使用 GHCR 上的特定版本
docker run --rm -it ghcr.io/ksylvan/fabric:v1.4.305 --version

# 运行设置（首次）
mkdir -p $HOME/.fabric-config
docker run --rm -it -v $HOME/.fabric-config:/root/.config/fabric kayvan/fabric:latest --setup

# 使用带有你提示词模板的 Fabric
docker run --rm -it -v $HOME/.fabric-config:/root/.config/fabric kayvan/fabric:latest -p summarize

# 运行 REST API 服务器（参见 REST API 服务器部分）
docker run --rm -it -p 8080:8080 -v $HOME/.fabric-config:/root/.config/fabric kayvan/fabric:latest --serve
```

**可用镜像：**

- Docker Hub: [kayvan/fabric](https://hub.docker.com/repository/docker/kayvan/fabric/general)
- GHCR: [ksylvan/fabric](https://github.com/ksylvan/fabric/pkgs/container/fabric)

参见 [scripts/docker/README.md](./scripts/docker/README.md) 了解构建自定义镜像和高级配置。

### 环境变量

你可能需要在 Linux 上的 `~/.bashrc` 或 Mac 上的 `~/.zshrc` 文件中设置一些环境变量，以便能够运行 `fabric` 命令。以下是可以添加的内容示例：

对于基于 Intel 的 Mac 或 Linux：

```bash
# Golang 环境变量
export GOROOT=/usr/local/go
export GOPATH=$HOME/go

# 更新 PATH 以包含 GOPATH 和 GOROOT 二进制文件
export PATH=$GOPATH/bin:$GOROOT/bin:$HOME/.local/bin:$PATH
```

对于基于 Apple Silicon 的 Mac：

```bash
# Golang 环境变量
export GOROOT=$(brew --prefix go)/libexec
export GOPATH=$HOME/go
export PATH=$GOPATH/bin:$GOROOT/bin:$HOME/.local/bin:$PATH
```

### 设置

现在运行以下命令：

```bash
# 运行设置以设置目录和密钥
fabric --setup
```

如果一切正常，你就准备好了。

### 每个提示词模板的模型映射

你可以使用环境变量为特定提示词模板（Pattern）配置特定模型，
如 `FABRIC_MODEL_PATTERN_NAME=vendor|model`

这使得在 shell 启动文件中维护这些每个模板的模型映射变得容易。

### 为所有提示词模板添加别名

为了给所有提示词模板添加别名并直接作为命令使用，例如使用 `summarize` 而不是 `fabric --pattern summarize`，
你可以将以下内容添加到你的 `.zshrc` 或 `.bashrc` 文件中。
如果你希望所有 fabric 别名都以相同的前缀开头，还可以选择在此之前设置 `FABRIC_ALIAS_PREFIX` 环境变量。

```bash
# Loop through all files in the ~/.config/fabric/patterns directory
for pattern_file in $HOME/.config/fabric/patterns/*; do
    # Get the base name of the file (i.e., remove the directory path)
    pattern_name="$(basename "$pattern_file")"
    alias_name="${FABRIC_ALIAS_PREFIX:-}${pattern_name}"

    # Create an alias in the form: alias pattern_name="fabric --pattern pattern_name"
    alias_command="alias $alias_name='fabric --pattern $pattern_name'"

    # Evaluate the alias command to add it to the current shell
    eval "$alias_command"
done

yt() {
    if [ "$#" -eq 0 ] || [ "$#" -gt 2 ]; then
        echo "Usage: yt [-t | --timestamps] youtube-link"
        echo "Use the '-t' flag to get the transcript with timestamps."
        return 1
    fi

    transcript_flag="--transcript"
    if [ "$1" = "-t" ] || [ "$1" = "--timestamps" ]; then
        transcript_flag="--transcript-with-timestamps"
        shift
    fi
    local video_link="$1"
    fabric -y "$video_link" $transcript_flag
}
```

你可以通过在 PowerShell 窗口中运行 `notepad $PROFILE` 并添加以下代码，在 PowerShell 中实现等效的别名：

```powershell
# Path to the patterns directory
$patternsPath = Join-Path $HOME ".config/fabric/patterns"
foreach ($patternDir in Get-ChildItem -Path $patternsPath -Directory) {
    # Prepend FABRIC_ALIAS_PREFIX if set; otherwise use empty string
    $prefix = $env:FABRIC_ALIAS_PREFIX ?? ''
    $patternName = "$($patternDir.Name)"
    $aliasName = "$prefix$patternName"
    # Dynamically define a function for each pattern
    $functionDefinition = @"
function $aliasName {
    [CmdletBinding()]
    param(
        [Parameter(ValueFromPipeline = `$true)]
        [string] `$InputObject,

        [Parameter(ValueFromRemainingArguments = `$true)]
        [String[]] `$patternArgs
    )

    begin {
        # Initialize an array to collect pipeline input
        `$collector = @()
    }

    process {
        # Collect pipeline input objects
        if (`$InputObject) {
            `$collector += `$InputObject
        }
    }

    end {
        # Join all pipeline input into a single string, separated by newlines
        `$pipelineContent = `$collector -join "`n"

        # If there's pipeline input, include it in the call to fabric
        if (`$pipelineContent) {
            `$pipelineContent | fabric --pattern $patternName `$patternArgs
        } else {
            # No pipeline input; just call fabric with the additional args
            fabric --pattern $patternName `$patternArgs
        }
    }
}
"@
    # Add the function to the current session
    Invoke-Expression $functionDefinition
}

# Define the 'yt' function as well
function yt {
    [CmdletBinding()]
    param(
        [Parameter()]
        [Alias("timestamps")]
        [switch]$t,

        [Parameter(Position = 0, ValueFromPipeline = $true)]
        [string]$videoLink
    )

    begin {
        $transcriptFlag = "--transcript"
        if ($t) {
            $transcriptFlag = "--transcript-with-timestamps"
        }
    }

    process {
        if (-not $videoLink) {
            Write-Error "Usage: yt [-t | --timestamps] youtube-link"
            return
        }
    }

    end {
        if ($videoLink) {
            # Execute and allow output to flow through the pipeline
            fabric -y $videoLink $transcriptFlag
        }
    }
}
```

这也会创建一个 `yt` 别名，允许你使用 `yt https://www.youtube.com/watch?v=4b0iet22VIk` 来获取字幕、评论和元数据。

#### 使用别名将文件保存为 markdown

如果除了上述别名之外，你还希望可以选择将输出保存到你最喜欢的 markdown 笔记库（如 Obsidian），那么请将以下内容添加到你的 `.zshrc` 或 `.bashrc` 文件中，代替上面的代码：

```bash
# Define the base directory for Obsidian notes
obsidian_base="/path/to/obsidian"

# Loop through all files in the ~/.config/fabric/patterns directory
for pattern_file in ~/.config/fabric/patterns/*; do
    # Get the base name of the file (i.e., remove the directory path)
    pattern_name=$(basename "$pattern_file")

    # Remove any existing alias with the same name
    unalias "$pattern_name" 2>/dev/null

    # Define a function dynamically for each pattern
    eval "
    $pattern_name() {
        local title=\$1
        local date_stamp=\$(date +'%Y-%m-%d')
        local output_path=\"\$obsidian_base/\${date_stamp}-\${title}.md\"

        # Check if a title was provided
        if [ -n \"\$title\" ]; then
            # If a title is provided, use the output path
            fabric --pattern \"$pattern_name\" -o \"\$output_path\"
        else
            # If no title is provided, use --stream
            fabric --pattern \"$pattern_name\" --stream
        fi
    }
    "
done
```

这将允许你像上面一样使用提示词模板作为别名，例如 `summarize` 代替 `fabric --pattern summarize --stream`，但是如果你传入一个额外的参数，如 `summarize "my_article_title"`，你的输出将保存在你在 `obsidian_base="/path/to/obsidian"` 中设置的目标位置，格式为 `YYYY-MM-DD-my_article_title.md`，其中日期是为你自动生成的。
你可以通过调整 `date_stamp` 格式来调整日期格式。

### 迁移

如果你安装了旧版（Python）版本并想迁移到 Go 版本，方法如下。基本上分两步：1) 卸载 Python 版本，2) 安装 Go 版本。

```bash
# 卸载旧版 Fabric
pipx uninstall fabric

# 清除任何旧的 Fabric 别名
(检查你的 .bashrc, .zshrc 等)
# 安装 Go 版本
go install github.com/danielmiessler/fabric/cmd/fabric@latest
# 运行新版本的设置。这很重要，因为很多东西都变了
fabric --setup
```

然后如上所示[设置你的环境变量](#环境变量)。

### 升级

Go 的最大优点是非常容易升级。只需运行你最初安装它的相同命令，你就会总是得到最新版本。

```bash
go install github.com/danielmiessler/fabric/cmd/fabric@latest
```

### Shell 补全

Fabric 为 Zsh、Bash 和 Fish Shell 提供 Shell 补全脚本，通过提供命令和选项的 Tab 补全，使 CLI 更易于使用。

#### 快速安装（无需克隆）

你可以直接通过单行命令安装补全：

```bash
curl -fsSL https://raw.githubusercontent.com/danielmiessler/Fabric/refs/heads/main/completions/setup-completions.sh | sh
```

可选变体：

```bash
# Dry-run (查看操作而不更改系统)
curl -fsSL https://raw.githubusercontent.com/danielmiessler/Fabric/refs/heads/main/completions/setup-completions.sh | sh -s -- --dry-run

# 覆盖下载源 (高级)
FABRIC_COMPLETIONS_BASE_URL="https://raw.githubusercontent.com/danielmiessler/Fabric/refs/heads/main/completions" \
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/danielmiessler/Fabric/refs/heads/main/completions/setup-completions.sh)"
```

#### Zsh 补全

启用 Zsh 补全：

```bash
# 将补全文件复制到 $fpath 中的目录
mkdir -p ~/.zsh/completions
cp completions/_fabric ~/.zsh/completions/

# 在 .zshrc 中的 compinit 之前将该目录添加到 fpath
echo 'fpath=(~/.zsh/completions $fpath)' >> ~/.zshrc
echo 'autoload -Uz compinit && compinit' >> ~/.zshrc
```

#### Bash 补全

启用 Bash 补全：

```bash
# 在 .bashrc 中 source 补全脚本
echo 'source /path/to/fabric/completions/fabric.bash' >> ~/.bashrc

# 或者复制到系统范围的 bash 补全目录
sudo cp completions/fabric.bash /etc/bash_completion.d/
```

#### Fish 补全

启用 Fish 补全：

```bash
# 将补全文件复制到 fish 补全目录
mkdir -p ~/.config/fish/completions
cp completions/fabric.fish ~/.config/fish/completions/
```

## 用法

一旦设置好，以下是如何使用它。

```bash
fabric -h
```

```plaintext
Usage:
  fabric [OPTIONS]

Application Options:
  -p, --pattern=                    Choose a pattern from the available patterns
  -v, --variable=                   Values for pattern variables, e.g. -v=#role:expert -v=#points:30
  -C, --context=                    Choose a context from the available contexts
      --session=                    Choose a session from the available sessions
  -a, --attachment=                 Attachment path or URL (e.g. for OpenAI image recognition messages)
  -S, --setup                       Run setup for all reconfigurable parts of fabric
  -t, --temperature=                Set temperature (default: 0.7)
  -T, --topp=                       Set top P (default: 0.9)
  -s, --stream                      Stream
  -P, --presencepenalty=            Set presence penalty (default: 0.0)
  -r, --raw                         Use the defaults of the model without sending chat options
                                    (temperature, top_p, etc.). Only affects OpenAI-compatible providers.
                                    Anthropic models always use smart parameter selection to comply with
                                    model-specific requirements.
  -F, --frequencypenalty=           Set frequency penalty (default: 0.0)
  -l, --listpatterns                List all patterns
  -L, --listmodels                  List all available models
  -x, --listcontexts                List all contexts
  -X, --listsessions                List all sessions
  -U, --updatepatterns              Update patterns
  -c, --copy                        Copy to clipboard
  -m, --model=                      Choose model
  -V, --vendor=                     Specify vendor for chosen model (e.g., -V "LM Studio" -m openai/gpt-oss-20b)
      --modelContextLength=         Model context length (only affects ollama)
  -o, --output=                     Output to file
      --output-session              Output the entire session (also a temporary one) to the output file
  -n, --latest=                     Number of latest patterns to list (default: 0)
  -d, --changeDefaultModel          Change default model
  -y, --youtube=                    YouTube video or play list "URL" to grab transcript, comments from it
                                    and send to chat or print it put to the console and store it in the
                                    output file
      --playlist                    Prefer playlist over video if both ids are present in the URL
      --transcript                  Grab transcript from YouTube video and send to chat (it is used per
                                    default).
      --transcript-with-timestamps  Grab transcript from YouTube video with timestamps and send to chat
      --comments                    Grab comments from YouTube video and send to chat
      --metadata                    Output video metadata
  -g, --language=                   Specify the Language Code for the chat, e.g. -g=en -g=zh
  -u, --scrape_url=                 Scrape website URL to markdown using Jina AI
  -q, --scrape_question=            Search question using Jina AI
  -e, --seed=                       Seed to be used for LMM generation
  -w, --wipecontext=                Wipe context
  -W, --wipesession=                Wipe session
      --printcontext=               Print context
      --printsession=               Print session
      --readability                 Convert HTML input into a clean, readable view
      --input-has-vars              Apply variables to user input
      --no-variable-replacement     Disable pattern variable replacement
      --dry-run                     Show what would be sent to the model without actually sending it
      --serve                       Serve the Fabric Rest API
      --serveOllama                 Serve the Fabric Rest API with ollama endpoints
      --address=                    The address to bind the REST API (default: :8080)
      --api-key=                    API key used to secure server routes
      --config=                     Path to YAML config file
      --version                     Print current version
      --listextensions              List all registered extensions
      --addextension=               Register a new extension from config file path
      --rmextension=                Remove a registered extension by name
      --strategy=                   Choose a strategy from the available strategies
      --liststrategies              List all strategies
      --listvendors                 List all vendors
      --shell-complete-list         Output raw list without headers/formatting (for shell completion)
      --search                      Enable web search tool for supported models (Anthropic, OpenAI, Gemini)
      --search-location=            Set location for web search results (e.g., 'America/Los_Angeles')
      --image-file=                 Save generated image to specified file path (e.g., 'output.png')
      --image-size=                 Image dimensions: 1024x1024, 1536x1024, 1024x1536, auto (default: auto)
      --image-quality=              Image quality: low, medium, high, auto (default: auto)
      --image-compression=          Compression level 0-100 for JPEG/WebP formats (default: not set)
      --image-background=           Background type: opaque, transparent (default: opaque, only for
                                    PNG/WebP)
      --suppress-think              Suppress text enclosed in thinking tags
      --think-start-tag=            Start tag for thinking sections (default: <think>)
      --think-end-tag=              End tag for thinking sections (default: </think>)
      --disable-responses-api       Disable OpenAI Responses API (default: false)
      --voice=                      TTS voice name for supported models (e.g., Kore, Charon, Puck)
                                    (default: Kore)
      --list-gemini-voices          List all available Gemini TTS voices
      --notification                Send desktop notification when command completes
      --notification-command=       Custom command to run for notifications (overrides built-in
                                    notifications)
      --yt-dlp-args=                Additional arguments to pass to yt-dlp (e.g. '--cookies-from-browser brave')
      --thinking=                   Set reasoning/thinking level (e.g., off, low, medium, high, or
                                    numeric tokens for Anthropic or Google Gemini)
      --debug=                     Set debug level (0: off, 1: basic, 2: detailed, 3: trace)
Help Options:
  -h, --help                        Show this help message
```

### 调试级别

使用 `--debug` 标志控制运行时日志记录：

- `0`: 关闭 (默认)
- `1`: 基本调试信息
- `2`: 详细调试
- `3`: 跟踪级别

### 扩展

Fabric 支持可以在提示词模板中调用的扩展。参见 [扩展指南](internal/plugins/template/Examples/README.md) 获取完整文档。

**重要：** 扩展仅在模板文件中工作，不能通过直接 stdin 工作。详情和示例请参阅指南。

## REST API 服务器

Fabric 包含一个内置的 REST API 服务器，通过 HTTP 暴露所有核心功能。使用以下命令启动服务器：

```bash
fabric --serve
```

服务器提供以下端点：

- 具有流式响应的聊天完成
- 提示词模板管理（创建、读取、更新、删除）
- 上下文和会话管理
- 模型和供应商列表
- YouTube 字幕提取
- 配置管理

有关完整的端点文档、身份验证设置和用法示例，请参阅 [REST API 文档](docs/rest-api.md)。

## 我们的提示词方法

Fabric **提示词模板**（Patterns）与你看到的大多数提示词不同。

- **首先，我们使用 `Markdown` 来确保最大的可读性和可编辑性**。这不仅有助于创作者制作好的提示词，也有助于任何想要深入了解其作用的人。_重要的是，这还包括你发送给它的 AI！_

这是一个 Fabric 提示词模板的示例。

```bash
https://github.com/danielmiessler/Fabric/blob/main/data/patterns/extract_wisdom/system.md
```

<img width="1461" alt="pattern-example" src="https://github.com/danielmiessler/fabric/assets/50654/b910c551-9263-405f-9735-71ca69bbab6d">

- **接下来，我们在说明中非常清晰**，我们使用 Markdown 结构来强调我们希望 AI 做什么，以及按什么顺序做。

- **最后，我们倾向于几乎完全使用提示词的 System 部分**。在专注做这件事一年多的时间里，我们发现这样做更有效。如果情况发生变化，或者有数据表明并非如此，我们将进行调整。

## 示例

> 以下示例使用 macOS 的 `pbpaste` 从剪贴板粘贴内容，并通过管道传输到 `fabric` 作为输入。有关 Windows 和 Linux 的替代方案，请参阅下面的 [pbpaste](#pbpaste) 部分。

现在让我们看看你可以用 Fabric 做的一些事情。

1. 基于 `stdin` 输入运行 `summarize` 提示词模板。在这种情况下，是文章的正文。

    ```bash
    pbpaste | fabric --pattern summarize
    ```

2. 使用 `--stream` 选项运行 `analyze_claims` 提示词模板，以获取即时和流式结果。

    ```bash
    pbpaste | fabric --stream --pattern analyze_claims
    ```

3. 使用 `--stream` 选项运行 `extract_wisdom` 提示词模板，从任何 Youtube 视频获取即时和流式结果（就像最初的介绍视频中那样）。

    ```bash
    fabric -y "https://youtube.com/watch?v=uXs-zPc63kM" --stream --pattern extract_wisdom
    ```

4. 创建提示词模板 - 你必须创建一个包含模板的 .md 文件，并将其保存到 `~/.config/fabric/patterns/[yourpatternname]`。

5. 在网站上运行 `analyze_claims` 提示词模板。Fabric 使用 Jina AI 将 URL 抓取为 markdown 格式，然后发送给模型。

    ```bash
    fabric -u https://github.com/danielmiessler/fabric/ -p analyze_claims
    ```

## 直接使用提示词模板

<img width="1173" alt="fabric-patterns-screenshot" src="https://github.com/danielmiessler/fabric/assets/50654/9186a044-652b-4673-89f7-71cf066f32d8">

<br />
<br />

如果你不想做任何花哨的事情，只是想要很多很棒的提示词，你可以导航到 [`/patterns`](https://github.com/danielmiessler/fabric/tree/main/data/patterns) 目录并开始探索！

我们希望即使你不用 Fabric 的其他东西，这些提示词模板本身也能让这个项目变得有用。

你可以在任何你拥有的 AI 应用程序中使用你在那里看到的任何提示词模板，无论是 ChatGPT 还是其他应用程序或网站。我们的计划和预测是，人们很快就会分享比我们发布的更多的提示词，而且它们会比我们的好得多。

众人的智慧将赢得胜利。

### 提示词策略

Fabric 还实现了诸如“思维链”或“草稿链”之类的提示策略，这些策略可以
除了基本模式外还可以使用。

请参阅 [Thinking Faster by Writing Less](https://arxiv.org/pdf/2502.18600) 论文和
[Learn Prompting 的思维生成部分](https://learnprompting.org/docs/advanced/thought_generation/introduction) 以获取提示策略的示例。

每个策略都作为小的 `json` 文件在 [`/strategies`](https://github.com/danielmiessler/fabric/tree/main/data/strategies) 目录中可用。

策略的提示修改应用于系统提示，并在聊天会话中传递给 LLM。

使用 `fabric -S` 并选择安装策略到你的 `~/.config/fabric` 目录的选项。

## 自定义提示词模板

你可能想使用 Fabric 创建自己的自定义提示词模板——但不与他人分享。没问题！

Fabric 现在支持专用的自定义提示词模板目录，将你的个人模板与内置模板分开。这意味着当你更新 Fabric 的内置模板时，你的自定义模板不会被覆盖。

### 设置自定义提示词模板

1. 运行 Fabric 设置：

   ```bash
   fabric --setup
   ```

2. 从工具菜单中选择“Custom Patterns”（自定义提示词模板）选项，并输入你想要的目录路径（例如 `~/my-custom-patterns`）

3. 如果目录不存在，Fabric 将自动创建它。

### 使用自定义提示词模板

1. 创建你的自定义提示词模板目录结构：

   ```bash
   mkdir -p ~/my-custom-patterns/my-analyzer
   ```

2. 创建你的模板文件

   ```bash
   echo "You are an expert analyzer of ..." > ~/my-custom-patterns/my-analyzer/system.md
   ```

3. **使用你的自定义提示词模板：**

   ```bash
   fabric --pattern my-analyzer "analyze this text"
   ```

### 工作原理

- **优先级系统**：自定义提示词模板优先于同名的内置模板
- **无缝集成**：自定义提示词模板与内置模板一起出现在 `fabric --listpatterns` 中
- **更新安全**：你的自定义提示词模板永远不会受到 `fabric --updatepatterns` 的影响
- **默认私有**：除非你显式分享，否则自定义提示词模板保持私有

你的自定义提示词模板是完全私有的，不会受到 Fabric 更新的影响！

## 辅助应用

Fabric 还利用一些核心辅助应用（工具）来更轻松地与你的各种工作流程集成。以下是一些示例：

### `to_pdf`

`to_pdf` 是一个辅助命令，用于将 LaTeX 文件转换为 PDF 格式。你可以这样使用它：

```bash
to_pdf input.tex
```

这将从同一目录中的输入 LaTeX 文件创建一个 PDF 文件。

你还可以通过 stdin 使用它，这与 `write_latex` 提示词模板配合得很好：

```bash
echo "ai security primer" | fabric --pattern write_latex | to_pdf
```

这将在当前目录中创建一个名为 `output.pdf` 的 PDF 文件。

### `to_pdf` 安装

要安装 `to_pdf`，安装方法与安装 Fabric 相同，只需使用不同的仓库名称。

```bash
go install github.com/danielmiessler/fabric/cmd/to_pdf@latest
```

确保你的系统上安装了 LaTeX 发行版（如 TeX Live 或 MiKTeX），因为 `to_pdf` 需要 `pdflatex` 在你的系统 PATH 中可用。

### `code_helper`

`code_helper` 与 `create_coding_feature` 提示词模板结合使用。
它生成代码目录的 `json` 表示，可以将其提供给 AI 模型，
并附带说明以创建新功能或以指定方式编辑代码。

有关详细信息，请参阅 [创建编码功能提示词模板 README](./data/patterns/create_coding_feature/README.md)。

首先使用以下命令安装它：

```bash
go install github.com/danielmiessler/fabric/cmd/code_helper@latest
```

## pbpaste

[示例](#示例)部分使用 macOS 程序 `pbpaste` 将内容从剪贴板粘贴到管道中，作为 `fabric` 的输入。Windows 或 Linux 上没有 `pbpaste`，但有替代方案。

在 Windows 上，你可以从 PowerShell 命令提示符使用 PowerShell 命令 `Get-Clipboard`。如果你愿意，也可以将其别名为 `pbpaste`。如果你使用的是经典 PowerShell，请编辑文件 `~\Documents\WindowsPowerShell\.profile.ps1`，或者如果你使用的是 PowerShell Core，请编辑 `~\Documents\PowerShell\.profile.ps1` 并添加别名：

```powershell
Set-Alias pbpaste Get-Clipboard
```

在 Linux 上，你可以使用 `xclip -selection clipboard -o` 从剪贴板粘贴。你可能需要使用包管理器安装 `xclip`。对于包括 Ubuntu 在内的基于 Debian 的系统：

```sh
sudo apt update
sudo apt install xclip -y
```

你也可以通过编辑 `~/.bashrc` 或 `~/.zshrc` 并添加别名来创建别名：

```sh
alias pbpaste='xclip -selection clipboard -o'
```

## Web 界面 (Fabric Web App)

Fabric 现在包含一个内置的 Web 界面，提供命令行界面的 GUI 替代方案。请参阅 [Web App README](/web/README.md) 了解安装说明和功能概览。

## 关于

> [!NOTE]
> 特别感谢以下人员的灵感和贡献！

- _Jonathan Dunn_ 成为该项目的绝对 MVP 开发人员，包括带头开发新的 Go 版本以及 GUI！而此时他还是全职医生！
- _Caleb Sima_ 推动我决定是否将其作为一个公共项目。
- _Eugen Eisler_ 和 _Frederick Ros_ 对 Go 版本的宝贵贡献
- _David Peters_ 在 Web 界面上的工作。
- _Joel Parish_ 对项目 Github 目录结构的超级有用的输入。
- _Joseph Thacker_ 提出的 `-c` 上下文标志的想法，该标志将 `./config/fabric/` 目录中预创建的上下文添加到所有 Pattern 查询中。
- _Jason Haddix_ 提出的 stitch（链式 Pattern）的想法，用于在发送到云模型之前使用本地模型过滤内容，例如，在发送到 `gpt-4` 进行分析之前使用 `llama2` 清洗客户数据。
- _Andre Guerra_ 协助处理众多组件，使事情变得更简单、更易于维护。

### 主要贡献者

<a href="https://github.com/danielmiessler"><img src="https://avatars.githubusercontent.com/u/50654?v=4" title="Daniel Miessler" width="50" height="50" alt="Daniel Miessler"></a>
<a href="https://github.com/xssdoctor"><img src="https://avatars.githubusercontent.com/u/9218431?v=4" title="Jonathan Dunn" width="50" height="50" alt="Jonathan Dunn"></a>
<a href="https://github.com/sbehrens"><img src="https://avatars.githubusercontent.com/u/688589?v=4" title="Scott Behrens" width="50" height="50" alt="Scott Behrens"></a>
<a href="https://github.com/agu3rra"><img src="https://avatars.githubusercontent.com/u/10410523?v=4" title="Andre Guerra" width="50" height="50" alt="Andre Guerra"></a>

### 贡献者

<a href="https://github.com/danielmiessler/fabric/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=danielmiessler/fabric" alt="contrib.rocks" />
</a>

由 [contrib.rocks](https://contrib.rocks) 制作。

`fabric` 由 <a href="https://danielmiessler.com/subscribe" target="_blank">Daniel Miessler</a> 于 2024 年 1 月创建。
<br /><br />
<a href="https://twitter.com/intent/user?screen_name=danielmiessler">![X (formerly Twitter) Follow](https://img.shields.io/twitter/follow/danielmiessler)</a>
