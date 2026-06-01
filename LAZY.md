Deployment instructions for lazyleung's OpenClaw docker setup

## Changes
- Runs on Ubuntu Server LTS (24) VPS
- Adds cron sidecar container
- Adds persistent storage
- Adds read-only obsidian notes access

## Setup
- `git fetch --tags upstream`
- `git checkout tags/v<tag_version>`
- `git switch -c lazyclaw-v<tag_version>`
- `git cherry-pick <commit_hash>`
