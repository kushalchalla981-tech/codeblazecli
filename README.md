# CodeBlaze CLI

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=FFD700&height=300&section=header&text=CodeBlaze&fontSize=90&animation=fadeIn&fontAlignY=35" width="100%" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-0.1.0-yellow" alt="Version">
  <img src="https://img.shields.io/badge/node-18%2B-green" alt="Node Version">
  <img src="https://img.shields.io/badge/license-MIT-blue" alt="License">
  <img src="https://img.shields.io/github/last-commit/kushalchalla981-tech/codeblazecli" alt="Last Commit">
  <img src="https://img.shields.io/github/issues/kushalchalla981-tech/codeblazecli" alt="Issues">
</p>

<p align="center">
  🔥 A lightweight CLI wrapper that enables free AI providers with your Claude Code installation. Write code, debug, and build with zero API costs.
</p>

---

## ✨ Features

- 🚀 **Up to 290 RPM** with premium preset combinations
- 💰 **100% Free** - Zero API costs with free-tier providers  
- 🔄 **15+ AI Providers** - Groq, NVIDIA, Google, DeepSeek, and more
- 🎯 **6 Smart Presets** - Pre-configured provider combinations
- 🛠️ **Tool Support** - Automatic fallback to Anthropic for complex tasks
- 🎨 **Seamless Experience** - Maintains the Claude Code CLI interface
- 💡 **Reasoning Support** - Compatible with DeepSeek R1, Grok, and more
- 🔒 **Privacy-First** - Your API keys stay local, no telemetry

---

## 🛠️ Tech Stack

- **Node.js** (18+) - Runtime environment
- **JavaScript ES6+** - CLI logic
- **npm** - Package management
- **Claude Code** - Base CLI (installed separately)

---

## 🚀 Getting Started

### Prerequisites

- Node.js 18 or higher installed
- Claude Code installed (`npm install -g @anthropic-ai/claude-code`)
- A free API key from one of the supported providers

### Installation

#### Windows

```powershell
# 1. Clone the repository
git clone https://github.com/kushalchalla981-tech/codeblazecli.git
cd codeblazecli

# 2. Install dependencies
npm install

# 3. Link globally (optional)
npm link

# 4. Run CodeBlaze
codeblaze --help
```

**Alternative (without git):**
1. Download the repository as ZIP
2. Extract to a folder
3. Open PowerShell in that folder
4. Run `npm install` then `npm link`

#### Linux

```bash
# 1. Clone the repository
git clone https://github.com/kushalchalla981-tech/codeblazecli.git
cd codeblazecli

# 2. Install dependencies
npm install

# 3. Link globally
sudo npm link

# 4. Make executable (optional)
chmod +x bin/codeblaze

# 5. Run CodeBlaze
codeblaze --help
```

**Installation paths:**
- Global: `/usr/local/lib/node_modules/`
- User: `~/.npm-global/lib/node_modules/`

#### macOS

```bash
# 1. Clone the repository  
git clone https://github.com/kushalchalla981-tech/codeblazecli.git
cd codeblazecli

# 2. Install dependencies
npm install

# 3. Link globally
sudo npm link

# 4. Run CodeBlaze
codeblaze --help
```

**Note:** On macOS, you may need to add npm's global bin to your PATH:
```bash
export PATH="$PATH:$(npm root -g)/../bin"
```
Add this to your `~/.zshrc` or `~/.bash_profile`.

---

## 📋 Quick Usage Guide

### 1. Get a Free API Key

| Provider | URL | RPM | Best For |
|----------|-----|-----|----------|
| **Groq** | [console.groq.com](https://console.groq.com/) | 60 | Fastest responses |
| **NVIDIA** | [build.nvidia.com](https://build.nvidia.com/) | 40 | High quality |
| **OpenRouter** | [openrouter.ai](https://openrouter.ai/) | 20 | Model variety |
| **Google** | [aistudio.google.com](https://aistudio.google.com/app/apikey) | 15 | 1M context |
| **DeepSeek** | [platform.deepseek.com](https://platform.deepseek.com/) | 50+ | Reasoning |

### 2. Set Your API Key

#### Windows (PowerShell)
```powershell
# Temporary (current session only)
$env:GROQ_API_KEY = "your-groq-key"

# Permanent
# Add to your PowerShell profile:
notepad $PROFILE
# Add: $env:GROQ_API_KEY = "your-key"
```

#### Windows (Command Prompt)
```cmd
set GROQ_API_KEY=your-groq-key
```

#### Linux/macOS (Bash/Zsh)
```bash
# Add to ~/.bashrc or ~/.zshrc
export GROQ_API_KEY="your-groq-key"
export NVIDIA_API_KEY="your-nvidia-key"

# Reload profile
source ~/.bashrc  # or source ~/.zshrc
```

### 3. Run CodeBlaze

```bash
# Show help
codeblaze --help

# Enable with specific provider
codeblaze on groq
codeblaze on nvidia
codeblaze on openrouter

# Enable with preset (recommended!)
codeblaze on premium    # 290 RPM - MAXIMUM SPEED
codeblaze on speed      # 90 RPM
codeblaze on balanced   # 65 RPM
codeblaze on coding    # 62 RPM

# Check status
codeblaze status

# Run Claude Code with CodeBlaze enabled
codeblaze
```

---

## 🎮 Controls

| Command | Description |
|---------|-------------|
| `codeblaze` | Start CLI with CodeBlaze mode |
| `codeblaze on` | Enable CodeBlaze mode |
| `codeblaze on <provider>` | Enable with specific provider |
| `codeblaze on <preset>` | Enable with preset |
| `codeblaze off` | Disable CodeBlaze mode |
| `codeblaze status` | Show current configuration |
| `codeblaze setup` | Run setup wizard |
| `codeblaze --help` | Show help message |

---

## 📁 Project Structure

```
codeblazecli/
├── bin/
│   └── codeblaze          # CLI entry point
├── package.json           # Package configuration
├── README.md              # This file
├── LICENSE                # MIT License
└── src/                   # (Future: additional modules)
    └── index.js
```

---

## 🎯 Presets Guide

| Preset | Providers | RPM | Use Case |
|--------|-----------|-----|----------|
| `premium` | Groq + Cerebras + AI21 | **290** | Maximum throughput |
| `speed` | Groq + Cerebras | 90 | Fast responses |
| `balanced` | Google + Groq + OpenRouter | 65 | Quality + speed |
| `coding` | Groq + Mistral | 62 | Code generation |
| `research` | Google + DeepSeek | 75 | Long context |
| `rag` | Cohere | 20 | Document Q&A |

---

## 🔧 Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `CODEBLAZE_ENABLED` | No | Set to "true" to enable |
| `CODEBLAZE_PROVIDER` | No | Provider name (groq, nvidia, etc.) |
| `CODEBLAZE_PRESET` | No | Preset name (premium, speed, etc.) |
| `GROQ_API_KEY` | Yes* | Groq API key (*if using Groq) |
| `NVIDIA_API_KEY` | Yes* | NVIDIA API key (*if using NVIDIA) |
| `OPENROUTER_API_KEY` | Yes* | OpenRouter API key (*if using OpenRouter) |
| `GOOGLE_API_KEY` | Yes* | Google AI API key (*if using Google) |
| `DEEPSEEK_API_KEY` | Yes* | DeepSeek API key (*if using DeepSeek) |

---

## ⚠️ Troubleshooting

### "claude: command not found"

**Windows:**
```powershell
npm install -g @anthropic-ai/claude-code
```

**Linux/macOS:**
```bash
sudo npm install -g @anthropic-ai/claude-code
```

### "No API key configured"

Check your API key is set:
```bash
echo $GROQ_API_KEY  # Linux/macOS
echo %GROQ_API_KEY%  # Windows
```

### Rate limit errors

Use a preset with more providers:
```bash
codeblaze on premium  # 290 RPM
```

### PATH issues (Linux/macOS)

Add npm global bin to PATH:
```bash
export PATH="$PATH:$(npm root -g)/../bin"
```

---

## 📜 License

MIT License - Feel free to use this for learning and personal projects!

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/kushalchalla981-tech">Kushal Challa</a>
</p>

<p align="center">
  🔥 CodeBlaze - Free Multi-Provider AI CLI
</p>