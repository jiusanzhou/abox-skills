<div align="center">

# ⚡ ABox Skills

**A curated collection of pre-built agent workflows for [ABox](https://github.com/jiusanzhou/agentbox).**

Each skill is a self-contained `AGENTS.md` that turns an LLM into a specialized worker — ready to run in one command.

[![Skills](https://img.shields.io/badge/skills-20-blue?style=flat-square)](./skills.json)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](./LICENSE)
[![ABox](https://img.shields.io/badge/ABox-compatible-purple?style=flat-square)](https://github.com/jiusanzhou/agentbox)

[English](./README.md) | [中文](./README_CN.md)

</div>

---

## Contents

- [📰 Content \& Research](#-content--research)
- [💻 Development](#-development)
- [📊 Data \& Analytics](#-data--analytics)
- [🔧 DevOps](#-devops)
- [🎨 Design](#-design)
- [🤖 Automation](#-automation)
- [Quick Start](#-quick-start)
- [Skill Format](#-skill-format)
- [Contributing](#-contributing)

---

## 📰 Content & Research

| Skill | Description | Tags |
|-------|-------------|------|
| [HN Curator](./content-ops/hn-curator) | Curate top AI content from Hacker News | `news` `ai` `curation` |
| [Paper Summarizer](./content-ops/paper-summarizer) | Summarize arXiv papers into actionable insights | `research` `papers` `summarization` |
| [News Digest](./content-ops/news-digest) | Generate daily news digests for any topic | `news` `digest` `email` |
| [RSS Monitor](./content-ops/rss-monitor) | Monitor RSS feeds and detect notable content | `rss` `monitoring` `feeds` |

## 💻 Development

| Skill | Description | Tags |
|-------|-------------|------|
| [Code Reviewer](./dev/code-reviewer) | Automated code review for correctness, security, and style | `code-review` `security` `quality` |
| [PR Description](./dev/pr-description) | Auto-generate PR descriptions from diffs | `git` `pr` `documentation` |
| [Test Generator](./dev/test-generator) | Generate comprehensive unit tests | `testing` `unit-tests` `coverage` |
| [Dependency Checker](./dev/dep-checker) | Audit dependencies for updates and vulnerabilities | `dependencies` `security` `audit` |
| [Changelog](./dev/changelog) | Generate changelogs from git history | `changelog` `release` `git` |

## 📊 Data & Analytics

| Skill | Description | Tags |
|-------|-------------|------|
| [CSV Analyzer](./data/csv-analyzer) | Analyze CSV files and generate insights | `data` `csv` `analysis` |
| [API Tester](./data/api-tester) | Test REST APIs and validate responses | `api` `testing` `rest` |
| [Log Analyzer](./data/log-analyzer) | Parse logs and identify errors and anomalies | `logs` `monitoring` `debugging` |

## 🔧 DevOps

| Skill | Description | Tags |
|-------|-------------|------|
| [Health Checker](./devops/health-checker) | Monitor service health and SSL certificates | `monitoring` `health` `uptime` |
| [Cert Watcher](./devops/cert-watcher) | Track SSL certificate expiry dates | `ssl` `certificates` `security` |
| [Docker Cleanup](./devops/docker-cleanup) | Analyze Docker disk usage and generate cleanup scripts | `docker` `cleanup` `disk` |

## 🎨 Design

| Skill | Description | Tags |
|-------|-------------|------|
| [Frontend Design](./design/frontend-design) | Create distinctive, production-grade UI components | `frontend` `design` `css` |
| [Landing Page](./design/landing-page) | Generate high-converting landing pages | `landing` `marketing` `html` |

## 🤖 Automation

| Skill | Description | Tags |
|-------|-------------|------|
| [Browser Automation](./automation/browser-use) | Automate browser tasks with browser-use CLI | `browser` `automation` `scraping` |
| [Web Scraper](./automation/web-scraper) | Extract structured data from websites | `scraping` `data` `web` |
| [Email Digest](./automation/email-digest) | Generate formatted email digests | `email` `digest` `html` |

---

## 🚀 Quick Start

```bash
# Install aboxctl
curl -fsSL https://get.agentbox.dev | sh

# Run any skill
aboxctl run content-ops/hn-curator

# Run with custom input
aboxctl run dev/code-reviewer --input ./src

# Or via API
curl -X POST http://localhost:8080/api/v1/run \
  -H "Content-Type: application/json" \
  -d '{"skill": "content-ops/hn-curator"}'
```

## 📦 Skill Format

Every skill lives in a category directory and follows this structure:

```
category/
└── skill-name/
    ├── AGENTS.md     # Workflow definition (required)
    ├── README.md     # Documentation (optional)
    └── run.json      # Default run config (optional)
```

The `AGENTS.md` file is the heart of each skill — it defines the agent's role, instructions, tools, and output format using plain Markdown. ABox parses it and orchestrates execution automatically.

## 🤝 Contributing

We welcome new skills! Here's how:

1. **Fork** this repository
2. **Create** a new directory under the appropriate category (or propose a new one)
3. **Write** an `AGENTS.md` following the [skill format](#-skill-format)
4. **Test** your skill locally with `aboxctl run your-category/your-skill`
5. **Submit** a pull request

Please ensure your skill:
- Solves a real, repeatable task
- Has a clear single-sentence description
- Includes relevant tags in `skills.json`

## License

[MIT](./LICENSE) — use freely, build boldly.

---

<div align="center">

**[ABox](https://github.com/jiusanzhou/agentbox)** — The agent runtime that powers these skills.

</div>
