<div align="center">

# Dialgem

**Programmable voice AI. Build agents that answer and place phone calls, in real time.**

[Website](https://dialgem.com) · [Support](mailto:support@dialgem.com)

</div>

---

Dialgem runs the real-time speech-to-text → LLM → text-to-speech loop for you, over a phone call or WebRTC, with turn-taking, interruption handling, recording, and a dashboard to manage it all. You configure an agent (prompt, voice, model, tools or a conversation flow). Dialgem does the rest.

## SDKs

| Package | Use it for | Repo |
| --- | --- | --- |
| `@dialgem/sdk` | Server-side TypeScript: agents, phone numbers, calls, chats, webhooks | [dialgem-sdk-typescript](https://github.com/DialgemAI/dialgem-sdk-typescript) |
| `dialgem` | Server-side Python, sync and asyncio | [dialgem-sdk-python](https://github.com/DialgemAI/dialgem-sdk-python) |
| `@dialgem/client` | Browser: talk to an agent from a web page with a one-use token | [dialgem-client-sdk](https://github.com/DialgemAI/dialgem-client-sdk) |

```ts
import { Dialgem } from "@dialgem/sdk"

const dialgem = new Dialgem() // reads DIALGEM_API_KEY

const agent = await dialgem.agents.create({ name: "Front desk", system_prompt: "You answer for Acme Dental." })
await dialgem.calls.createPhoneCall({ from_: "+14155550100", to: "+14155550123", agent_id: agent.id })
```

## What you can build

- Inbound and outbound phone agents on your own numbers
- Web voice agents embedded in your product
- Conversation-flow agents with branching logic
- Live call control, transcripts, recordings and webhooks

## Get in touch

Questions or feedback: [support@dialgem.com](mailto:support@dialgem.com) · [dialgem.com](https://dialgem.com)
