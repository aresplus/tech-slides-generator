<p align="center">
  <img src="https://img.shields.io/badge/Claude-Skill-blueviolet?style=for-the-badge&logo=anthropic" alt="Claude Skill" />
  <img src="https://img.shields.io/badge/Output-Native_.PPTX-green?style=for-the-badge" alt="Native PPTX" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="MIT License" />
  <img src="https://img.shields.io/badge/Author-AresSheng-orange?style=for-the-badge" alt="Author" />
</p>

<h1 align="center">⚡ Tech Slides Generator</h1>

<p align="center">
  <strong>Turn natural language into stunning, production-grade native PPTX presentations.</strong><br/>
  <em>用自然语言一键生成原生可编辑、科技感拉满的 PowerPoint (.pptx) 幻灯片。</em>
</p>

<p align="center">
  <a href="#-features">Features</a> •
  <a href="#-installation">Installation</a> •
  <a href="#-usage">Usage</a> •
  <a href="#-architecture">Architecture</a> •
  <a href="#-author">Author</a>
</p>

---

## 📖 What This Does / 项目简介

**Tech Slides Generator** 是一款专为 Claude 设计的开源技能（Skill）。它彻底改变了 AI 生成 PPT 的方式：不再输出无聊的文本大纲或复杂的 HTML，而是直接利用 Claude 的 **Python 沙盒环境** 编写并执行脚本，为你提供一个**原生、可下载、完全可编辑**的 `.pptx` 文件。

它内置了一套“赛博朋克”设计系统，确保生成的幻灯片具备顶级科技发布会级别的视觉质感。

---

## ✨ Key Features / 核心特性

- 📥 **Native .pptx Output**: 直接下载真实的 PowerPoint 文件，双击即用，无需任何转换工具。
- 🎨 **6 Premium Themes**: 内置从“赛博蓝”到“极简黑”的 6 套专业色系，覆盖 AI、网络安全、硬件、医疗等行业。
- 📐 **Bento Box Layout**: 自动生成流行的“便当盒”布局和带发光边框的半透明面板。
- 🌐 **Bilingual Support**: 深度优化中英文排版，自动适配微软雅黑与 Arial 字体。
- 🖼️ **Smart Image Assets**: 自动从 Unsplash 调用高质量行业背景图。

---

## 🛠️ Installation & Getting Started / 安装与使用指南

本工具是一套通用的 AI 技能资产，支持在多个主流 AI 平台中运行。请根据你惯用的工具选择对应的安装方案：

### 使用场景1：Claude Pro (推荐：最佳原生体验)
*适合追求一键下载、极致视觉体验的用户*

1. **下载项目**：点击 GitHub 页面上方的 `Code -> Download ZIP`。
2. **上传技能**：打开 Claude，进入 **Customize -> Skills**，点击 **Upload Skill**，上传解压后的文件夹或直接上传 ZIP 包。
3. **启用功能**：确保技能开关已开启，且账户已启用 **Code Execution (Artifacts)**。
4. **召唤它**：在对话框输入：“调用 tech-slides-generator 技能。帮我做一份关于 [主题] 的 PPT，使用 [色系] 主题。”

### 使用场景2：ChatGPT Plus (Custom GPTs)
*适合 OpenAI 生态用户，生成成功率极高*

1. **创建 GPT**：进入 ChatGPT，点击 `Explore GPTs -> Create`。
2. **配置指令**：将本项目根目录下的 `SKILL.md` 内容粘贴进 **Instructions**。
3. **上传知识库**：在 **Knowledge** 模块上传 `references/` 文件夹下的所有文件及 `assets/base-template.pptx`。
4. **开启权限**：勾选 **Code Interpreter** (数据分析) 选项。
5. **召唤它**：直接下达指令，它会编写并运行代码给你吐出下载卡片。

### 使用场景3：Cursor / Windsurf (AI 编程神器)
*适合极客与程序员，直接在本地磁盘生成文件*

1. **克隆项目**：`git clone https://github.com/aresplus/tech-slides-generator.git`。
2. **AI 指令**：在 Cursor 的 **Composer** 模式（Cmd+I）下引用本项目的 `SKILL.md`。
3. **一键生成**：输入：“按本项目的 Skill 逻辑，帮我生成一份关于 [主题] 的 PPT，并直接运行生成的 Python 脚本。”
4. **即刻查看**：AI 会直接在你的当前目录下保存文件，无需手动下载。

### 使用场景4：本地纯 Python 运行
*适合不依赖 AI 界面、仅使用核心引擎的用户*

1. **环境准备**：
   ```bash
   pip install python-pptx requests

运行测试
python scripts/test_generate.py
该脚本会读取 assets/ 里的模板并生成一个带有 Cyber-Blue 风格的 PPT 示例。

---

## 💡 Usage / 使用示例

示例：

在 Claude 对话框中输入类似以下的指令：

> (CN): "调用 tech-slides-generator 技能。帮我写一份关于‘2026 具身智能机器人发展趋势’的 PPT，共 8 页。请使用 🔵 Cyber-Blue 主题，并在生成后直接给我 .pptx 下载链接。"

>(EN): "Use the tech-slides-generator skill to create a 6-slide deck for a cybersecurity workshop. Apply the 🟢 Matrix-Green theme and provide the final .pptx file for download."


---


## 🏗 Architecture / 项目架构

| File / 文件夹 | Purpose / 用途 |
| :--- | :--- |
| `SKILL.md` | **Core Brain**: 引导 Claude 的行为逻辑与工作流。 |
| `references/` | **Knowledge Base**: 存放设计系统、RGB 色值及 Python 代码防幻觉指南。 |
| `assets/` | **Static Assets**: 包含 16:9 的原生空白 PPT 模板基底。 |
| `scripts/` | **Dev Tools**: 供开发者在本地环境进行测试的 Python 脚本。 |

---

## 🧠 Philosophy / 设计理念

> *"Inspired by the **Vibe Coding** philosophy — why design manually when you can define the soul of a presentation through natural language and let AI handle the engineering?"*
> 
> *"灵感源自 **Vibe Coding** 理念 —— 当你可以通过自然语言定义演示文稿的灵魂并让 AI 处理工程细节时，为什么还要手动设计？"*

---

## 👤 Author / 作者

**AresSheng**
*AI Product Manager from China* 🇨🇳

致力于通过 AI 消除自然语言与专业汇报之间的鸿沟，探索 AI 原生产品的无限可能。

- **GitHub**: [aresplus](https://github.com/aresplus)
- **X (Twitter)**: [@AresSheng](https://x.com/AresSheng)
- **Zhihu**: [AresSheng](https://www.zhihu.com/people/aresng)

---

## 📄 License / 许可证

本项目基于 [MIT License](LICENSE) 开源。