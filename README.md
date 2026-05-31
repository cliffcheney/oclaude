# oclaude

**Claude Code Ollama Launcher** — Start Claude Code with local Ollama models.

## Features

- **Model selection menu** — Interactive picker for available Ollama models
- **Auto-remember** — Saves your last used model for quick relaunch
- **Server health check** — Built-in `--test` to verify Ollama connectivity

## Installation

```bash
# Clone or copy the oclaude script
chmod +x oclaude

# Optional: add to your PATH
sudo ln -s $(pwd)/oclaude /usr/local/bin/oclaude
```

## Usage

```bash
# Use last model (or prompt if none saved)
oclaude

# Force model selection (short flag)
oclaude -s

# Use a specific model (short flag)
oclaude -m llama3.2

# Use a specific model with tag (long flag)
oclaude --model codellama:7b

# Test Ollama server and Claude Code
oclaude -t

# Forget saved model preference
oclaude --reset

# Show help
oclaude -h
```

## Options

| Option | Description |
|--------|-------------|
| `--help` | Show help message |
| `--select` | Force model selection prompt |
| `--model NAME` | Use specified model directly |
| `--test` | Test Ollama server and Claude Code and exit |

## Requirements

- [Ollama](https://ollama.com) installed and running
- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) CLI installed
- At least one model pulled (e.g., `ollama pull llama3.2`)

## Configuration

Last used model is stored in `~/.oclaude-last-model`. Delete this file to reset.

## License

MIT
