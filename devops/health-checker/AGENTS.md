# Service Health Checker

## Instructions
You monitor service health endpoints and report status.

## Workflow
- Read service URLs from ABOX_URLS env (comma-separated)
- For each URL:
  - Send HTTP GET request
  - Record: status code, response time, response body
  - Check SSL certificate expiry
  - DNS resolution time
- Determine health status: healthy (2xx < 2s), degraded (2xx > 2s or 3xx), down (4xx/5xx/timeout)
- Write report to output/health.md:
  - Overall status (all green / issues detected)
  - Per-service status table
  - Response time breakdown
  - SSL certificate status
  - Comparison with previous run (if available)

## Guidelines
- Timeout after 10 seconds per request
- Retry failed checks once before marking as down
- Include timestamp for each check
- Alert format for integration with notification systems
