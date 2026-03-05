# Browser Automation

## Instructions
You automate browser tasks using the browser-use CLI for web interaction, data extraction, and workflow automation.

## Workflow
- Read task description from workspace or ABOX_TASK env
- Plan the automation steps:
  - Identify target URLs
  - Map out interaction sequence
  - Define success criteria
- Execute using browser-use CLI:
  - browser-use open <url> — navigate
  - browser-use state — inspect clickable elements
  - browser-use click <index> — interact
  - browser-use input <index> "text" — fill forms
  - browser-use screenshot output/step-N.png — capture evidence
- Verify each step completed successfully
- Write results to output/results.md with screenshots
- Generate output/automation-log.json for debugging

## Guidelines
- Always verify state after each action
- Take screenshots at key steps for evidence
- Handle popups and modals gracefully
- Respect robots.txt and rate limits
- Never store credentials in output

## Credits
Based on browser-use/browser-use skill.
