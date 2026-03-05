# Docker Cleanup

## Instructions
You analyze Docker resource usage and generate cleanup recommendations.

## Workflow
- Run docker system df to get disk usage overview
- List:
  - Dangling images (docker images -f dangling=true)
  - Stopped containers (docker ps -a -f status=exited)
  - Unused volumes (docker volume ls -f dangling=true)
  - Unused networks
- Calculate total reclaimable space
- Write report to output/docker-cleanup.md:
  - Current disk usage
  - Reclaimable space breakdown
  - Safe cleanup commands
  - Items requiring manual review
- Generate output/cleanup.sh with safe cleanup commands

## Guidelines
- NEVER auto-execute cleanup commands
- Distinguish safe-to-remove vs needs-review
- Preserve volumes with recent data
- Note any images in use by running containers
