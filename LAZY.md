Deployment instructions for lazyleung's OpenClaw docker setup

## Changes
- Runs on Ubuntu Server LTS (24) VPS
- Adds cron sidecar container
- Adds persistent storage
- Adds read-only obsidian notes access

## Scenarios
Checkout latest release tag and replay changes on top
- `git fetch --tags upstream`
- `git checkout tags/v<tag_version>`
- `git switch -c lazyclaw-v<tag_version>`
- `git cherry-pick <commit_hash>` (TODO Look into squashing changes)
Build and upload image to server
- Set OPENCLAW_IMAGE env to `lazyclaw:latest`
- `docker compose build`
- `docker save -o lazyclaw.tar lazyclaw:latest`
- Use powershell to access 1password ssh key `scp lazyclaw.tar <user>@<ip>:~`