# GitHub Repos with Real Anthropic / OpenAI / DeepMind Interview Questions (面经)

## Tier 1 — Repos with REAL company-tagged questions for the three target companies

### 1. yubol-bobo/ace-the-system-design-interview
- **URL:** https://github.com/yubol-bobo/ace-the-system-design-interview
- **Stars:** 6 | **Updated:** 2026-08-01 | **Language:** Mixed Chinese/English
- Dedicated per-company raw question files (`raw_Q/anthropic.md`, `raw_Q/openai.md`, `raw_Q/google-deepmind.md`, plus `xai.md`, `meta-msl.md`) with per-question source attribution (1point3acres, Glassdoor, Blind, Reddit, Exponent, interviewing.io, IGotAnOffer).
- **Anthropic samples:** "Design Claude Chat Service"; "Handle 100K RPS for LLM Token Generation"; "Design a Key-Value Store"; "Design a Web Crawler"; "Design a Banking App"; "Implement QKV attention in PyTorch from scratch"; "Concurrent web crawler"; "20 variants in A/B test show one significant result — is it suspicious?"; "What would you do if AI were starting to feel sad?"; "Tell me about a time you had a moral conflict with work"; "What concerns do you have with Anthropic's mission?"
- **OpenAI samples:** Resumable iterator (抽象类 ResumableIterator, pause/resume/skip/reset); Time-Based KV Store follow-ups (如何写测试？如何 mock 时间戳？多线程环境如何加锁？); Unix cd 解析 `../A/B/`、`./A/` w/ symlink + cycle detection; "Count Machines and Recover a Distributed Tree Topology"; Grid infection (m×n, 'X' 感染 '.', 同步更新, ≥T of 8 neighbors); Webhook Delivery System (12K/s avg, 50K/s peak); "Design ChatGPT for 100M Users" (~600 msg/s avg); Transformer debugging (~300 lines nanoGPT, 4 marked regions, then implement KV caching); "If deciding whether to release a new AI model, what criteria would you use?"
- **DeepMind samples:** balls-in-bag posterior probability question; L1 vs L2 正则化 sparsity from gradient behavior; derive ELBO for a graphical model; Trie prefix matching; Snapshot Array (LC 1146); Best Meeting Point (LC 296); parse & evaluate math expression; Python basic filesystem interface; "训练 100B 参数模型显存溢出；Data/Model Parallelism design"; YouTube recommendation design; mobile autocomplete + spell check.

### 2. xttjsn/ai-learn — `anthropic-question-bank.md`
- **URL:** https://github.com/xttjsn/ai-learn/blob/master/anthropic-question-bank.md
- Explicitly sourced from 一亩三分地面经汇总 (1point3acres aggregated Anthropic 面经):
  - OA: "Recipe Manager", "Task Management System (四问，整体不难)", "Toy Simulation of an App (TypeScript 或 Python)"
  - Coding: Web Crawler (same-domain links from a URL); LRU Cache (like functools.lru_cache); Stack Trace (地里原题); Mode/Median (地里原题)
  - System design: "Batch GPU Requests — batch GPU inference 系统"; "Batch File Streaming — stream big file from cloud storage to 1000 machines"; large-scale data infra (ingest/process/serve)
  - Specialized: "RL Fundamental — 需要熟悉 GRPO 训练流程"; Culture round 核心: AI Safety

### 3. harry-the-nerd/interview-notes-questions (darkinterview.com)
- **URL:** https://github.com/harry-the-nerd/interview-notes-questions
- **Stars:** 206 | **Updated:** 2026-08-05
- **Anthropic** (`anthropic/web-crawler.md`): crawler returning all URLs reachable from startUrl sharing its hostname; follow-up multithreaded w/ bounded thread pool; discussion: distributed crawling, politeness/rate limiting, near-duplicate detection.
- **OpenAI** (`openai/toy-language-type-system.md`): `__str__()` for type Nodes/Functions, then `get_return_type()` with generic substitution, "Expecting int but got str", generic-binding conflicts. 5 worked examples + reference solution.

### 4. ombharatiya/FAANG-Coding-Interview-Questions
- **URL:** https://github.com/ombharatiya/FAANG-Coding-Interview-Questions
- **Stars:** 5,675 | **Updated:** 2026-08-07
- `AI-Companies-Interview-Questions.md` (compiled from 1,500+ candidate reports: Reddit, Blind, Glassdoor, 1point3acres, LeetCode Discuss, interviewing.io, Exponent).
- **DeepMind:** Implement Trie; Find Median from Data Stream; quiz topics (eigenvalues, SVD, probability, autodiff); "Design a training system for a model that does not fit on a single accelerator".
- **OpenAI** (~8 custom problems): KV Store Serialize/Deserialize; CD Directory Navigation w/ symlink cycle detection; Excel/Spreadsheet Engine w/ circular-dependency detection; Toy Language Interpreter (75-min lexer/parser/evaluator); Versioned KV Store; unique agentic round: existing codebase + features "too large to tackle by hand" — drive an AI coding agent.
- **Anthropic** (~6 live-coding questions): In-Memory Database (4 levels: SET/GET/DELETE → backup/restore); Web Crawler (BFS → multithreaded); LRU Cache (bugfix + extend + persistence); Tokenization Engine; Bank System (merging, cashback); File System Implementation. "AI tools strictly prohibited in live interviews" but "explicitly permitted on the performance take-home."

### 5. Zchary1106/agent-interview-hub
- **URL:** https://github.com/Zchary1106/agent-interview-hub
- **Stars:** 148 | **Updated:** 2026-08-07 | Chinese
- Per-company folders (岗位要求.md + 面试题与面经.md): Anthropic, OpenAI, Google, Microsoft + Chinese giants (June 2026).
- **Anthropic:** "设计一个有 15 个工具的 Customer Service Agent 的 System Prompt 架构"; "Agent 运行 50 轮对话后 Context Window 快满了，怎么处理？"; "设计 Claude Code（Agentic Coding Assistant）的核心架构"; "设计一个 Agent Eval 系统，自动评估 Claude 在 1000 个任务上的 Agent 能力"; values: "如果发现 Claude 在边缘情况绕过安全限制，但修复需要 3 个月，怎么处理？"
- **OpenAI:** "RLHF 在 Agent 训练 vs 普通聊天模型的差异?"; "o1/o3 推理模型在 Agent 场景的优势/劣势?何时该用?"; "Function Calling 底层实现原理?模型如何学会何时调用工具、如何生成参数?"
- **Google:** "Gemini 多模态原生架构 vs GPT-4V 先视觉编码再拼接的差异？"; "A2A 协议 vs MCP 协议区别？"

### 6. atomeocean/job-compass — true 1point3acres thread archiver
- **URL:** https://github.com/atomeocean/job-compass (site: jobcompass.atomeocean.com)
- **Stars:** 16 | **Updated:** 2026-08-03 | Chinese
- 36 company folders incl. **openai** (no anthropic/deepmind yet). Each file = archived 1p3a thread.
- `openai/y2ti8x.md` = 1p3a thread-1175440 (2026-05-03, MLE phone screen, did not pass): virus-spread grid — "susceptible cell with K+ infected of 8 neighbors becomes infected next day"; follow-up: recovery/immunity after D consecutive infected days.

### 7. warrenzhu25/system-design — `anthropic_interview_questions.md`
- **URL:** https://github.com/warrenzhu25/system-design
- Index/mirror of https://www.1point3acres.com/interview/problems/company/anthropic (behavioral areas: "Views on AI Safety and Company Mission", "Standing Up for Your Beliefs", "Interest in Anthropic"). Also chatgpt_system_design.md, llm-inference-serving.md.

### 8. ombharatiya/AI-Engineer-Interview-Questions
- **URL:** https://github.com/ombharatiya/AI-Engineer-Interview-Questions — 26 company files incl. anthropic.md, openai.md, google-deepmind.md. **Synthesized, not leaked** — representative only.
- DeepMind (synth): multi-head self-attention from scratch, causal; "pretraining loss diverges at step 300k — diagnose"; "expected fair coin flips until two heads in a row?"

### 9. Automaat/research-machine — `findings/job-search/anthropic-interview-process.md`
- Anthropic SWE process doc: recruiter → CodeSignal OA → HM screen → 4-5h onsite → values round. No AI tools in live rounds; Python primary; SD = "LLM API serving, request batching, GPU optimization."

## Tier 2 — High-star generic LLM/ML banks (no A/O/D company tagging)
| Repo | Stars | Lang | Notes |
|---|---|---|---|
| wdndev/llm_interview_note | 14,852 | 中文 | Best-known 大模型面试 bank; no company 面经 |
| khangich/machine-learning-interview | 12,764 | EN | FAANG-focused; no A/O/D |
| alirezadir/AIMLInterviews | 8,698 | EN | generic ML system design |
| adongwanai/AgentGuide | 7,965 | 中文 | 大模型面试题库 |
| luhengshiwo/LLMForEverybody | 7,107 | 中文 | conceptual |
| amusi/AI-Job-Notes | 6,131 | 中文 | AI 算法岗求职攻略 |
| chiphuyen/ml-interviews-book | 4,705 | EN | 200+ questions, not company-tagged |
| WeThinkIn/AIGC-Interview-Book | 4,267 | 中文 | AIGC/LLM/Agent 面试 |
| 315386775/DeepLearing-Interview-Awesome-2024 | 2,874 | 中文 | CV/LLM 面试题集 |
| km1994/LLMs_interview_notes | 2,593 | 中文 | 大模型面试题 |
| guocong-bincai/ai-interview-guide | 401 | 中文 | 国内大厂真题集 |

## Key findings
1. No single high-star repo is dedicated to A/O/D 面经; real company-tagged questions live in small personal repos mirroring 1p3a/Glassdoor.
2. Cross-confirmed real questions (2+ independent repos): Anthropic — multithreaded same-hostname web crawler, LRU cache bugfix, 4-level in-memory KV/database, batch GPU inference design, AI-safety values round; OpenAI — resumable iterator, cd/symlink path resolution, grid infection, toy-language type system, versioned KV store, nanoGPT bug hunt + KV caching; DeepMind — quiz round (SVD/eigenvalues/probability/ELBO), Trie, distributed training beyond one accelerator.
3. 1point3acres is the upstream source for most Chinese-language aggregation; job-compass archives raw threads verbatim.
4. Famous high-star repos (khangich, alirezadir, chiphuyen) contain no A/O/D-specific questions.
