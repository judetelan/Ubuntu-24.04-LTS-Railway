# Ubuntu 24.04 LTS Web Terminal

Access a full Ubuntu terminal from your browser. Anywhere. Anytime.

## What You Get

- **Ubuntu 24.04 LTS** - Latest Long Term Support (supported until 2029)
- **Web-based Terminal** - No SSH needed, just open in browser
- **Password Protected** - Secure login required
- **Dev Tools Pre-installed** - Node.js, npm, Python3, Git, and more
- **Persistent Storage** - Your files survive restarts

## Pre-installed

```
nodejs npm python3 git curl wget vim nano htop build-essential neofetch
```

## Quick Setup

1. Set `USERNAME` - your login name
2. Set `PASSWORD` - your login password
3. Deploy and access via the generated URL

## Use Cases

**Remote Development** - Code from any device with a browser

**Cloud Shell** - Personal Linux environment in the cloud

**Learning** - Safe sandbox to practice Linux commands

**CI/CD** - Quick environment for testing scripts

## Technical Details

| Component | Version |
|-----------|---------|
| Ubuntu | 24.04 LTS (Noble Numbat) |
| ttyd | 1.7.7 |
| Node.js | Latest LTS |
| Python | 3.x |

## Adding More Tools

Once deployed, install anything via apt:

```bash
sudo apt update && sudo apt install <package>
```

Or npm:

```bash
npm install -g <package>
```

## Persistent Storage

Volume mounted at `/root` - your home directory persists across restarts and redeploys.

---

**Support**: [GitHub Issues](https://github.com/judetelan/Ubuntu-24.04-LTS-Railway/issues)
