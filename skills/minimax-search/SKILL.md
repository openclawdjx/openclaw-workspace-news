---
name: minimax-search
description: Use MiniMax MCP for web search and image understanding. Triggers when user needs to: (1) Search the web for information, (2) Analyze or understand images, (3) Get answers from images. Requires MiniMax Coding Plan API key.
---

# MiniMax Search & Image Understanding

Use the MiniMax MCP server for web search and image understanding tasks.

## Tools

### web_search
Search the web for information.

| Parameter | Type   | Required | Description     |
|-----------|--------|----------|-----------------|
| query     | string | ✓       | Search query    |

### understand_image
Analyze and understand images.

| Parameter | Type   | Required | Description                      |
|-----------|--------|----------|-----------------------------------|
| prompt    | string | ✓       | Question or analysis request     |
| image_url | string | ✓       | Image URL (HTTP/HTTPS) or local file path |

**Supported formats**: JPEG, PNG, GIF, WebP (max 20MB)

## Setup

1. Get API key from https://platform.minimaxi.com/subscribe/coding-plan
2. Install uvx if not already: `curl -LsSf https://astral.sh/uv/install.sh | sh`
3. Add MCP to your client:

```bash
claude mcp add -s user MiniMax --env MINIMAX_API_KEY=your_api_key --env MINIMAX_API_HOST=https://api.minimaxi.com -- uvx minimax-coding-plan-mcp -y
```

## Usage

When user asks to search something or analyze an image, use these tools directly.

