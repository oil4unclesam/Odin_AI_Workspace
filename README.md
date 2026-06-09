
![Odin](docs/Odin.jpg)

A self-hosted AI workspace — the self-hosted version of ChatGPT/Claude, but with more features. Run on your own hardware, keep your data local, and stay private.

*Inspired by tools we actually use. Built for people who care where their data lives.*

## Features

- **Chat** -- chat with any local model or API; adding them is super simple.<br>　<sub>vLLM · llama.cpp · Ollama · OpenRouter · OpenAI · GitHub Copilot</sub>
- **Agent** -- hand it tools and let it run the whole task itself.<br>　<sub>built on [opencode](https://github.com/anomalyco/opencode) · MCP · web · files · shell · skills · memory</sub>
- **Cookbook** -- Scans your hardware, recommends models, click to download and serve.. easy!<br>　<sub>built on [llmfit](https://github.com/AlexsJones/llmfit) · VRAM-aware · GGUF / FP8 / AWQ · fit scoring · vLLM / llama.cpp serving</sub>
- **Deep Research** -- multi-step runs that gather, read, and synthesize sources into a nice visual report.<br>　<sub>adapted from [Tongyi DeepResearch](https://github.com/Alibaba-NLP/DeepResearch)</sub>
- **Compare** -- a fun tool to compare models side by side. Test completely blind, no bias!<br>　<sub>multi-model · blind test · synthesis</sub>
- **Documents** -- YOU write the text, AI is there to assist, not the opposite.<br>　<sub>multi-tab editor · markdown · HTML · CSV · syntax highlighting · AI edits · suggestions</sub>
- **Memory / Skills** -- Persistent memory and skills, your agent evolves over time as it better understands you and your tasks!<br>　<sub>ChromaDB · fastembed (ONNX) · vector + keyword retrieval · import/export</sub>
- **Email** -- IMAP/SMTP inbox with AI triage built in: urgency reminders, auto-tag, auto-summary, auto-reply drafts, auto-spam.<br>　<sub>IMAP · SMTP · per-account routing · CalDAV-aware</sub>
- **Notes & Tasks** -- Quick notes with reminders, a todo list, and scheduled tasks the agent can act on.<br>　<sub>note pings · checklist · cron-style tasks · ntfy / browser / email channels</sub>
- **Calendar** -- Local-first calendar with CalDAV sync to Radicale / Nextcloud / Apple / Fastmail.<br>　<sub>CalDAV pull · .ics import/export · per-calendar colors · agent-aware</sub>
- **Works on mobile** -- looks and runs great on your phone, not just desktop.<br>　<sub>responsive · installable (PWA) · touch gestures</sub>
- **Extras** -- more to explore, happy if you give it a go!<br>　<sub>image editor · theme editor · file uploads (vision + PDF) · web search · presets · sessions · 2FA</sub>

## Demo

A full tour lives in `docs/index.html`. Watch the clips — this thing works.

<details>
<summary>Screenshots / clips</summary>

### Chat & Agents
![Chat & Agents](docs/chat.gif)
### Deep Research
![Deep Research](docs/research.gif)
### Compare
![Compare](docs/compare.gif)
### Documents
![Documents](docs/document.gif)
### Notes & Tasks
![Notes & Tasks](docs/notes.gif)

</details>

## Quick Start

Default config works out of the box: clone, run, configure inside Settings. Only touch `.env` for deployment overrides.

On first boot, Odin creates an admin account and prints a temporary password in the terminal. For Docker, check `docker compose logs Odin` for the password. Change it in Settings immediately.

**Need help?** Open an issue or ping the community. We don't collect anything — no crash reports, no analytics, no tracking.

### Docker (recommended)

```bash
git clone https://github.com/oil4unclesam/Odin_AI_Workspace.git
cd Odin_AI_Workspace
cp .env.example .env       # optional but recommended
docker compose up -d --build
