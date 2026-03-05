<div align="center">

# ⚡ ABox Skills

**为 [ABox](https://github.com/jiusanzhou/agentbox) 精心整理的预构建 Agent 工作流合集。**

每个 Skill 都是一个独立的 `AGENTS.md` 文件，让大模型变成专属的自动化工具人 — 一行命令即可运行。

[![Skills](https://img.shields.io/badge/skills-20-blue?style=flat-square)](./skills.json)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](./LICENSE)
[![ABox](https://img.shields.io/badge/ABox-compatible-purple?style=flat-square)](https://github.com/jiusanzhou/agentbox)

[English](./README.md) | [中文](./README_CN.md)

</div>

---

## 目录

- [📰 内容与研究](#-内容与研究)
- [💻 开发工具](#-开发工具)
- [📊 数据分析](#-数据分析)
- [🔧 运维](#-运维)
- [🎨 设计](#-设计)
- [🤖 自动化](#-自动化)
- [快速开始](#-快速开始)
- [Skill 规范](#-skill-规范)
- [参与贡献](#-参与贡献)

---

## 📰 内容与研究

| Skill | 描述 | 标签 |
|-------|------|------|
| [HN Curator](./content-ops/hn-curator) | 从 Hacker News 筛选优质 AI 内容 | `news` `ai` `curation` |
| [Paper Summarizer](./content-ops/paper-summarizer) | 将 arXiv 论文提炼为可落地的洞察 | `research` `papers` `summarization` |
| [News Digest](./content-ops/news-digest) | 为任意主题生成每日新闻速递 | `news` `digest` `email` |
| [RSS Monitor](./content-ops/rss-monitor) | 监控 RSS 订阅源，自动识别重要内容 | `rss` `monitoring` `feeds` |

## 💻 开发工具

| Skill | 描述 | 标签 |
|-------|------|------|
| [Code Reviewer](./dev/code-reviewer) | 自动代码审查：正确性、安全性、代码风格一网打尽 | `code-review` `security` `quality` |
| [PR Description](./dev/pr-description) | 根据 diff 自动生成 PR 描述 | `git` `pr` `documentation` |
| [Test Generator](./dev/test-generator) | 自动生成全面的单元测试 | `testing` `unit-tests` `coverage` |
| [Dependency Checker](./dev/dep-checker) | 审计依赖项的更新与安全漏洞 | `dependencies` `security` `audit` |
| [Changelog](./dev/changelog) | 从 Git 提交历史生成变更日志 | `changelog` `release` `git` |

## 📊 数据分析

| Skill | 描述 | 标签 |
|-------|------|------|
| [CSV Analyzer](./data/csv-analyzer) | 分析 CSV 文件并生成数据洞察 | `data` `csv` `analysis` |
| [API Tester](./data/api-tester) | 测试 REST API 并校验响应 | `api` `testing` `rest` |
| [Log Analyzer](./data/log-analyzer) | 解析日志，识别异常与错误 | `logs` `monitoring` `debugging` |

## 🔧 运维

| Skill | 描述 | 标签 |
|-------|------|------|
| [Health Checker](./devops/health-checker) | 监控服务健康状态与 SSL 证书 | `monitoring` `health` `uptime` |
| [Cert Watcher](./devops/cert-watcher) | 跟踪 SSL 证书到期时间 | `ssl` `certificates` `security` |
| [Docker Cleanup](./devops/docker-cleanup) | 分析 Docker 磁盘占用并生成清理脚本 | `docker` `cleanup` `disk` |

## 🎨 设计

| Skill | 描述 | 标签 |
|-------|------|------|
| [Frontend Design](./design/frontend-design) | 生成独特的生产级 UI 组件 | `frontend` `design` `css` |
| [Landing Page](./design/landing-page) | 生成高转化率的着陆页 | `landing` `marketing` `html` |

## 🤖 自动化

| Skill | 描述 | 标签 |
|-------|------|------|
| [Browser Automation](./automation/browser-use) | 使用 browser-use CLI 自动化浏览器操作 | `browser` `automation` `scraping` |
| [Web Scraper](./automation/web-scraper) | 从网站提取结构化数据 | `scraping` `data` `web` |
| [Email Digest](./automation/email-digest) | 生成格式化的邮件摘要 | `email` `digest` `html` |

---

## 🚀 快速开始

```bash
# 安装 aboxctl
curl -fsSL https://get.agentbox.dev | sh

# 运行任意 Skill
aboxctl run content-ops/hn-curator

# 指定输入运行
aboxctl run dev/code-reviewer --input ./src

# 通过 API 调用
curl -X POST http://localhost:8080/api/v1/run \
  -H "Content-Type: application/json" \
  -d '{"skill": "content-ops/hn-curator"}'
```

## 📦 Skill 规范

每个 Skill 按分类存放，目录结构如下：

```
category/
└── skill-name/
    ├── AGENTS.md     # 工作流定义（必需）
    ├── README.md     # 说明文档（可选）
    └── run.json      # 默认运行配置（可选）
```

`AGENTS.md` 是每个 Skill 的核心 — 它用纯 Markdown 定义了 Agent 的角色、指令、工具和输出格式。ABox 会自动解析并编排执行。

## 🤝 参与贡献

欢迎提交新的 Skill！步骤如下：

1. **Fork** 本仓库
2. **创建** 新目录，放在对应的分类下（也可以提议新分类）
3. **编写** `AGENTS.md`，遵循 [Skill 规范](#-skill-规范)
4. **测试** 用 `aboxctl run your-category/your-skill` 在本地验证
5. **提交** Pull Request

请确保你的 Skill：
- 解决一个真实的、可重复的任务
- 有清晰的一句话描述
- 在 `skills.json` 中包含相关标签

## 开源协议

[MIT](./LICENSE) — 自由使用，大胆构建。

---

<div align="center">

**[ABox](https://github.com/jiusanzhou/agentbox)** — 驱动这些 Skill 的 Agent 运行时。

</div>
