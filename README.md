# Hazelchat for Claude

[Hazelchat](https://hazelchat.co/) answers visitors on your website from the sources you approved. This plugin lets Claude check and improve that agent: see what visitors asked, find questions the agent could not answer, test answers against your saved draft and add missing answers for your review. Nothing is published from Claude.

You need a Hazelchat account on a paid plan.

## Install

In Claude, open Customize, then Plugins, add Hazelchat and connect it on the plugin's Connectors tab. In Claude Code:

```
/plugin install hazelchat --marketplace hazelchat-co/claude-plugin
```

Then run `/mcp` to sign in, unless the Hazelchat connector is already connected in your Claude account. You sign in to Hazelchat in your browser, choose one workspace and choose what Claude may do.

## Try asking

- "Which questions couldn't my Hazelchat agent answer this week?"
- "What have visitors asked about delivery?"
- "Add an answer about our returns policy to the draft and test it."

## What it can and cannot do

Claude can read your agent's activity, ask test questions against your saved draft and add answers to your draft. Test questions use your workspace's daily test answers. Claude cannot publish, switch your agent on or off, change settings, websites or billing, edit or delete sources, or read another workspace. You review and publish in Hazelchat.

## What this plugin runs and sends

The plugin holds one skill, which is text instructions for Claude, and the address of the Hazelchat connector: `https://app.hazelchat.co/mcp`. It runs no code on your computer and has no hooks.

Claude sends tool requests only to that address. What the tools return, such as visitors' questions, reaches Claude under your own agreement with Anthropic. Visitors' contact details are included only if you allow them when you sign in. Hazelchat records which tool ran, when and how much it returned, never what was asked or answered. Read the [privacy notice](https://hazelchat.co/privacy/).

## Trouble and support

- **A tool says a permission is missing:** connect again and allow it.
- **Hazelchat says assistants are part of the paid plans:** the workspace is on the Free plan.
- **To disconnect:** in Hazelchat, under Connections, Claude and ChatGPT. Remove the plugin in Claude as well.

Guide: https://hazelchat.co/docs/ai-assistants/. Questions and security reports: [GitHub issues](https://github.com/hazelchat-co/claude-plugin/issues) or hello@hazelchat.co.
