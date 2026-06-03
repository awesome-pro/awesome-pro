<!--
  GitHub profile README for github.com/awesome-pro
  Paste the content BELOW this comment into the README.md of your
  special profile repo: github.com/awesome-pro/awesome-pro
  (create that repo — name it exactly "awesome-pro" — if it doesn't exist).
-->

### Abhinandan

**Agentic AI Engineer.** I build the infrastructure AI products run on.

Multi-agent systems, LLM inference pipelines, and the unglamorous production
work that separates demos from products. I care about the parts that don't make
it into the demo — latency budgets, cost models, error surfaces, observability —
because those decide whether a product survives contact with real users.

---

#### Currently

**Founding Engineer @ Browzer** — CDP-native browser automation agents.

- A Chrome MV3 recorder + CDP agent with **95%+ AX/DOM element capture**, cross-iframe support, and real mouse/key/upload execution.
- A streaming **ReAct loop** over FastAPI + extension: SSE tool execution, multi-tab orchestration, safe parallelism, abort/continue, audit logs.
- **~67% lower LLM spend** via compact recording traces, context compression, prompt caching, and model routing across GPT-5 / Claude Sonnet & Haiku.
- A **zero-LLM replay engine** (recordings run as variable-driven tool-call templates) with a stateful AI fallback that resumes mid-run on failure.
- **Self-healing docs** that auto-repair on UI drift — Haiku→Sonnet diff triage, LLM-free replay of intact steps, and an agent that fixes only what changed.

~700K+ production LLM calls monitored to date.

---

#### Selected open source

**[agentflow-pro](https://github.com/awesome-pro/agentflow-pro)** — *RL for agentic reasoning.*
Rebuilt the ICLR 2026 AgentFlow architecture as a local Qwen3-8B Planner→Executor→Verifier→Memory loop, then trained the planner with **DAPO + a learned Qwen3-0.6B Process Reward Model** (replacing the paper's GRPO). Full A40 pipeline (DeepSeek-judged labels → PRM → bf16 LoRA DAPO → GGUF). **+5.0 pts on GPQA-Diamond (40.0% → 45.0%)** under leakage-free, quantization-matched eval.

**[guardloop](https://github.com/awesome-pro/guardloop)** — *Guardrail runtime for async agents.*
Pre-flight cost/token/time/tool-call budgets, per-tool circuit breakers, a verifier-feedback retry loop, OpenTelemetry GenAI spans, and no-rewrite adapters for LangGraph & the OpenAI Agents SDK — safety enforced inside your existing LLM/tool calls.

**[smartmemo](https://github.com/awesome-pro/smartmemo)** — *Semantic memory/cache for LLM agents.*
Embeddings retrieve candidates; a learned pair-equivalence classifier decides reuse. Bundled classifier trained on 16,576 pairs across 9 domains — **+30 precision points at equal recall vs. cosine** — with implicit bad-hit detection and gated retraining.

**[orchflow](https://github.com/awesome-pro/orchflow)** — *Dependency-free multi-agent pipelines.*
Typed Python for readable sequential/parallel/conditional flows: retries, shared context, flat traces, lifecycle events, human gates, and JSON checkpoint/resume.

**[agenteval](https://github.com/awesome-pro/agenteval)** — *Behavioral eval for agents.*
Replaces exact-match asserts with repeated-run pass-rate tests; traces tool calls/timing/steps and emits JSON reports for CI gates. OpenAI / Anthropic / LangChain adapters.

---

#### Stack

```
Agents      LangGraph · OpenAI Agents SDK · LangChain · LlamaIndex · MCP/FastMCP
            ReAct · function calling · multi-agent orchestration · CDP agents
LLM eng     Fine-tuning (LoRA/QLoRA/PEFT) · DPO/GRPO/DAPO/PRM · vLLM/SGLang/Ollama
            quantization (AWQ/GPTQ/GGUF) · context engineering · KV-cache · streaming
Retrieval   PyTorch · sentence-transformers · RAG · FAISS · Qdrant · pgvector
Eval/Obs    OpenTelemetry · Langfuse · Arize Phoenix · LangSmith · GPQA/AIME
Systems     FastAPI · Nest.js · GraphQL · SSE/WebSockets · Docker · GCP · AWS · Redis
Languages   Python · TypeScript · C++ · SQL
```

---

#### Elsewhere

[abhinandan.one](https://abhinandan.one) · [linkedin/in/abhibuilds](https://linkedin.com/in/abhibuilds) · hi@abhinandan.one

<sub>Open-source contributor at HeroUI (YC S24) — fixed 10+ bugs and shipped 7+ enhancements across Calendar, Table, and Pagination, which led to a personal offer from the CEO.</sub>
