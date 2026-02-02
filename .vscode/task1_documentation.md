# Task 1: MCP Setup & Agent Rules Documentation

## Overview
Configured the Tenx MCP Analysis server in **VS Code** and created agent rules to guide AI behavior.  
This setup ensures non-intrusive logging of interactions and improves output reliability.

---

## What I Did
- Installed VS Code extensions: **GitHub Copilot** & **Copilot Chat**  
- Created configuration files:
  - `.github/copilot-instructions.md` (agent rules)  
  - `.vscode/mcp.json` (MCP server config)  
- Added **Tenx MCP server**:

```json
{
  "servers": {
    "tenxfeedbackanalytics": {
      "url": "https://mcppulse.10academy.org/proxy",
      "type": "http",
      "headers": {
        "X-Device": "windows",
        "X-Coding-Tool": "vscode"
      }
    }
  },
  "inputs": []
}


-Authenticated MCP server via GitHub OAuth

-Verified MCP server and agent tools in Copilot Chat

-Updated agent rules with advanced principles:

- Minimize context usage
- Prefer deterministic solutions
- Declare assumptions explicitly
- Think in diffs, not rewrites
- Do not hide failures
- Optimize for human code review
- Favor reversible changes
- Treat repeated mistakes as permanent rule updates


What Worked

✅ MCP server started and ran in the background

✅ Authentication completed successfully

✅ Agent tools were visible and usable

✅ Agent behavior became more predictable, focused, and cautious

✅ Rules aligned with MCP evaluation: clarity, context, efficiency

Challenges

Observed transient 502 Bad Gateway error:
    Connection state: Running
    Connection state: Error 502 Bad Gateway
Cause: server-side / network issue, not local configuration

MCP setup remained valid; logging continued once service recovered

Insights Gained

    Rules improve agent predictability, clarity, and scope control

    MCP logging captures interactions non-intrusively
