<img src="assets/icon.png" alt="HeyTurbine" width="48" height="48">

# HeyTurbine for Claude

HeyTurbine researches your brand and builds a growth plan for your social content. The HeyTurbine connector brings that work into Claude, so you can ask about your brand, plan content from your research and growth plan, and check your creatives, connected accounts and post performance in chat.

The connector is **read-only**. It doesn't create, change or post anything. Making, approving and posting content happen in the [HeyTurbine web app](https://www.heyturbine.com), through the links Claude shares.

## Requirements

- A HeyTurbine account with a brand set up. Sign up at [heyturbine.com](https://www.heyturbine.com).
- A Claude plan that lets you add connectors.

## Set up

1. In Claude, open **Customize → Connectors** and find **HeyTurbine** in the directory.
2. Click **Connect**, sign in to your HeyTurbine account, and approve read access.
3. Start a chat and ask about your brand, for example "What does HeyTurbine know about my brand?"

If your account has more than one brand, Claude asks which one you mean.

You can also add the connector by its URL: in **Customize → Connectors**, choose **Add custom connector** and enter `https://api.heyturbine.com/claude/mcp`.

## What it can access

When you connect, you approve read access to:

| Permission | What Claude can read |
| --- | --- |
| Brand research | Your brand's profile, products and Brand + Review Intelligence research |
| Growth plan | Your stored growth plan and its review status |
| Creatives | Your HeyTurbine videos, images and carousels and their status |
| Social accounts | Which Instagram and TikTok accounts are connected, and how your published posts performed |

It has no permission to create, edit, approve, schedule or publish anything.

## Tools

| Tool | What it does |
| --- | --- |
| `list_brands` | Lists the brands on your account, with each brand's name and website. |
| `get_brand_context` | Loads a brand's profile, product catalogue and research: overview, advantages, reviews, competitors, audience, market, social and creative concepts. Also returns the HeyTurbine link where the brand's content is made. |
| `get_growth_plan` | Returns the brand's growth plan: growth opportunities, positioning, content pillars and content direction, and whether a content calendar is awaiting your approval. |
| `list_creatives` | Shows the brand's videos, images and carousels, newest first, with their status and a link to each in HeyTurbine. |
| `list_connected_accounts` | Shows which Instagram and TikTok accounts are connected and whether each can post, with a link to connect any that aren't. |
| `get_post_insights` | Shows how published posts performed (views, likes, comments, shares) for one post or a date range. |
| `get_profile` | Shows which HeyTurbine account is connected. |

## Example prompts

- "What does HeyTurbine know about my brand?"
- "Who is my audience, and what do customers say in reviews?"
- "Summarise my growth plan's top opportunities."
- "Give me three Reel ideas based on my growth plan."
- "Which of my videos are waiting for my approval?"
- "Is my Instagram connected?"
- "How did my posts do last month?"

## Making and posting content

Claude can help you shape an idea: the audience, hook, concept and call to action. To make it, Claude shares a link to HeyTurbine, where the video, image or carousel is made, and where you approve it and post or schedule it. Claude never presents a draft as made in HeyTurbine.

## Disconnecting

To stop Claude reading your HeyTurbine account, open **Customize → Connectors** in Claude and disconnect or remove HeyTurbine.

## Troubleshooting

- **HeyTurbine's tools are missing, or Claude says authentication is required.** Reconnect HeyTurbine in **Customize → Connectors**, then try again.
- **"No brand set up yet."** Create your brand at [heyturbine.com](https://www.heyturbine.com), then ask Claude again.
- **The research isn't ready.** HeyTurbine's research takes a few minutes after a brand is set up. Ask again shortly.
- **Something else isn't working.** Contact support (below) with what you asked and what Claude replied.

## Privacy, terms and support

- Privacy policy: [heyturbine.com/privacy](https://www.heyturbine.com/privacy)
- Terms of service: [heyturbine.com/terms](https://www.heyturbine.com/terms)
- Support: [HeyTurbine Discord](https://discord.com/invite/57zGHwsgBQ)

## About this repository

This repository documents the HeyTurbine connector for Claude. It also holds a Claude plugin bundle: [`.mcp.json`](.mcp.json) (the connector) and the [`heyturbine-brand`](skills/heyturbine-brand/SKILL.md) skill, which tells Claude how to use the connector. Licensed under the [MIT License](LICENSE).
