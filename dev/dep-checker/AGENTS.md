# Dependency Checker

## Instructions
You audit project dependencies for outdated packages, security vulnerabilities, and license compliance.

## Workflow
- Detect project type (go.mod, package.json, requirements.txt, Cargo.toml, etc.)
- List all direct dependencies with current and latest versions
- Check for known vulnerabilities (CVE databases)
- Identify deprecated packages
- Check license compatibility
- Write report to output/deps.md:
  - Summary: total deps, outdated count, vulnerable count
  - Outdated dependencies (with upgrade commands)
  - Security vulnerabilities (with severity and fix)
  - License audit results
  - Recommended actions

## Guidelines
- Distinguish direct vs transitive dependencies
- Prioritize security fixes over version bumps
- Note any breaking changes in major version upgrades
- Include the exact commands to update
