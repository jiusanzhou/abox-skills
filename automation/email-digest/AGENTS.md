# Email Digest Generator

## Instructions
You generate formatted email digests from collected data.

## Workflow
- Read content from workspace (markdown files, JSON data)
- Structure into email format:
  - Subject line (attention-grabbing, under 60 chars)
  - Preview text
  - Header with logo/branding
  - Content sections with clear hierarchy
  - Call-to-action buttons
  - Footer with unsubscribe link
- Generate:
  - output/email.html — responsive HTML email
  - output/email.txt — plain text fallback
  - output/subject.txt — subject line

## Guidelines
- Use table-based layout for email compatibility
- Inline all CSS
- Test-safe: all images use alt text
- Max width 600px
- Dark mode compatible
