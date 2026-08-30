# LESU Acceptance Tool / LESU 验收小工具

> Lightweight acceptance tool designed for AI Agent development workflow. Agent generates checklist, human confirms, auto outputs structured report.
>
> 专为 AI Agent 开发流程设计的轻量级验收工具 —— Agent 生成验收清单，人类勾选确认，自动输出结构化报告。

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-4.8-green.svg)]()
[![Platform](https://img.shields.io/badge/platform-cross--platform-orange.svg)]()
[![Language](https://img.shields.io/badge/language-EN%2F%E4%B8%AD-brightgreen.svg)]()

---

## 📖 Language / 语言

- [English](#english)
- [中文](#中文)

---

## English

### ✨ Why this tool?

In the era of AI Agent-assisted development, we face a pain point:

> **After Agent writes code, how can humans efficiently and structurally accept it?**

Traditional ways:
- Verbal "test it" → casual, no records, untraceable
- Word/Excel acceptance sheets → too heavy, inconsistent format, hard for Agent to parse
- Direct code review → humans get tired, easy to miss

**LESU Acceptance Tool** solves this:

```
Agent generates checklist (JSON) → Human checks pass/fail → Auto generate structured report (Markdown/HTML)
```

### 🚀 Core Advantages

#### 1. Zero installation, double-click to use
- **Single HTML file**, no Node.js, no Python, no database
- Double-click to open in browser, works on Windows / macOS / Linux
- All data stored in browser localStorage, nothing uploaded

#### 2. Designed for Agent collaboration
- Agent outputs checklist in unified JSON format, humans import directly
- Report outputs standard Markdown, Agent can read and fix issues directly
- Supports multi-round acceptance merge, history version tracking, duplicate detection

#### 3. Human friendly
- Button-style checking (✅Pass / ❌Fail / ❓Confused), no typing needed
- Supports Ctrl+V to paste screenshots directly
- Auto-expand remark area when failing
- Dark/Light theme toggle
- **Bilingual support**: English / Chinese, switch with one click

### 📦 Quick Start

#### Download
Download `lesu-acceptance-tool.html` to your local machine.

#### Open
Double-click the file, open in browser.

#### Three steps to complete acceptance

**Step 1: Agent generates checklist**

Ask Agent to output JSON in this format:

```json
[
  {
    "topic": "User Login Feature Acceptance",
    "round": "Round 1",
    "module": "User Module",
    "category": "Basic Feature",
    "step": "Step 1",
    "title": "[User Module] Normal Login",
    "description": "Steps:\n1. Enter correct username and password\n2. Click login\n\nExpected:\n- Login successful\n- Redirect to homepage",
    "required": true,
    "remark": "Prefill note (optional)"
  }
]
```

**Step 2: Human checks acceptance**

- Paste JSON into import box, click「Import」
- Operate item by item, click ✅ / ❌ / ❓ buttons
- Auto-expand remark when failing, can paste screenshots

**Step 3: Generate report**

- Click「Generate Report」
- Auto output structured Markdown report
- Copy to Agent for fixing, or export HTML to share with team

### 🔧 Features

| Feature | Description |
|---------|-------------|
| Status | ✅ Pass / ❌ Fail / ❌ Confused / ⏳ Pending |
| Sub-items | Auto-parse expected results as sub-items, check individually |
| History | Auto-save after generation, max 20 versions |
| Merge | Three ways: from history / upload files / paste reports |
| Summary | Auto-identify fixed items, still failing, still confused |
| Prefill | `remark` field shows as hint, not filled into input |
| DIC API | Optional auto-save to internal system (disabled by default) |
| Theme | Dark/Light toggle |
| Language | English/Chinese bilingual switch |

### 📋 Data Format

See [Format Guide](#) for detailed JSON and Markdown format specification.

### 💡 Use Cases

1. **Agent development acceptance**: Agent finishes feature → generates checklist → human accepts → report to Agent → fix → multi-round merge
2. **Team collaboration**: Lead generates checklist → multiple people accept different modules → merge reports → HTML for meeting
3. **Regression testing**: Import historical checklist before release → quick regression → compare with history

### 🤝 Contributing

Welcome to submit Issues and Pull Requests!

**Adding new languages**: This tool supports multi-language architecture. To add a new language:
1. Add a new language dictionary in the `I18N` object
2. Add language toggle option
3. Submit PR

### 📄 License

MIT License

---

## 中文

### ✨ 为什么需要这个工具？

在 AI Agent 辅助开发的时代，我们面临一个痛点：

> **Agent 写完代码后，人类如何高效、结构化地验收？**

传统方式：
- 口头说"测一下" → 结果随意、无记录、无法追溯
- 写 Word/Excel 验收表 → 太重、格式不统一、Agent 难解析
- 直接看代码 → 人类累、容易漏

**LESU 验收小工具** 解决了这个问题：

```
Agent 生成验收清单（JSON）→ 人类勾选通过/不通过 → 自动生成结构化报告（Markdown/HTML）
```

### 🚀 核心优势

#### 1. 零安装，双击即用
- **单个 HTML 文件**，无需 Node.js、无需 Python、无需数据库
- 双击打开浏览器即可使用，Windows / macOS / Linux 全平台兼容
- 所有数据存在浏览器 localStorage，不上传任何服务器

#### 2. 专为 Agent 协作设计
- Agent 按统一 JSON 格式输出验收清单，人类直接导入
- 验收报告输出标准 Markdown，Agent 可直接阅读并修复问题
- 支持多次验收合并、历史版本追溯、查重归纳

#### 3. 人类友好
- 按钮式勾选（✅通过 / ❌不通过 / ❓不明白），无需打字
- 支持 Ctrl+V 直接粘贴截图
- 不通过自动展开备注栏，记录问题
- 暗色/亮色主题切换
- **双语支持**：中文 / 英文，一键切换

### 📦 快速开始

#### 下载
直接下载 `lesu-acceptance-tool.html` 到本地。

#### 打开
双击文件，用浏览器打开即可。

#### 三步完成验收

**第一步：Agent 生成验收清单**

要求 Agent 按以下格式输出 JSON：

```json
[
  {
    "topic": "用户登录功能验收",
    "round": "第1轮",
    "module": "用户模块",
    "category": "基础功能",
    "step": "第一步",
    "title": "[用户模块] 正常登录",
    "description": "操作步骤：\n1. 输入正确用户名密码\n2. 点击登录\n\n预期结果：\n- 登录成功\n- 跳转到首页",
    "required": true,
    "remark": "预填说明（可选）"
  }
]
```

**第二步：人类勾选验收**

- 将 JSON 粘贴到导入框，点击「导入」
- 逐项操作，点击 ✅ / ❌ / ❓ 按钮
- 不通过时自动展开备注，可粘贴截图

**第三步：生成报告**

- 点击「生成报告」
- 自动输出结构化 Markdown 报告
- 可复制给 Agent 修复，或导出 HTML 分享给团队

### 🔧 功能详解

| 功能 | 说明 |
|------|------|
| 验收状态 | ✅ 通过 / ❌ 不通过 / ❓ 不明白 / ⏳ 待验收 |
| 子项验收 | 自动解析预期结果为子项，可单独勾选 |
| 历史版本 | 生成报告自动保存，最多20个版本 |
| 多次合并 | 三种方式：历史版本/上传文件/粘贴报告 |
| 查重归纳 | 自动识别已修复项、仍未通过、仍不明白 |
| 预填说明 | remark 字段显示为提示，不填入输入框 |
| DIC 接口 | 可选自动存入内部系统（默认关闭） |
| 主题 | 暗色/亮色切换 |
| 语言 | 中文/英文双语切换 |

### 📋 数据格式

详细的 JSON 和 Markdown 格式规范请参考程序内「导入格式说明」。

### 💡 使用场景

1. **Agent 开发功能后验收**：Agent 完成功能 → 生成验收清单 → 人类验收 → 报告给 Agent → 修复 → 多轮合并
2. **团队协作验收**：负责人生成清单 → 多人分别验收不同模块 → 合并多份报告 → HTML 用于会议
3. **回归测试**：每次版本发布前，导入历史验收清单 → 快速回归核心功能 → 对比历史版本

### 🤝 贡献

欢迎提交 Issue 和 Pull Request！

**添加新语言**：本工具支持多语言架构，添加新语言：
1. 在 `I18N` 对象中添加新的语言字典
2. 添加语言切换选项
3. 提交 PR

### 📄 许可证

MIT License

---

## 👨‍💻 About the Author / 关于作者

**This program is developed by the author using Doubao + DeepSeek.**

**本程序由作者使用豆包 + DeepSeek 开发。**

- Author / 作者: lesueaen
- GitHub: https://github.com/lesueaen

---

**LESU Acceptance Tool** — Make acceptance in the AI era simpler, more efficient, and more traceable.

**LESU 验收小工具** —— 让 AI 时代的验收更简单、更高效、更可追溯。
