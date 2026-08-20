# Telegram Inventory Bot

> An AI-powered Telegram bot that helps customers find products, check stock, and browse inventory using RAG (Retrieval-Augmented Generation).

---

## 📸 Demo

![Bot Demo](./demo.gif)

---

## 🚀 Features

- **Semantic Product Search** — Uses Pinecone vector search + Google Gemini embeddings
- **Real-time Stock Lookup** — Google Sheets as inventory database
- **Intent Routing** — LLM classifier routes to inventory list, product search, help, or fallback
- **Product Images** — Sends product images directly in Telegram
- **Fallback Handling** — Gracefully handles "no results" with helpful alternatives

---

## 🛠️ Tech Stack

| Tool | Purpose |
| :--- | :--- |
| [n8n](https://n8n.io) | Workflow automation & orchestration |
| [Pinecone](https://pinecone.io) | Vector database for RAG retrieval |
| [Google Gemini](https://ai.google.dev) | Embeddings + LLM generation |
| [Google Sheets](https://sheets.google.com) | Inventory data storage |
| [Telegram API](https://core.telegram.org/bots/api) | User interface |

---

## 🧠 How It Works
