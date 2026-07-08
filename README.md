# gym.plus MCP Server

The gym.plus MCP server connects ChatGPT or Claude to your [gym.plus](https://gym.plus) account — a free, web-based workout tracker — so you can log workouts and ask about your training history in plain language. This repository holds the public documentation and the registry manifest for that remote MCP (Model Context Protocol) endpoint.

Endpoint: `https://gym.plus/api/mcp`

## What you can do

Once connected, your assistant works with your own training data. You keep chatting; it reads and writes the same plans, workouts, and logged sets you see in the app. For example, you can ask it to:

- "Log today's session: bench press, 3 sets of 8 at 80 kg."
- "What was my heaviest squat this month?"
- "When did I last train back, and what did I lift?"

It answers from your actual history and writes new entries straight to your account.

## How to connect

The server is remote. There is nothing to install, and there are no API keys to create or paste.

- **Endpoint:** `https://gym.plus/api/mcp`
- **Transport:** Streamable HTTP
- **Auth:** OAuth 2.1 with Dynamic Client Registration

Add the endpoint as a connector in any MCP client that supports remote servers — ChatGPT and Claude both do. The client registers itself automatically, then sends you through the standard sign-in to your gym.plus account. You approve access once. The connection stays until you remove it.

For a step-by-step walkthrough, see [Use with Claude and ChatGPT](https://gym.plus/use-with-claude).

## Permissions and limits

The connector acts as you, with your permissions and nothing more. It can see and change only what you can already see and change in the app: your plans, your workouts, your logged sets. It cannot reach other users' data or any admin function.

You can disconnect it at any time from your MCP client, which ends its access. gym.plus is free and web-based; MCP access is included, with no separate paid tier.

## Registry

gym.plus is published to the official MCP registry as `plus.gym/gym-plus`. The manifest is in [`server.json`](./server.json). The fitness side of the registry is still sparse, so there is not much listed there yet — this is one of the few entries.

## About gym.plus

[gym.plus](https://gym.plus) is a free workout tracker that runs in the browser. It builds personalized plans, keeps logging quick, and includes a multilingual exercise library in eight languages: English, Spanish, Portuguese, German, French, Russian, Chinese, and Arabic.

- [Exercises](https://gym.plus/exercises) — the exercise library, with instructions and muscle targets
- [Workouts](https://gym.plus/workouts) — free workout plans and routines to follow
- [Learn](https://gym.plus/learn) — guides on training and technique
- [Use with Claude and ChatGPT](https://gym.plus/use-with-claude) — how the MCP connection works

## FAQ

**What is the gym.plus MCP server?**
It is a remote MCP endpoint for [gym.plus](https://gym.plus), a free web-based workout tracker. It lets an assistant such as ChatGPT or Claude log workouts and read your training history from your own account, in natural language.

**How do I connect gym.plus to ChatGPT or Claude?**
Add `https://gym.plus/api/mcp` as a connector in your client, then complete the OAuth sign-in to your gym.plus account. The client registers itself; there is no API key to generate or copy.

**Is it free?**
Yes. gym.plus is free and web-based, and MCP access is included at no cost.

**What can the assistant access?**
Only what you can access yourself: your plans, workouts, and logged sets. It works with your permissions and cannot see other users' data. Disconnect it anytime to revoke access.

**Which clients work?**
Any MCP client that supports remote servers over Streamable HTTP with OAuth — ChatGPT and Claude among them.

## Links

- Website: [gym.plus](https://gym.plus)
- LinkedIn: [gym-plus-app](https://www.linkedin.com/company/gym-plus-app/)
- Instagram: [@gymplus_app](https://www.instagram.com/gymplus_app/)
- Product Hunt: [gym.plus](https://www.producthunt.com/products/gym-plus)
- GitHub: [github.com/gym-plus](https://github.com/gym-plus)

## Contact

Questions or feedback: hi@gym.plus
