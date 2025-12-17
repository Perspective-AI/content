---
title: "Use the Perspective AI MCP Server"
description: "Connect Perspective to Claude Desktop, Claude Code, or Cursor to create agents, analyze interviews, and deploy embeds directly from your AI assistant."
date: "2025-12-12"
tags: ["mcp", "integration", "ai-assistant", "workflow"]
nav_order: 7
nav_display: true
---

# Use the Perspective AI MCP Server

The Perspective AI MCP (Model Context Protocol) Server connects your Perspective workspace to AI assistants like Claude Desktop, Claude Code, and Cursor. Once configured, you can create conversation agents, analyze interview data, and deploy embeds without leaving your development environment.

## What You Can Do

With the MCP server connected, you can:

- **Create conversation agents** directly in your AI assistant—no need to switch to the Perspective dashboard
- **Analyze interviews from a single outline** by pulling responses and insights into your current workflow
- **Analyze interviews across multiple outlines** to identify patterns and themes across research projects
- **Deploy embeds quickly** by generating and inserting embed code directly into your codebase

## Prerequisites

- A Perspective AI workspace
- One of these AI assistants installed:
  - Claude Desktop
  - Claude Code (command-line tool)
  - Cursor IDE

## Setup

### 1. Generate Your MCP Token

Click your profile in the bottom left corner of Perspective and select **MCP** from the menu. Click **Generate Token** to create an access token.

![MCP Token page showing Generate Token button](/images/generate-mcp-token.gif "screenshot")
*Generate an access token to enable MCP integration.*

Once generated, you'll see your token along with configuration details for each supported AI assistant.

![MCP Token page showing active token and configuration options](/images/ai-ide-options.png "screenshot")
*Copy the configuration details for your AI assistant.*

### 2. Configure Your AI Assistant

**For Claude Code**, run this command in your terminal:
```bash
claude mcp add perspective --transport http https://getperspective.ai/mcp --header "Authorization: Bearer [your-token]"
```

**For Claude Desktop**, add this configuration to your Claude Desktop config file:
```json
{
  "mcpServers": {
    "perspective": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "https://getperspective.ai/mcp",
        "--header",
        "Authorization: Bearer [your-token]"
      ]
    }
  }
}
```

**For Cursor**, add this configuration to your Cursor settings:
```json
{
  "mcpServers": {
    "perspective": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "https://getperspective.ai/mcp",
        "--header",
        "Authorization: Bearer [your-token]"
      ]
    }
  }
}
```

### 3. Verify the Connection

Open your AI assistant and try a Perspective-related request, such as "Create a new interview outline for user feedback on our pricing page." If configured correctly, your assistant will connect to Perspective and execute the request.

## Example Workflows

**Create a conversation agent from your IDE:**
Ask your AI assistant: "Create a new interview outline for customer discovery on our mobile app usage patterns."

**Analyze interviews during development:**
Ask: "Pull all responses from the Q3 user research outline and summarize the top pain points."

**Compare across research projects:**
Ask: "Analyze interviews from both the onboarding outline and the pricing outline. What themes appear in both?"

**Deploy an embed while coding:**
Ask: "Generate the inline embed code for the product feedback outline and add it to the pricing page component."

## Best Practices

- **Keep tokens secure**: Treat your MCP token like a password. Rotate it if you suspect it's been compromised.
- **Use specific outline names**: When referencing outlines in requests, use exact names to ensure your assistant accesses the correct data.
- **Test with simple requests first**: Verify the connection works by creating a test outline or fetching a single interview before running complex analysis.

## Common Pitfalls & Fixes

**Issue**: AI assistant returns "unable to connect to Perspective"  
**Fix**: Verify the token is active by checking your profile menu > MCP. Check that you copied the full authorization header including "Bearer" prefix.

**Issue**: Assistant creates duplicate outlines  
**Fix**: Be specific in your requests. Instead of "create an outline," say "check if an outline named [name] exists, and if not, create it."

**Issue**: Token shows "Never" under "Last used"  
**Fix**: This updates after the first successful request. Try a simple command like "list my interview outlines" to verify the connection is working.
