---
title: 'Enable Image Vision in Claude Code CLI with DeepSeek V4 API'
date: 2026-05-25
permalink: /posts/2026/05/enable-image-vision-in-claude-code-cli-with-deepseek-v4-api/
tags:
  - cool posts
  - category1
  - category2
---

If you want Claude Code CLI to understand images while using the DeepSeek V4 API, ask Claude to install the vision skill first:

    Install this skill for Claude Code CLI:
    https://github.com/asuojun/claude-vision-skill

Then ask Claude to update the API endpoint to the DashScope compatible endpoint:

    Replace the API URL with:
    https://dashscope-intl.aliyuncs.com/compatible-mode/v1

Next, provide your API key directly in Claude Code CLI when prompted.

Finally, ask Claude:

    增加 max_token 到4096

You can also give Claude the whole instruction in one shot:

    Install the skill https://github.com/asuojun/claude-vision-skill
    Replace the API URL with https://dashscope-intl.aliyuncs.com/compatible-mode/v1
    I will provide the API key in CLI
    增加 max_token 到4096