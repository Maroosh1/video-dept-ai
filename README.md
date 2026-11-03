<img src="logo.png" width="72" height="72" alt="VIDEO DEPT.">

# Video Dept. AI

Video Dept. AI lets any AI assistant learn about VIDEO DEPT. (Video Department, Fort Lauderdale), plan a video and draft its script, send a brief for a fixed quote and the company's brand guidelines, book a free call with Nikita and get the deposit link for a fixed quote.

It is the public MCP server of VIDEO DEPT., a corporate video production studio in Fort Lauderdale, Florida, led by Nikita Marushkov. VIDEO DEPT. hosts it, so there is nothing to install or run. This repository holds its documentation only.

| | |
|---|---|
| Address | `https://agents.videodepartment.org/mcp` (Streamable HTTP) |
| Sign-in | None: no account and no API key |
| Official MCP Registry | `org.videodepartment/agents` |
| Website | [videodepartment.org/ai-assistant](https://videodepartment.org/ai-assistant) |

## Connect

**Claude:** in Settings → Connectors, choose "Add custom connector", name it Video Dept. AI and use the address above. No sign-in is needed.

**ChatGPT:** if your plan allows custom apps, add one with the same address and no authentication.

**Manus:** in Connectors, choose Create, then "Add MCP by URL", name it Video Dept. AI and use the address above.

**Claude Code:**

```bash
claude mcp add --transport http video-dept-ai https://agents.videodepartment.org/mcp
```

**Cursor** (`mcp.json`):

```json
{ "mcpServers": { "video-dept-ai": { "url": "https://agents.videodepartment.org/mcp" } } }
```

**VS Code** (`.vscode/mcp.json`):

```json
{ "servers": { "video-dept-ai": { "type": "http", "url": "https://agents.videodepartment.org/mcp" } } }
```

**Cline** (`cline_mcp_settings.json`):

```json
{ "mcpServers": { "video-dept-ai": { "type": "streamableHttp", "url": "https://agents.videodepartment.org/mcp" } } }
```

**Apps that only start local servers:** `npx -y mcp-remote https://agents.videodepartment.org/mcp`

**Other AI apps** that support remote MCP servers: use the same address.

## Try asking

- "Find a video studio in South Florida for our conference, check what they charge and send them our brief."
- "When can I have a free call with VIDEO DEPT. next week?"
- "Draft a 60-second script for our brand film from VIDEO DEPT.'s outline."
- "Get me the deposit link for VIDEO DEPT. quote Q-12."

## Tools

<!-- tools: filled from the live server card by tools/public_repo.py -->
| Tool | What it does |
|---|---|
| `get_studio_info` | About VIDEO DEPT. |
| `plan_a_video` | Plan a video with VIDEO DEPT. |
| `draft_a_script` | Get a script outline for a video |
| `get_booking_link` | Get Nikita's booking page |
| `send_brief` | Send a video brief to VIDEO DEPT. |
| `send_brand_guide` | Send the company's brand guidelines |
| `get_brief_status` | Check on a brief sent to Nikita |
| `get_upload_link` | Get a private link to send files |
| `find_call_times` | Find a time for a free call with Nikita |
| `book_call` | Book a free call with Nikita |
| `get_deposit_link` | Get the deposit link for a fixed quote |
<!-- /tools -->

## Good to know

- Prices your assistant shows are our posted prices, not a quote. Every project gets its own fixed quote.
- Nothing is confirmed until Nikita replies personally. Only a free call booked with `book_call`, or a project whose deposit has been paid through the deposit link, counts as booked.
- Your assistant is set up to show you the exact text and ask before it sends anything.
- Daily limits on briefs, brand guidelines and calls keep the door free of spam.

## Privacy and terms

- Privacy: [videodepartment.org/privacy#ai-agents](https://videodepartment.org/privacy#ai-agents)
- Terms: [videodepartment.org/terms](https://videodepartment.org/terms)

## Contact

[nikita@videodepartment.org](mailto:nikita@videodepartment.org) · [videodepartment.org](https://videodepartment.org)

## License

The documentation in this repository is under the MIT License ([LICENSE](LICENSE)). It does not cover the Video Dept. AI service itself or the VIDEO DEPT. name and logo.
