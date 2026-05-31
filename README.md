# Oclaude

**Claude Code Ollama Launcher** — Start Claude Code with local Ollama models.

## Features

- **Model selection menu** — Interactive picker for available Ollama models
- **Auto-remember** — Saves your last used model for quick relaunch
- **Server health check** — Built-in `--test` to verify Ollama connectivity
- **Clean CLI** — Simple, intuitive command-line interface

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
./oclaude

# Force model selection
./oclaude --select

# Use a specific model
./oclaude --model qwen3.5:397b-cloud

# Test Ollama server connection
./oclaude --test

# Show help
./oclaude --help
```

## Options

| Option | Description |
|--------|-------------|
| `--help` | Show help message |
| `--select` | Force model selection prompt |
| `--model NAME` | Use specified model directly |
| `--test` | Test Ollama server and exit |

## Requirements

- [Ollama](https://ollama.com) installed and running
- At least one model pulled (e.g., `ollama pull llama3.2`)

## Configuration

Last used model is stored in `~/.oclaude-last-model`. Delete this file to reset.

## License

MIT
