# Telegram Inventory Bot

> An AI-powered Telegram bot that helps customers find products, check stock, and browse inventory using RAG (Retrieval-Augmented Generation).

---

## 📸 Demo

![Bot Demo](demo.GIF)

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

1. User sends a message via Telegram.
2. Gemini classifies the intent.
3. If `list_inventory` → Google Sheets returns all products → Gemini formats as list.
4. If `search_product` → Pinecone finds the closest product → Google Sheets checks stock → Gemini generates response → Telegram sends text + image.
5. If `help` → Static help menu.
6. If `unknown` → Helpful fallback.

---

## 🔧 Why No LangChain?

I built this without LangChain to understand the underlying components of RAG:

- What embeddings are and how they're generated
- How vector search works (Pinecone)
- How retrieval and generation connect
- How to orchestrate workflows manually

This gave me full control and a deeper understanding of how RAG systems work.

---

## 🚀 Quick Start

1. Clone this repo
2. Import `workflow.json` into n8n
3. Set up your Pinecone index
4. Add your Google Gemini API key
5. Configure Google Sheets with your inventory
6. Create a Telegram bot via @BotFather
7. Set your Telegram webhook URL
8. Activate the workflow

---


---

## 🎓 What I Learned

- Building RAG systems without LangChain
- Working with Pinecone vector databases
- Intent classification using LLMs
- Orchestrating complex workflows in n8n
- Integrating multiple APIs (Telegram, Sheets, Gemini, Pinecone)
- Handling fallback logic for production reliability

---

## 📅 Next Features (Planned)

- [ ] Product recommendations
- [ ] User session memory
- [ ] Analytics dashboard
- [ ] Order placement

---

## 🙋‍♂️ About Me

I'm an AI Automation Engineer with a passion for building production-ready AI systems.

[GitHub](https://github.com/alamin-omoyele) | [LinkedIn](https://linkedin.com/in/al-amin-mohammed) 

---

## 📄 License

MIT

