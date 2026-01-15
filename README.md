![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04_LTS-E95420?logo=ubuntu&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?logo=docker&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-Deploy-0B0D0E?logo=railway&logoColor=white)
![ttyd](https://img.shields.io/badge/ttyd-1.7.7-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

<div align="center">
  <img src="assets/ubuntu.svg" alt="Ubuntu Logo" width="120"/>
  <h1>Ubuntu 24.04 LTS Web Terminal</h1>
  <p><strong>Access a full Ubuntu terminal from your browser, anywhere.</strong></p>

  [![Deploy on Railway](https://railway.app/button.svg)](https://railway.com/template/4lvigd?referralCode=zkQBwB)
</div>

---

## Overview

Deploy a fully-functional **Ubuntu 24.04 LTS (Noble Numbat)** terminal accessible via web browser. Powered by [ttyd](https://github.com/tsl0922/ttyd), this template provides secure, password-protected shell access from anywhere in the world.

**LTS Support**: Ubuntu 24.04 is supported until **April 2029** (standard) and **April 2034** (extended).

## Features

| Feature | Description |
|---------|-------------|
| **Ubuntu 24.04 LTS** | Latest Long Term Support release |
| **Web Terminal** | Access via browser using ttyd 1.7.7 |
| **Password Protected** | Secure authentication required |
| **Dev Tools Included** | Node.js, npm, Python3, Git, and more |
| **Persistent Storage** | Optional Railway volume support |
| **Instant Deploy** | One-click Railway deployment |

## Pre-installed Packages

```
wget curl git python3 python3-pip nodejs npm neofetch vim nano htop build-essential
```

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `PORT` | Yes | Port for ttyd (Railway sets automatically) |
| `USERNAME` | Yes | Login username for web terminal |
| `PASSWORD` | Yes | Login password for web terminal |

> **Security**: Always set `USERNAME` and `PASSWORD` before deploying to production.

## Quick Start

### Deploy to Railway

1. Click the **Deploy on Railway** button above
2. Set environment variables:
   - `USERNAME`: Your preferred username
   - `PASSWORD`: A strong password
3. Deploy and access via the generated Railway URL

### Run Locally

```bash
docker build -t ubuntu-webterminal .
docker run -p 8080:8080 -e PORT=8080 -e USERNAME=admin -e PASSWORD=secret ubuntu-webterminal
```

Access at `http://localhost:8080`

## Use Cases

- **Remote Development** - Access a Linux environment from any device
- **Learning Linux** - Practice commands in a safe environment
- **Script Testing** - Test bash scripts without local setup
- **CI/CD Staging** - Quick environment for testing deployments
- **Cloud Shell** - Personal cloud terminal accessible anywhere

## Architecture

```
┌─────────────────────────────────────────────┐
│                  Browser                     │
└─────────────────┬───────────────────────────┘
                  │ HTTPS
┌─────────────────▼───────────────────────────┐
│              Railway                         │
│  ┌────────────────────────────────────────┐ │
│  │         ttyd (Port 8080)               │ │
│  │  ┌──────────────────────────────────┐  │ │
│  │  │     Ubuntu 24.04 LTS Shell       │  │ │
│  │  │  • bash • python3 • node • git   │  │ │
│  │  └──────────────────────────────────┘  │ │
│  └────────────────────────────────────────┘ │
│                    │                         │
│  ┌─────────────────▼──────────────────────┐ │
│  │        Volume (Optional /root)         │ │
│  └────────────────────────────────────────┘ │
└─────────────────────────────────────────────┘
```

## Adding Persistent Storage

In Railway dashboard:
1. Go to your service → **Settings** → **Volumes**
2. Add volume with mount path: `/root`
3. Redeploy

Your home directory will now persist across restarts.

## Extending the Image

Fork this repo and modify the Dockerfile:

```dockerfile
# Add more packages
RUN apt-get update && apt-get install -y \
    your-package-here \
    another-package

# Or install from npm
RUN npm install -g your-global-package
```

## Troubleshooting

| Issue | Solution |
|-------|----------|
| "Application failed to respond" | Check PORT env var is set |
| Can't login | Verify USERNAME and PASSWORD are set |
| Packages not found | Run `apt-get update` first |
| Permission denied | Use `sudo` or run as root |

## Resources

- [Ubuntu 24.04 Release Notes](https://discourse.ubuntu.com/t/noble-numbat-release-notes/39890)
- [ttyd Documentation](https://github.com/tsl0922/ttyd)
- [Railway Documentation](https://docs.railway.app/)

## License

MIT License - Feel free to use, modify, and distribute.

---

<div align="center">
  <p>Made with Ubuntu + ttyd + Railway</p>
  <p>
    <a href="https://github.com/judetelan/Ubuntu-24.04-LTS-Railway/issues">Report Bug</a>
    ·
    <a href="https://github.com/judetelan/Ubuntu-24.04-LTS-Railway/issues">Request Feature</a>
  </p>
</div>
