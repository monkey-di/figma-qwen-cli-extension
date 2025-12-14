# Figma Extension for Qwen CLI

Integrate Figma into your Qwen CLI workflow using the community MCP server.

## Installation

```bash
qwen extensions install https://github.com/monkey-di/figma-qwen-cli-extension
```

Or install locally:
```bash
qwen extensions install /path/to/figma-qwen-cli-extension
```

## Setup

1. Get your Figma Personal Access Token:
   - Go to https://www.figma.com/developers/api#access-tokens
   - Click "Get personal access token"
   - Copy the token

2. Set the environment variable:

**Linux/macOS:**
```bash
export FIGMA_API_KEY="your_figma_token_here"
```

Add to `~/.bashrc` or `~/.zshrc` to make it permanent:
```bash
echo 'export FIGMA_API_KEY="your_figma_token_here"' >> ~/.bashrc
source ~/.bashrc
```

**Windows:**
```cmd
setx FIGMA_API_KEY "your_figma_token_here"
```

3. Restart Qwen CLI to pick up the environment variable

## Available Tools

- `download_figma_images` - Download images from Figma files
- `get_figma_data` - Get design data from Figma

## Limitations

This extension uses the community MCP server which has limited functionality compared to the official Figma MCP server. The official server is only available on macOS/Windows desktop apps with whitelisted clients (Gemini CLI, Claude Code, Cursor, VS Code).

## Security Note

**NEVER commit your Figma API token to version control.** Always use environment variables.
