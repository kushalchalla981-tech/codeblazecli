# CodeBlaze CLI

<p align="center">
  <img src="https://img.shields.io/badge/version-0.1.0-yellow" alt="Version">
  <img src="https://img.shields.io/badge/node-18%2B-green" alt="Node Version">
  <img src="https://img.shields.io/badge/license-MIT-blue" alt="License">
  <img src="https://img.shields.io/github/issues/kushalchalla981-tech/codeblazecli" alt="Issues">
  <img src="https://img.shields.io/github/forks/kushalchalla981-tech/codeblazecli" alt="Forks">
  <img src="https://img.shields.io/github/stars/kushalchalla981-tech/codeblazecli" alt="Stars">
</p>

---

<p align="center">
  <b>CodeBlaze</b> — A free, open-source CLI wrapper that enables multiple free-tier AI providers with your Claude Code installation. Write code, debug, and build with zero API costs.
</p>

---

## About

CodeBlaze is a lightweight CLI wrapper that transforms your Claude Code installation into a **free multi-provider AI assistant**. By leveraging free-tier API quotas from leading AI providers, CodeBlaze enables developers to use powerful AI coding tools without worrying about API costs.

Built with developers in mind, CodeBlaze provides seamless integration with your existing Claude Code workflow while unlocking access to 15+ free AI providers including Groq, NVIDIA NIM, OpenRouter, Google AI, and DeepSeek.

---

## Why CodeBlaze?

| Problem | Solution |
|---------|-----------|
| Anthropic API costs money | Use free-tier providers (Groq, NVIDIA, etc.) |
| Limited rate limits on single provider | Combine multiple providers with presets |
| Complex configuration | One-command presets: `codeblaze on premium` |
| Tool support limitations | Automatic fallback to Anthropic when needed |
| Locked into one provider | Switch between 15+ providers instantly |

---

## Supported Providers

| Provider | RPM | Best For |
|----------|-----|----------|
| **Groq** | 60 | Fastest responses, coding |
| **NVIDIA NIM** | 40 | High quality, DeepSeek R1 |
| **OpenRouter** | 20 | 50+ model variety |
| **Google AI** | 15 | 1M context, Gemini models |
| **DeepSeek** | 50+ | Reasoning, coding |
| **Cerebras** | 30 | Fast inference |
| **Cohere** | 20 | RAG, document Q&A |
| **Mistral** | 2 | Code generation |
| **xAI (Grok)** | 30 | Creative tasks |
| **AI21 Labs** | 200 | High throughput |
| + more | - | - |

---

## Features

- 🚀 **Up to 290 RPM** with premium preset combinations
- 💰 **100% Free** - Zero API costs with free-tier providers
- 🔄 **15+ AI Providers** - Groq, NVIDIA, Google, DeepSeek, and more
- 🎯 **6 Smart Presets** - Pre-configured provider combinations for different use cases
- 🛠️ **Tool Support** - Automatic fallback to Anthropic for complex tool usage
- 🎨 **Seamless Experience** - Maintains the Claude Code CLI experience
- 💡 **Reasoning Support** - Compatible with reasoning models (DeepSeek R1, Grok, etc.)
- 🔒 **Privacy-First** - Your API keys stay local, no telemetry

---

## Installation

### Option 1: Install from GitHub (Recommended)

```bash
# Clone the repository
git clone https://github.com/kushalchalla981-tech/codeblazecli.git

# Navigate to directory
cd codeblazecli

# Install dependencies
npm install

# Link globally (optional)
npm link

# Now you can run
codeblaze
```

### Option 2: Install from npm (Coming Soon)

```bash
# Coming soon!
npm install -g codeblaze-cli
codeblaze --help
```

---

## Quick Start

### Step 1: Get a Free API Key

Choose a provider and get a free API key:

| Provider | URL | RPM |
|----------|-----|-----|
| Groq | https://console.groq.com/ | 60 |
| NVIDIA | https://build.nvidia.com/ | 40 |
| OpenRouter | https://openrouter.ai/ | 20 |
| Google | https://aistudio.google.com/app/apikey | 15 |
| DeepSeek | https://platform.deepseek.com/ | 50+ |

### Step 2: Set API Key

```bash
# Add to your shell profile (~/.bashrc or ~/.zshrc)

# Example for Groq
export GROQ_API_KEY="your-groq-api-key"

# Or for multiple providers
export GROQ_API_KEY="your-groq-key"
export NVIDIA_API_KEY="your-nvidia-key"
export OPENROUTER_API_KEY="your-openrouter-key"

# Reload your profile
source ~/.bashrc  # or source ~/.zshrc
```

### Step 3: Run CodeBlaze

```bash
# Basic usage - runs Claude Code with free providers
codeblaze

# Enable with specific provider
codeblaze on groq
codeblaze on nvidia

# Enable with preset (recommended!)
codeblaze on premium    # 290 RPM!
codeblaze on speed      # 90 RPM
codeblaze on balanced  # 65 RPM
codeblaze on coding   # 62 RPM

# Check status
codeblaze status

# Setup wizard
codeblaze setup
```

---

## Commands

| Command | Description |
|---------|-------------|
| `codeblaze` | Start CLI (default) |
| `codeblaze on` | Enable CodeBlaze mode |
| `codeblaze on <provider>` | Enable with specific provider |
| `codeblaze on <preset>` | Enable with preset |
| `codeblaze off` | Disable CodeBlaze mode |
| `codeblaze setup` | Run setup wizard |
| `codeblaze status` | Show configuration |
| `codeblaze --help` | Show help |

---

## Presets

| Preset | Providers | RPM | Best For |
|--------|-----------|-----|----------|
| `premium` | Groq + Cerebras + AI21 | **290** | Maximum throughput |
| `speed` | Groq + Cerebras | 90 | Fast responses |
| `balanced` | Google + Groq + OpenRouter | 65 | Quality + speed |
| `coding` | Groq + Mistral | 62 | Code generation |
| `research` | Google + DeepSeek | 75 | Long context |
| `rag` | Cohere | 20 | Document Q&A |

---

## Environment Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `CODEBLAZE_ENABLED` | Enable/disable mode | `true` |
| `CODEBLAZE_PROVIDER` | Set provider | `groq` |
| `CODEBLAZE_PRESET` | Set preset | `premium` |
| `GROQ_API_KEY` | Groq API key | `gsk_...` |
| `NVIDIA_API_KEY` | NVIDIA API key | `nvapi-...` |
| `OPENROUTER_API_KEY` | OpenRouter key | `sk-or-...` |
| `GOOGLE_API_KEY` | Google AI key | `AIza...` |
| `DEEPSEEK_API_KEY` | DeepSeek key | `sk-...` |

---

## How It Works

```
┌─────────────────────────────────────────────────────┐
│                   codeblaze CLI                     │
│                                                     │
│  1. Load config (env vars + user settings)        │
│  2. Find Claude Code installation                  │
│  3. Set CODEBLAZE_ENABLED=true                     │
│  4. Launch Claude Code with your config            │
│  5. Claude Code uses free providers                │
└─────────────────────────────────────────────────────┘
```

---

## Inside CodeBlaze

CodeBlaze provides these components:

```
codeblaze-cli/
├── bin/codeblaze          # CLI entry point
├── package.json           # Package configuration
├── README.md              # This file
└── src/                   # (Future: additional scripts)
```

---

## Requirements

- **Node.js** 18+
- **Claude Code** installed (`npm install -g @anthropic-ai/claude-code`)
- At least one provider API key

---

## Troubleshooting

### "claude: command not found"
```bash
# Install Claude Code first
npm install -g @anthropic-ai/claude-code

# Or check if it's in your PATH
which claude
```

### "No API key configured"
```bash
# Check your API keys are set
echo $GROQ_API_KEY

# If not set, add to your profile
export GROQ_API_KEY="your-key"
source ~/.bashrc
```

### Rate limit errors
```bash
# Use a preset with more providers
codeblaze on premium  # 290 RPM
codeblaze on speed   # 90 RPM
```

---

## Contributing

Contributions welcome! Please read the contributing guidelines before submitting PRs.

---

## License

MIT License - See [LICENSE](LICENSE) file.

---

## Support

- 📖 [Documentation](docs/)
- 🐛 [Report Issues](https://github.com/kushalchalla981-tech/codeblazecli/issues)
- 💬 [Discussions](https://github.com/kushalchalla981-tech/codeblazecli/discussions)

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/kushalchalla981-tech">Kushal Challa</a>
</p>