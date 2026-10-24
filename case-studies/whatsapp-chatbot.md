# WhatsApp chatbot
Node.js personal assistant prototype.

[Original repository](https://github.com/MANTHAN137/Whatsapp_agent) · [Later UltimateManthanBot](https://github.com/MANTHAN137/UltimateManthanBot)

## Verified implementation
The original project's event handler connects Baileys messages to a Gemini service. It distinguishes direct and group messages, checks mentions/quoted replies, and pauses per chat when the owner replies. Explicit resume/pause commands control that state.

The AI service tries configured Gemini model endpoints and falls back to local knowledge matching, quick responses and NLP. Conversation context is bounded and held in memory in this version.

The later bot repository adds a SQLite-backed memory module and a router for chat, search, links, translation, reminders and tasks. Its README and router describe different versions, so this showcase claims only the inspected modules.

## Relevant client work
Chat interfaces with per-conversation state, API-backed replies, human takeover and deterministic utility routing.

## Scope
Code was inspected on 25 October 2026; no account was connected or live message sent for this showcase. No customer deployment, response-time benchmark or official WhatsApp Business Cloud API implementation is claimed. Business delivery would need an agreed platform integration and clear identification of automated replies. Personal configuration, conversation data and sessions are not reproduced here.

## Code references
- [Incoming-message and takeover logic](https://github.com/MANTHAN137/Whatsapp_agent/blob/main/bot.js)
- [Gemini integration and fallback paths](https://github.com/MANTHAN137/Whatsapp_agent/blob/main/src/services/ai-service.js)
- [Conversation state](https://github.com/MANTHAN137/Whatsapp_agent/blob/main/src/services/conversation-service.js)
- [Later routing module](https://github.com/MANTHAN137/UltimateManthanBot/blob/main/src/brains/brain-router.js)
- [Later persistent memory module](https://github.com/MANTHAN137/UltimateManthanBot/blob/main/src/memory/memory-store.js)
