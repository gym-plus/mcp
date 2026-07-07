# Gym Plus MCP Server

**Connect [ChatGPT](https://chatgpt.com) or [Claude](https://claude.ai) to your [Gym Plus](https://gym.plus) account — log workouts and review your training history in plain language, from inside the assistant you already use.**

[Gym Plus](https://gym.plus) is an AI-powered workout tracker. It ships a remote **Model Context Protocol (MCP)** server so any MCP-compatible AI client can securely read and write *your* real training data.

## What you can do

- **Log a workout** — *"log today's push day: bench 3×8 at 80 kg, incline DB press 3×10…"*
- **Review your history** — *"what's my squat PR?"*, *"how many sessions this month?"*
- **Get coaching over your own data** — *"what should I train next and why?"*

## Connect it

The server is a remote, OAuth-authenticated MCP endpoint:

```
https://gym.plus/api/mcp
```

- **Transport:** Streamable HTTP
- **Auth:** OAuth 2.1 with Dynamic Client Registration — you sign in to your Gym Plus account and approve access. No API keys to copy around.

Add it in any MCP client that supports remote servers (Claude, ChatGPT, and others) using the URL above. The registry manifest lives in [`server.json`](./server.json) and is published to the [official MCP Registry](https://registry.modelcontextprotocol.io) as **`plus.gym/gym-plus`**.

## About Gym Plus

[**Gym Plus**](https://gym.plus) is a free, web-based AI workout tracker: personalized training plans, effortless progress logging, and a multilingual [exercise library](https://gym.plus/exercises) in 8 languages.

- 🌐 Website — https://gym.plus
- 🏋️ Exercise library — https://gym.plus/exercises
- 📋 Workout plans — https://gym.plus/workouts
- 📚 Guides — https://gym.plus/learn

---

_Questions or feedback? **hi@gym.plus**_
