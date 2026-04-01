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

## ⚡ Quick Install (Windows / Linux / macOS)

### One-Line Installation

```bash
# Clone and install
git clone https://github.com/kushalchalla981-tech/codeblazecli.git
cd codeblazecli
npm install
npm link

# Run CodeBlaze
codeblaze --help
```

### Detailed Installation

#### Windows (PowerShell)

```powershell
# 1. Clone the repository
git clone https://github.com/kushalchalla981-tech/codeblazecli.git
cd codeblazecli

# 2. Install dependencies
npm install

# 3. Link globally
npm link

# 4. Run
codeblaze --help
```

#### Linux / macOS (Terminal)

```bash
# 1. Clone the repository
git clone https://github.com/kushalchalla981-tech/codeblazecli.git
cd codeblazecli

# 2. Install dependencies
npm install

# 3. Link globally (use sudo on Linux/macOS if needed)
sudo npm link

# 4. Run
codeblaze --help
```

---

## 🔑 Get Your Free API Key

| Provider | URL | Free RPM | Best For |
|----------|-----|----------|----------|
| **Groq** | [console.groq.com](https://console.groq.com/) | 60 | Fastest responses |
| **NVIDIA** | [build.nvidia.com](https://build.nvidia.com/) | 40 | High quality |
| **OpenRouter** | [openrouter.ai](https://openrouter.ai/) | 20 | Model variety |
| **Google** | [aistudio.google.com](https://aistudio.google.com/app/apikey) | 15 | 1M context |
| **DeepSeek** | [platform.deepseek.com](https://platform.deepseek.com/) | 50+ | Reasoning |

---

## ⚙️ Configure Your API Key

#### Windows (PowerShell)
```powershell
# Temporary (current session)
$env:GROQ_API_KEY = "your-groq-key"

# Permanent - add to your PowerShell profile
notepad $PROFILE
# Add: $env:GROQ_API_KEY = "your-key"
```

#### Linux / macOS (Bash/Zsh)
```bash
# Add to ~/.bashrc or ~/.zshrc
export GROQ_API_KEY="your-groq-key"

# Reload
source ~/.bashrc  # or source ~/.zshrc
```

---

## 🚦 How to Use

```bash
# Show help
codeblaze --help

# Enable CodeBlaze mode with a provider
codeblaze on groq
codeblaze on nvidia
codeblaze on openrouter

# Enable with a preset (RECOMMENDED!)
codeblaze on premium    # 290 RPM - MAXIMUM SPEED ⭐
codeblaze on speed      # 90 RPM
codeblaze on balanced  # 65 RPM
codeblaze on coding    # 62 RPM

# Check status
codeblaze status

# Run CLI
codeblaze
```

---

## 📋 Available Presets

| Preset | Providers | RPM | Use Case |
|--------|-----------|-----|----------|
| `premium` | Groq + Cerebras + AI21 | **290** | Maximum throughput ⭐ |
| `speed` | Groq + Cerebras | 90 | Fast responses |
| `balanced` | Google + Groq + OpenRouter | 65 | Quality + speed |
| `coding` | Groq + Mistral | 62 | Code generation |
| `research` | Google + DeepSeek | 75 | Long context |
| `rag` | Cohere | 20 | Document Q&A |

---

## 🎮 Commands Reference

| Command | Description |
|---------|-------------|
| `codeblaze` | Start CLI |
| `codeblaze on` | Enable CodeBlaze mode |
| `codeblaze on <provider>` | Enable with specific provider |
| `codeblaze on <preset>` | Enable with preset |
| `codeblaze off` | Disable CodeBlaze mode |
| `codeblaze status` | Show current configuration |
| `codeblaze setup` | Run setup wizard |
| `codeblaze --help` | Show help |

---

## 🛠️ Tech Stack

- **Node.js** (18+) - Runtime environment
- **JavaScript ES6+** - CLI logic
- **npm** - Package management
- **Claude Code** - Base CLI (installed separately)

---

## ⚠️ Troubleshooting

### "claude: command not found"

Install Claude Code first:
```bash
npm install -g @anthropic-ai/claude-code
```

### "No API key configured"

Make sure you set your API key:
```bash
# Check it's set
echo $GROQ_API_KEY  # Linux/macOS
echo %GROQ_API_KEY%  # Windows
```

### Rate limit errors

Use a preset with more providers:
```bash
codeblaze on premium  # 290 RPM
```

---

## 📜 License

MIT License - Feel free to use!

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/kushalchalla981-tech">Kushal Challa</a>
</p>

<p align="center">
  🔥 CodeBlaze - Free Multi-Provider AI CLI
</p>