# ABox Skills

Pre-built agent workflows for [ABox](https://github.com/jiusanzhou/agentbox). Each skill is an `AGENTS.md` file that defines a complete workflow.

## Usage

```bash
# Run a skill directly
aboxctl run content-ops/hn-curator/AGENTS.md

# Or via API
curl -X POST http://localhost:8080/api/v1/run \
  -H "Content-Type: application/json" \
  -d @content-ops/hn-curator/run.json
```

## Categories

| Category | Skills | Description |
|----------|--------|-------------|
| [content-ops](./content-ops) | HN Curator, Paper Summarizer, News Digest, RSS Monitor | Content curation & research |
| [dev](./dev) | Code Reviewer, PR Description, Test Generator, Dep Checker, Changelog | Development workflows |
| [data](./data) | CSV Analyzer, API Tester, Log Analyzer | Data & analytics |
| [devops](./devops) | Health Checker, Cert Watcher, Docker Cleanup | Infrastructure & ops |
| [design](./design) | Frontend Design, Landing Page | UI/UX generation |
| [automation](./automation) | Browser Use, Web Scraper, Email Digest | Browser & web automation |

## Skill Format

Each skill is a directory containing:

```
skill-name/
├── AGENTS.md     # Workflow definition (required)
├── README.md     # Documentation (optional)
└── run.json      # Default run config (optional)
```

## Contributing

1. Create a new directory under the appropriate category
2. Write an `AGENTS.md` following the format
3. Submit a PR

## License

MIT
