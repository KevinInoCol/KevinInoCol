<h1 align="center">Kevin Adier Inofuente Colque</h1>

<p align="center">
  <b>AI Engineer</b> — LLM Agents · RAG · MLOps<br>
  MSc in Computer Engineering · PhD Student @ UNICAMP<br>
  📍 Campinas, Brazil
</p>

<p align="center">
  <a href="https://kevininocol.github.io/kevinadierinofuentecolque.github.io/">
    <img src="https://img.shields.io/badge/Portfolio-0b1220?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Portfolio">
  </a>
  <a href="https://www.linkedin.com/in/kevin-inofuente-colque">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <a href="https://kevininocol.github.io/reinforcement-learning-gmm-sac-ppo-calvin/">
    <img src="https://img.shields.io/badge/Research-8b5cf6?style=for-the-badge&logo=googlescholar&logoColor=white" alt="Research">
  </a>
</p>

---

## About

I design and ship **LLM agents that run in production** — not demos. My work sits where
agent orchestration meets real infrastructure: retrieval over private knowledge bases,
tool calling against live systems (BigQuery, CRMs, WhatsApp), input guardrails, persistent
memory, and full tracing so failures are debuggable instead of mysterious.

In parallel, I'm a PhD student in Computer Engineering at UNICAMP researching
**reinforcement learning for robot skill acquisition**.

---

## Tech stack

**Agents & LLM frameworks**

![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langgraph&logoColor=white)
![CrewAI](https://img.shields.io/badge/CrewAI-FF5A5F?style=flat-square)
![LlamaIndex](https://img.shields.io/badge/LlamaIndex-3d2a5c?style=flat-square)
![Google ADK](https://img.shields.io/badge/Google%20ADK-4285F4?style=flat-square&logo=google&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)

**RAG, data & observability**

![Pinecone](https://img.shields.io/badge/Pinecone-000000?style=flat-square&logo=pinecone&logoColor=white)
![Langfuse](https://img.shields.io/badge/Langfuse-0A0A0A?style=flat-square)
![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?style=flat-square&logo=googlebigquery&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)

**Backend & MLOps**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Google Cloud](https://img.shields.io/badge/Google%20Cloud-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

**ML & Robotics**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Stable Baselines3](https://img.shields.io/badge/Stable%20Baselines3-4b4b4b?style=flat-square)
![Isaac Sim](https://img.shields.io/badge/Isaac%20Sim-76B900?style=flat-square&logo=nvidia&logoColor=white)

---

## Featured work

### 🏗️ [AgentForge — multi-tenant agent runtime (SaaS)](https://github.com/KevinInoCol/AgentForge)

No hardcoded prompt: every GoHighLevel sub-account configures its own agent from the
dashboard, and the runtime loads that config **dynamically per incoming message** — one
service serving all tenants. Inbound webhooks return fast and enqueue; a Redis **debounce
buffer** merges rapid-fire user messages into a single inference; async workers then run one
full turn — agent factory, chat history, pgvector RAG retrieval and CRM tools (scheduling,
tags, custom fields) — before replying.

`FastAPI` · `LangChain` · `Supabase/pgvector` · `Redis` · `Next.js` · `Multi-tenant`

### 🤖 [DataBot — Multi-tool WhatsApp agent with guardrails & observability](https://github.com/KevinInoCol/Project-LangChain-Agent-for-Whatsapp-with-KB-CH-Multitool-and-Security-Langfuse)

Production support agent serving WhatsApp through Chatwoot. RAG over a private knowledge
base (Pinecone), contextual web search (Tavily), persistent conversation memory
(PostgreSQL), and **human handoff** when the agent should step aside. Ships with an
**8-layer input guardrail** and end-to-end Langfuse tracing plus LLM-as-a-Judge scoring.

`LangChain` · `FastAPI` · `Pinecone` · `PostgreSQL` · `Chatwoot` · `Langfuse`

### 📊 [Text2SQL agent over BigQuery](https://github.com/KevinInoCol/Project-LangGraph-Agente-Text2SQL-BigQuery)

Turns natural-language questions into valid BigQuery SQL, executes it, and answers in plain
language. Built as a **LangGraph state graph** cycling between an agent node and a tool
node until the answer is grounded in real query results. Runs on the public NYC Citi Bike
dataset, served via Streamlit and containerized with Docker.

`LangGraph` · `BigQuery` · `SQLAlchemy` · `Streamlit` · `Docker`

### 🕸️ [Multi-agent cold email pipeline](https://github.com/KevinInoCol/Project-LangGraph-Multiagente-Scraper-Profiler-Copywriter)

Give it a company URL and three specialized agents hand work down a chain: a **scraper**
crawls the site (Apify), a **profiler** infers pain points, tech stack and ideal customer,
and a **copywriter** writes a personalized cold email. Non-conversational, fully
orchestrated as a LangGraph pipeline.

`LangGraph` · `Multi-agent orchestration` · `Apify`

### 🎙️ [Voice agent over a property dataset](https://github.com/KevinInoCol/Project-LangChain-Agente-Voz-Google-Sheets)

You speak, Whisper transcribes, a LangChain agent reasons over a pandas dataframe of São
Paulo rental listings, and the answer comes back as speech via OpenAI TTS. Full
voice-in / voice-out loop.

`LangChain` · `Whisper` · `pandas` · `OpenAI TTS`

### 🏘️ [Kommo CRM sales agent — cloud vs local LLM](https://github.com/KevinInoCol/Agente-Conversacional-Kommo-CRM-LMStudio-VS-OpenAI)

Real-estate sales agent wired into **Kommo CRM** through webhooks: answers from a RAG
policy base, searches listings in Google Sheets, and drives the sales funnel (moves stages,
updates custom fields) via tool calling. Swaps between **OpenAI** and a **local LM Studio
model** by changing a single environment variable.

`LangGraph` · `Kommo CRM` · `RAG` · `LM Studio` · `Tool calling`

### ⚙️ MLOps pipelines

A series of end-to-end deployments — regression and classification models packaged and
shipped to **Google Cloud Run** and **Azure** through GitHub Actions CI/CD, with Streamlit
front-ends. [Browse the MLOps repos →](https://github.com/KevinInoCol?tab=repositories&q=MLOps)

---

## Research

**PhD in Computer Engineering — UNICAMP** · Reinforcement learning for robot skill adaptation

[**Robot skill adaptation: GMM, SAC-GMM & GMM+PPO on CALVIN**](https://github.com/KevinInoCol/reinforcement-learning-gmm-sac-ppo-calvin)
— reproducibility study and benchmark of RL methods for skill learning on the
[CALVIN](https://github.com/mees/calvin) benchmark, building on
*Robot Skill Adaptation via Soft Actor-Critic Gaussian Mixture Models*
(Nematollahi et al., ICRA 2022).

| Method | Type | Status |
|---|---|---|
| GMM only | Offline learning from demonstration (Bayesian GMM) | ✅ Reproduced |
| SAC-GMM | Hybrid — SAC refines trajectory parameters | ✅ Reproduced |
| GMM + continuous PPO | Hybrid — PPO refines Δθ ∈ ℝ⁹ via SB3 | 🧪 In progress |

Evaluated on the `open_drawer` skill, CALVIN scene D, across 3 seeds × 20 episodes per
method. 📄 *Paper in preparation* · with Maria Fernanda Paulino Gomes.

📈 **[Live results, videos & training curves →](https://kevininocol.github.io/reinforcement-learning-gmm-sac-ppo-calvin/)**

---

## Currently working on

- 🔐 **Hardening agents for production** — layered guardrails, prompt-injection defense and Langfuse-based evaluation loops
- 🧩 **Google ADK** — exploring Agent Development Kit patterns against LangGraph for multi-agent systems
- 🏠 **Local-first LLMs** — agents running on LM Studio / Gemma so sensitive data never leaves the machine
- 🦾 **PhD research** — finishing the continuous GMM+PPO benchmark on CALVIN

---

## Contribution graph

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/KevinInoCol/KevinInoCol/output/github-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/KevinInoCol/KevinInoCol/output/github-snake.svg">
  <img alt="Contribution snake animation" src="https://raw.githubusercontent.com/KevinInoCol/KevinInoCol/output/github-snake.svg">
</picture>

---

<p align="center">
  <i>Open to collaboration on LLM agents, applied AI and robot learning.</i>
</p>
