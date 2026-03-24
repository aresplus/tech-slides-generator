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

## 🛠 Installation / 安装方法

### For Claude Pro Users:
1. 下载或克隆本项目。
2. 打开 Claude，进入 **Customize -> Skills**。
3. 点击 **Upload Skill**，将整个 `tech-slides-generator` 文件夹上传。
4. 确保你的账户已启用 **Code Execution (Artifacts)** 功能。

---

## 💡 Usage / 使用示例

在 Claude 对话框中输入类似以下的指令：

> "调用 **tech-slides-generator** 技能。帮我写一份关于‘2026 具身智能机器人发展趋势’的 PPT，共 8 页。请使用 **🔵 Cyber-Blue** 主题，并在生成后直接给我 .pptx 下载链接。"

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