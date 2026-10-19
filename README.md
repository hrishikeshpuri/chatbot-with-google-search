# Chatbot with Google search

n8n chat workflow that answers questions with live Google results via SerpAPI.

Synced from the n8n workflow **Chatbot with Google search** (`OzcaHVVQkDQdT6Lv`).

## What it does

1. A chat trigger receives the user message.
2. An AI Agent (OpenAI `gpt-4.1-mini`) answers the question.
3. Window memory keeps the last 10 turns of context.
4. The Serp tool is used first so answers are grounded in current search results.

## Import into n8n

1. In n8n, open **Workflows** → **Import from file**.
2. Select `chatbot-with-google-search.json`.
3. Attach credentials:
   - **OpenAI** on the OpenAI node
   - **SerpAPI** on the Serp node
4. Publish / activate the workflow if you want the chat trigger live.

API keys are not stored in this repository. Reconnect credentials after import.

## Nodes

| Node | Type |
| --- | --- |
| Trigger Message | Chat Trigger |
| AI Agent | LangChain Agent |
| OpenAI | OpenAI Chat Model |
| Simple Memory | Window Buffer Memory |
| Serp | SerpAPI Tool |
