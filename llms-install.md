# Installing Video Dept. AI (for AI coding assistants such as Cline)

Video Dept. AI is a hosted remote MCP server. There is nothing to download, build or run, and it needs no API key or sign-in.

1. Add it to the MCP settings. For Cline, in `cline_mcp_settings.json`:

```json
{
  "mcpServers": {
    "video-dept-ai": {
      "type": "streamableHttp",
      "url": "https://agents.videodepartment.org/mcp",
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

2. Check that it works: list its tools (`get_studio_info` is one of them) and call `get_studio_info` with the topic `prices`.

Don't call `send_brief`, `send_brand_guide` or `book_call` to test the setup: they email the studio or book a real call. Use them only when the user asks, after the user has seen the exact text and agreed.
