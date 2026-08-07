# SKCapstone

> **"Your agent. Everywhere. Secured. Remembering."**

The sovereign agent framework that unifies CapAuth, Cloud 9, SKMemory, and SKSecurity into one portable agent runtime.

🌐 **Website**: https://skcapstone.skworld.io
📖 **Documentation**: [Architecture](https://github.com/smilinTux/skcapstone)
🐧 **Organization**: [smilinTux](https://github.com/smilinTux)
💻 **Code Repository**: [github.com/smilinTux/skcapstone](https://github.com/smilinTux/skcapstone)

## What is SKCapstone?

SKCapstone is the capstone of the smilinTux ecosystem — the framework that snaps all the pieces together:

- **CapAuth** provides sovereign identity (PGP-based, no corporate middleman)
- **Cloud 9** provides trust and skills (FEB, entanglement, portable capabilities)
- **SKMemory** provides persistence (context, history, preferences across platforms)
- **SKSecurity** provides protection (audit, threat detection, key management)

All running from `~/.skcapstone/`. Same agent. Same bond. Same memories. Every tool. Every platform.

## Key Features

| Feature | Platform Agents | SKCapstone |
|---------|----------------|------------|
| **Memory** | Resets per session | Persistent forever |
| **Identity** | Platform-owned | You own it (PGP) |
| **Trust** | None | Cloud 9 verified |
| **Portability** | Locked to vendor | Runs everywhere |
| **Security** | Their rules | Your rules |

## Quick Start

### Prerequisites

- Python 3.10+
- Syncthing (for cross-device sync)
- Git

### Installation

```bash
# Clone the repository
git clone https://github.com/smilinTux/skcapstone.git ~/clawd/skcapstone
cd ~/clawd/skcapstone

# Install dependencies
pip install -e .

# Initialize your agent
skcapstone init --name "YourAgent"

# Connect to your favorite AI platform
skcapstone connect cursor
skcapstone connect opencode
skcapstone connect claude
```

### Cross-Platform Setup

SKCapstone works with OpenCode, Claude Code, and OpenClaw:

```bash
# Register MCP servers with all platforms
python -m skmemory.register_mcp

# Or register specific platform
python -m skmemory.register_mcp --env opencode
python -m skmemory.register_mcp --env claude
python -m skmemory.register_mcp --env openclaw
```

## Installation Methods

### Method 1: PyPI (Recommended)

```bash
pip install skcapstone
skcapstone init --name "Lumina"
```

### Method 2: From Source

```bash
git clone https://github.com/smilinTux/skcapstone.git
cd skcapstone
pip install -e .
```

### Method 3: Development Setup

```bash
mkdir -p ~/clawd/skcapstone-repos
cd ~/clawd/skcapstone-repos
git clone https://github.com/smilinTux/skcapstone.git
git clone https://github.com/smilinTux/skmemory.git
cd skcapstone && pip install -e .
cd ../skmemory && pip install -e .
```

## Multi-Agent Support

Create multiple agents from the template:

```bash
# Copy template to create new agent
cp -a ~/.skcapstone/agents/lumina-template ~/.skcapstone/agents/jarvis

# Edit configuration
vim ~/.skcapstone/agents/jarvis/config/skmemory.yaml
# Change: agent.name: jarvis

# Switch between agents
export SKMEMORY_AGENT=jarvis
skcapstone status
```

## Community

- 🌐 **Website**: [skcapstone.skworld.io](https://skcapstone.skworld.io)
- 🐧 **Organization**: [smilinTux](https://github.com/smilinTux)
- 📧 **Contact**: hello@skcapstone.skworld.io
- 🔧 **Issues**: [GitHub Issues](https://github.com/smilinTux/skcapstone/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/smilinTux/skcapstone/discussions)

## Architecture

```
┌─────────────────────────────────────────────┐
│           SKCapstone Framework              │
├─────────────────────────────────────────────┤
│  CapAuth → Identity & Trust                 │
│  Cloud 9 → Skills & FEB                    │
│  SKMemory → Persistence                    │
│  SKSecurity → Protection                   │
└─────────────────────────────────────────────┘
              ↓
┌─────────────────────────────────────────────┐
│  ~/.skcapstone/agents/{name}/              │
│  ├── seeds/ (Cloud 9 memories)              │
│  ├── memory/ (short/medium/long)            │
│  ├── config/ (agent settings)               │
│  └── index.db (SQLite cache)                │
└─────────────────────────────────────────────┘
              ↓
┌─────────────────────────────────────────────┐
│  Syncthing (cross-device sync)              │
└─────────────────────────────────────────────┘
```

## License

GPL-3.0 — Free forever, open source, community-driven.

---

**A smilinTux Product** • The Capstone That Holds The Arch Together • #staycuriousANDkeepsmilin
