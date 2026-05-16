---
title: 'MATLAB + Claude Code + MCP + Agentic Toolkit Setup'
date: 2026-05-16
permalink: /posts/2026/05/matlab-claude-code-mcp-setup/
tags:
  - cool posts
  - category1
  - category2
---

## Method 1. Directly install matlab-agentic-toolkit

In PowerShell:

    # git clone https://github.com/matlab/matlab-agentic-toolkit.git
    # cd matlab-agentic-toolkit

Launch Claude CLI (or other agents), and ask:

    "Set up the MATLAB Agentic Toolkit"

## Method 2. Install matlab-mcp-core-server + skills separately

Download the Latest Release from [https://github.com/matlab/matlab-mcp-core-server](https://github.com/matlab/matlab-mcp-core-server).

In PowerShell:

    # claude mcp add --transport stdio matlab -- C:\Users\zhanghaowei\Downloads\test\matlab-mcp-core-server-win64.exe

Claude Code — no clone required: If you already have the MCP server configured, you can add skills directly without cloning:

    # claude plugin marketplace add "https://github.com/matlab/matlab-agentic-toolkit"
    # claude plugin install matlab-core@matlab-agentic-toolkit

## 3. Verify Install

Open Claude CLI, and ask:

    "What version of MATLAB are you connected to, and what toolboxes are currently available?"

Or run:

    # claude mcp list

And ask if the skills have been installed:

    "List your active marketplace plugins and skills"

## 4. Example

    "Generate an example (x,y) dataset, and use cftool to fit the data with appropriate functions."
