# Awesome-Agent-Native-Inbox

## Top Agent-Native Inbox Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Programmatic Inboxes, Inbound Parsing & Agent Email Infrastructure*  

**Last updated: March 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Agent-Native Inboxes**. These tools give AI agents their own email addresses with API-first inbox management—enabling OTP verification, customer support triage, document processing, and autonomous communication workflows without the limitations of human email providers.



**Examples** include AgentMail, OpenMail, AGmail, Bavimail, AgenticEmail, Sequenzy, Mailtrap, Nylas, Shortwave, and Superhuman AI (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting agent inboxes, deterministic security gates, and open email infrastructure—ideal for AI engineers, platform teams, and developers seeking transparent, vendor-independent agent email.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[AgentMail](https://agentmail.to/)**  

  The first email provider built for AI agents. API-first infrastructure with programmatic inbox creation, usage-based pricing, real-time webhooks/WebSockets, and simple API key authentication (no OAuth). Features automatic labeling, structured data extraction, full-text search across inboxes, and SDKs for Python, TypeScript, Go, plus an MCP server. Free tier: 3 inboxes, 3,000 emails/month. Y Combinator-backed with $6M seed .



- **[OpenMail](https://openmail.ai/)**  

  EU-based, GDPR-compliant agent email infrastructure positioned as the privacy-first alternative to AgentMail. Features instant replies via webhooks/WebSockets, RAG-ready attachment extraction, and two-way threading. Free tier: 3 inboxes, 3,000 emails/month. Developer plan at €9/month: 10 inboxes, 10,000 emails. Launch plan at €49/month: 200 inboxes, 150,000 emails .



- **[Nylas Agent Accounts](https://www.nylas.com/)**  

  Hosted mailboxes with calendar built in (beta). Enables programmatic inbox creation and management for agents without OAuth complexity.



- **[Mailtrap](https://mailtrap.io/)**  

  Email delivery platform with testing, sending, and inbound email APIs. Features SMTP/API sending, email testing sandbox, and inbound parsing for agent workflows.



- **[Shortwave](https://www.shortwave.com/)**  

  AI-powered email client with agent capabilities. Uses LLMs for email search, summarization, and drafting. Note: operates on your existing inbox rather than providing programmatic agent addresses.



- **[Superhuman AI](https://superhuman.com/)**  

  AI email client focused on speed and triage. Note: like Shortwave, operates on human inboxes rather than providing agent-native addresses.



- **[Mailforge](https://mailforge.com/)**  

  Mailbox provisioning infrastructure for agencies and GTM teams. API returns SMTP and IMAP credentials for agent use. Features official MCP and CLI support, automated SPF/DKIM/DMARC setup, and pre-warmed mailboxes. Pricing per mailbox slot: $3/month (annual: $2/month), minimum 10 slots .



- **[Sidemail](https://sidemail.io/)**  

  All-in-one email platform with official MCP server. Features inbound email API, white-label sending, detailed API logs, 90-day email history, and no-code/Markdown emails. Pricing from $19/month per 1,000 emails. 7-day free trial .



## Open-Source GitHub Projects



- **[Messo](https://github.com/messo-email/messo)**  

  Open-source email infrastructure for AI agents (license varies). Give agents their own mailboxes—send, receive, search, and parse emails programmatically. Self-hosted on Cloudflare with zero vendor lock-in. Features structured email parsing (intent detection, link extraction, action items without LLM), multi-mailbox support (one per agent), one-command deploy, and pre-built tool definitions for Vercel AI SDK / LangChain. TypeScript SDK + CLI. `npx messo claim my-agent` provisions a mailbox instantly .



- **[docker-mailagent](https://pypi.org/project/docker-mailagent/)**  

  LLM-powered email agent that watches Maildir inboxes, classifies mail, and executes workflows (open-source). Docker sidecar for docker-mailserver. Features multi-inbox support with 5 LLM providers (OpenAI, Anthropic, Gemini, OpenRouter, Groq), LLM classification with keyword fallback, 4 composable action types (reply, ignore, notify, webhook), smart SMTP replies with threading, sent folder sync, and message flagging. Includes REST API and web dashboard. `inotify` watching with catch-up on restart .



- **[emalia](https://pypi.org/project/emalia/)**  

  Security-first agent email framework (open-source). Built on the assumption that "an inbox is an unauthenticated public endpoint." Features empty allowlist by default (listener refuses to start), capability gating outside the model (disabled tools are never constructed), replies restricted to original sender unless explicitly widened, file sandboxing with credential-name refusal, shell/Python off by default (requires second explicit switch), and prompt-injection delimiters. Toolsets: email, file_read, file_write, http, shell, python. Supports Gmail (App Password or OAuth), Outlook/Microsoft 365 .



- **[NornWeave](https://pypi.org/project/nornweave/)**  

  Open-source, self-hosted Inbox-as-a-Service API for AI agents. Adds stateful layer (Inboxes, Threads, History) and intelligent layer (Markdown parsing, Semantic Search) to make email consumable by LLMs. Features virtual inboxes, webhook ingestion from Mailgun/SES/SendGrid/Resend, PostgreSQL storage, HTML-to-Markdown parsing, automatic threading, MCP server for Claude/Cursor, attachment text extraction, semantic search with pgvector, and multi-tenancy. Docker Compose deployment .



- **[Agentic Inbox (Cloudflare)](https://github.com/cloudflare/agentic-inbox)**  

  Self-hosted AI email client from Cloudflare (Apache-2.0). AI Agent automatically reads, summarizes, and processes emails. Runs entirely on Cloudflare Workers with no external dependencies. 3,800+ GitHub stars. Reference architecture for agent communication workflows on edge computing .



- **[dearagent](https://github.com/panda-sandeep/dearagent)**  

  Email inbox API for AI agents, self-hosted on Cloudflare Workers (open-source, AgentMail alternative). Features inboxes, threads, long-polling for messages, full-text search, read/label management, compose/reply/reply-all/forward, webhooks with HMAC signature verification, and MCP server at `/mcp`. Supports outbound attachments and multipart/alternative message generation .



- **[Pizza Bot (AWS)](https://aws.amazon.com/blogs/opensource/introducing-pizza-bot-an-open-source-inbox-for-ai-agents-that-work-in-the-background/)**  

  Open-source inbox for AI agents that work in the background (from AWS). Server + client architecture where runs keep going when you close the thread. Checkpointed runs via LangGraph. Connects to MCP servers for tools and works with Agent Skills. All data stays local in SQLite unless you configure otherwise. Features delegation through skills, memories that persist across threads, and approval gates for specific tools .



- **[Mailpit](https://github.com/axllent/mailpit)**  

  Email testing tool & API for developers (MIT). Not an agent inbox per se, but essential for testing agent email workflows. Acts as SMTP server with modern web UI, REST API for integration testing, and optional webhook for received messages. Fast: 100-200 emails/second. Includes HTML check, link check, spam check (via SpamAssassin), and message tagging. Single static binary, zero dependencies. MailHog successor .



### Additional Strong Open-Source Options



- **[MailHog](https://github.com/mailhog/MailHog)** — Email testing tool for developers (MIT). SMTP server with web UI and JSON API. Note: no longer actively maintained; Mailpit is the recommended successor .

- **[pytest-mailpit](https://pypi.org/project/pytest-mailpit/)** — Pytest plugin for testing email flows with Mailpit. Provides `mailpit_inbox.wait_for_message()`, `message.code()`, `message.link()`, and self-explaining failures. Useful for testing agent email handlers .

- Community **n8n** workflows for agent email routing and notification automation.



**Frameworks for building custom systems**: Combine **Messo** or **NornWeave** as the agent inbox API with **emalia** for deterministic security gates (allowlists, capability gating, prompt-injection defense), **docker-mailagent** for LLM-powered classification and workflow execution, **Mailpit** for testing, and **PostgreSQL** for persistence—creating a fully self-hosted, enterprise-grade agent-native inbox platform.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Agent inboxes handling email content must comply with data protection regulations (GDPR, CCPA, CAN-SPAM, etc.) and email sending regulations (SPF, DKIM, DMARC).

- Self-hosted open-source solutions require proper security hardening, domain configuration, and ongoing maintenance. An inbox is an unauthenticated public endpoint—anyone who learns the address can inject content. Security controls must gate capability outside the model (registration-time, not prompting) to defend against prompt injection .



---



**Made for AI engineers, platform teams, and developers building transparent agent email infrastructure.**  

Let's make Agent-Native Inboxes more open, data-driven, and secure.
