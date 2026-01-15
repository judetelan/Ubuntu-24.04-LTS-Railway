![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04_LTS-E95420?logo=ubuntu&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-Template-0B0D0E?logo=railway&logoColor=white)
![ttyd](https://img.shields.io/badge/ttyd-1.7.7-green)

<div align="center">
  <img src="assets/ubuntu.svg" alt="Ubuntu Logo" width="120"/>
  <h1>Ubuntu 24.04 LTS Web Terminal</h1>
  <p><strong>Access a full Ubuntu terminal from your browser, anywhere.</strong></p>

  [![Deploy on Railway](https://railway.com/button.svg)](https://railway.com/deploy/Rb4lm9?referralCode=oCtTyG&utm_medium=integration&utm_source=template&utm_campaign=generic)
</div>

---

## Overview

One-click deploy a **Ubuntu 24.04 LTS (Noble Numbat)** terminal on Railway. Powered by [ttyd](https://github.com/tsl0922/ttyd), get secure, password-protected shell access from any browser.

**LTS Support**: Ubuntu 24.04 is supported until **April 2029** (standard) and **April 2034** (extended).

## Features

- **Ubuntu 24.04 LTS** - Latest Long Term Support release
- **Web Terminal** - Browser-based access via ttyd 1.7.7
- **Password Protected** - Secure authentication
- **Dev Tools Included** - Node.js, npm, Python3, Git, and more
- **Persistent Storage** - Add a Railway volume for data persistence

## Pre-installed Packages

```
wget curl git python3 python3-pip nodejs npm neofetch vim nano htop build-essential
```

## Deploy

1. Click **Deploy on Railway** above
2. Set environment variables:
   - `USERNAME` - Your login username
   - `PASSWORD` - Your login password
3. Deploy and access via the generated URL

## Environment Variables

| Variable | Required | Default | Description |
|----------|----------|---------|-------------|
| `PORT` | Auto | `8080` | Set by Railway automatically |
| `USERNAME` | Yes | - | Login username |
| `PASSWORD` | Yes | - | Login password |

## Add Persistent Storage

1. Go to your service in Railway dashboard
2. **Settings** → **Volumes**
3. Add volume with mount path: `/root`
4. Redeploy

Your home directory will persist across restarts.

## Use Cases

- Remote development environment
- Linux learning sandbox
- Script testing
- Cloud shell access from any device

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Can't connect | Wait 1-2 min for container to start |
| Login fails | Check USERNAME and PASSWORD are set |
| Data lost on restart | Add a volume at `/root` |

## Resources

- [Ubuntu 24.04 Release Notes](https://discourse.ubuntu.com/t/noble-numbat-release-notes/39890)
- [ttyd Documentation](https://github.com/tsl0922/ttyd)
- [Railway Documentation](https://docs.railway.app/)

---

<div align="center">
  <a href="https://github.com/judetelan/Ubuntu-24.04-LTS-Railway/issues">Report Bug</a>
  ·
  <a href="https://github.com/judetelan/Ubuntu-24.04-LTS-Railway/issues">Request Feature</a>
</div>
