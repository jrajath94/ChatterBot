# AI Lab Interview Questions — Deep Research (Anthropic · OpenAI · Google DeepMind)

**Compiled: August 2026.** Deep research across 1point3acres (一亩三分地), other Chinese-language sites (searched in Chinese), GitHub aggregator repos, and niche English sources. Covers all technical tracks: SWE (junior → Staff), ML Engineer, Research Engineer, Research Scientist, Infrastructure, Performance, and adjacent roles.

**Method (first-principles / "Russian doll" layering):** each source layer was opened independently — search index → thread → mirror → secondary aggregator — and a question is only ranked "high confidence" when it appears in 2+ independent layers (e.g., a 1p3a thread AND a Blind post AND a GitHub archive). Raw per-source findings with full entry-level detail are in [`sources/`](sources/).

**Reliability legend:** ⭐⭐⭐ = cross-confirmed in 2+ independent sources · ⭐⭐ = single strong source (first-hand thread) · ⭐ = single aggregator/unverified.

---

## Table of contents

1. [Where to find these questions (the source map)](#1-where-to-find-these-questions-the-source-map)
2. [Anthropic — full question list](#2-anthropic)
3. [OpenAI — full question list](#3-openai)
4. [Google DeepMind — full question list](#4-google-deepmind)
5. [Cross-company high-confidence question bank](#5-cross-company-high-confidence-question-bank)
6. [Caveats](#6-caveats)

---

## 1. Where to find these questions (the source map)

### Tier 1 — 1point3acres (一亩三分地) and its mirrors — the upstream source

| Source | Link | Notes |
|---|---|---|
| 1p3a OpenAI question bank | https://www.1point3acres.com/interview/problems/company/openai | 196 indexed questions; **login-walled** |
| 1p3a Anthropic question bank | https://www.1point3acres.com/interview/problems/company/anthropic | 103 indexed questions; login-walled |
| 1p3a DeepMind index | https://www.1point3acres.com/interview/company/DeepMind | ~10 structured reports; also tag page `bbs/tag/deepmind-3761-1.html` |
| **Telegram mirror 北美跳槽面经** | **https://t.me/s/usinterview** | **The single best free source.** Live mirror of 1p3a-style reports; hashtag-searchable (`?q=%23openai`, `%23anthropic`, `?q=DeepMind`); dense 2025–2026 first-hand posts; no login |
| instant 1p3a mirror | https://instant.1point3acres.com/tag/deepmind | Mobile mirror of tag pages |

1p3a itself is Cloudflare + login/points-walled (some threads need >170–200 forum points). The Telegram mirror and Google-snippet mining recover most content. Key compilation threads (login needed for full bodies):
- OpenAI coding high-frequency: `bbs/thread-1149658-1-1.html` (Oct 2025) · systems: `thread-1149664` · 2024 full summaries: `thread-1112642`, `thread-1112645`
- Anthropic question-number ("题号") thread: `bbs/thread-1134248-1-1.html`
- DeepMind most-recent RE 挂经 (Sep 2025): `bbs/thread-1147017-1-1.html`

### Tier 2 — GitHub repos with real company-tagged questions (all free)

| Repo | What's inside |
|---|---|
| [yubol-bobo/ace-the-system-design-interview](https://github.com/yubol-bobo/ace-the-system-design-interview) | Per-company raw question files: `raw_Q/anthropic.md`, `raw_Q/openai.md`, `raw_Q/google-deepmind.md` — each question source-attributed (1p3a, Glassdoor, Blind, Exponent…) |
| [xttjsn/ai-learn](https://github.com/xttjsn/ai-learn/blob/master/anthropic-question-bank.md) | Raw dump of 1p3a's aggregated **Anthropic** 面经 (OA + coding + SD + RL/culture rounds) |
| [harry-the-nerd/interview-notes-questions](https://github.com/harry-the-nerd/interview-notes-questions) | 206★; full problem writeups: Anthropic web-crawler, OpenAI toy-language type system |
| [atomeocean/job-compass](https://github.com/atomeocean/job-compass) | Archives full 1p3a threads verbatim (36 companies incl. OpenAI, e.g. thread-1175440 MLE virus-simulation report) |
| [ombharatiya/FAANG-Coding-Interview-Questions](https://github.com/ombharatiya/FAANG-Coding-Interview-Questions) | 5.6k★; `AI-Companies-Interview-Questions.md` compiled from 1,500+ candidate reports; A/O/D sections |
| [Zchary1106/agent-interview-hub](https://github.com/Zchary1106/agent-interview-hub) | 中文; per-company 面试题与面经 for Anthropic/OpenAI/Google agent-engineering roles (June 2026) |
| [warrenzhu25/system-design](https://github.com/warrenzhu25/system-design) | Mirror/index of 1p3a's Anthropic problem list |

High-star generic banks (good 八股, **no** company 面经): wdndev/llm_interview_note (14.8k★, 中文), khangich/machine-learning-interview (12.8k★), alirezadir/AIMLInterviews (8.7k★), chiphuyen/ml-interviews-book (4.7k★).

### Tier 3 — Other Chinese sites (searched in Chinese)

| Site | Verdict |
|---|---|
| 知乎 zhihu.com | Best long-form Chinese analysis (OpenAI 面经, DeepMind 挂经/过经); zhuanlan 403s bots — use search snippets or browser. Key posts: `zhuanlan.zhihu.com/p/1922101111503975390` (what OpenAI screens for), `/p/1954883564152788970` (MLE round 1), `/p/983167020` (DeepMind) |
| CSDN + portal mirrors (163/sohu/thepaper) | Best Anthropic long-form: the Anthropic Fellow 9-hour pipeline article — `163.com/dy/article/JOMTOEL20511FQO9.html`, `sohu.com/a/862277837_413980` |
| 篱笆教育 libaedu.com | OpenAI question bank (`/questions/4477_37.html` CS, `/4477_41.html` DS/Research); first ~5 per category free |
| 看准网 kanzhun.com | DeepMind 面试题 mirror (`/gsm5672397.html`) |
| 牛客网 nowcoder | Domestic companies only — near-zero A/O/D content |
| 脉脉 / 小红书 | Login-walled, poorly indexed; in-app only |
| Service sites (programhelp.net, oavoservice.com, csoahelp.com, learncswithus.com) | Question-rich but they are 代面/cheating-service ads — use only to corroborate |

### Tier 4 — Niche English sources

Blind (best raw signal; via search snippets) · Hello Interview (`hellointerview.com/blog/openai-coding-questions`) · interviewing.io guides (Anthropic + OpenAI) · Exponent Anthropic guide · linkjob.ai question banks · first-hand blogs: Anqi Silvia (Medium, Anthropic 2025), Aleksa Gordić (DeepMind RE), Yuan Meng (`yuan-meng.com/posts/mle_interviews_2.0/`), CodingBFF (OpenAI senior fail) · **Anthropic's own engineering blog** (`anthropic.com/engineering/AI-resistant-technical-evaluations` — primary-source take-home disclosure) · prachub.com/companies/anthropic (182 dated questions) · crackmlinterview.com/company/openai (36 titles).

---

## 2. Anthropic

### 2.1 Process by role

- **SWE / Staff SWE:** recruiter → CodeSignal OA (90 min, 4 progressive levels, need ~520–550/600) → technical phone screen (1 coding question from the bank) → onsite: coding ×1–2, system design, technical deep dive (past project), **culture/values round** (highest failure rate). Staff+: first round is system design. No LeetCode; no AI tools in live rounds (new exception below).
- **New 2026 round — AI-enabled coding:** "This interview will evaluate your ability to write and review code using AI tools. You'll have access to the Claude Code CLI…" ⭐⭐
- **Research Engineer / Scientist:** recruiter lets you **pick the screen format** from four options: (1) Coding problem-solving, (2) Coding & Design, (3) ML Configuration System design+implement, (4) "Prompting and Engineering with LLMs" (55 min, Colab). Onsite adds ML/system design on training/inference infra, project presentation, values. Research roles may get a 48-hour problem-set take-home. Reference checks are real and early (references contacted during the loop; one candidate rejected AFTER reference check). ⭐⭐⭐
- **Performance Engineer:** 2-hour timed take-home, GPU/accelerator kernel optimization, **AI tools permitted** (see §2.5). ⭐⭐⭐
- **MLE:** CodeSignal (pure Python, no ML libs) → prompting/LLM-engineering screen → onsite incl. cloud-capacity dataset analysis, project presentation.

### 2.2 Coding questions — the numbered bank ("题号" Q1–Q6+)

Anthropic runs a small, transparent bank; recruiters often say which family you'll get. Error tolerance reported as "几乎为零" (near zero) because everyone has seen the questions.

| # | Question | Detail & follow-ups | Conf. |
|---|---|---|---|
| Q1 | **Web crawler** | Same-domain crawler with provided `get_urls(url)`; BFS single-threaded → multithreaded (bounded pool) → async; follow-ups: threads vs processes, politeness/rate limiting, distributed, dedup. | ⭐⭐⭐ |
| Q1' (2026) | **Image processing** | Grayscale/scale ops multi-part; multithread; thread-vs-process, distributed follow-ups. | ⭐⭐⭐ |
| Q2 (new) | **LRU cache debug + extend** | Given buggy Python LRU (key built from args/kwargs — find bug); add crash-resilient disk persistence; distributed follow-up. Behaves like `functools.lru_cache`. | ⭐⭐⭐ |
| Q2 (old) | **Find duplicate files** | Hash-based content dedup over a directory tree; don't load large files fully; nested dirs, distributed follow-up. | ⭐⭐⭐ |
| Q3 | **Stack-trace → profiler events** | Timestamped sampling-profiler stack samples → function start/end events (nested end first); follow-ups: ≥N consecutive samples (de-noise), recursion, longest-running function. | ⭐⭐⭐ |
| Q4 | **Distributed mode/median** | Multiset across 10 workers; `send`/`recv`/`barrier` primitives; local read 10 B/s, network 1 B/s (minimize communication); find mode, then median (median kills most candidates). | ⭐⭐⭐ |
| Q5 | **Profiler trace variant** | Unlimited execution changes between samples; functions continuous N times / over period t. | ⭐⭐ |
| Q6 | **Tokenizer debug + implement** | Buggy `tokenize`/`detokenize`; fails on out-of-vocab chars; add UNK support; token-matching efficiency, UNK-literal collisions. Also seen as "tokenization engine with text streaming." | ⭐⭐⭐ |
| — | **Claude agent loop** (2026 phone screen) | "写一个 claude agent loop，用 tools 回答股票价格计算的问题" — implement an agent loop with provided tools answering stock-price questions. | ⭐⭐ |
| — | **Bootloader** (new 2026, details unreleased) | "代码轮新题Bootloader" — poster hid details. | ⭐ |
| — | **Job scheduling** | Jobs as (start, duration) e.g. "1030 30"; minimum workers; print per-job worker assignment. | ⭐⭐ |
| — | **Text justification** | Justify a list of words within a given width. | ⭐ |
| — | **Serialize/deserialize a list of strings** | Length-prefix style encoding. | ⭐⭐ |
| — | **Thread-safe queue / concurrency round** | Dedicated concurrency interview reported on Blind. | ⭐⭐ |

### 2.3 CodeSignal OA (90 min, 4 levels) — canonical specs

- **In-memory database** ⭐⭐⭐ (the classic): L1 `SET/GET/DELETE` → L2 `SCAN`, `SCAN_BY_PREFIX` → L3 timestamps + TTL (`SET_AT`, `SET_AT_WITH_TTL`, `GET_AT`, `SCAN_AT`) → L4 file ops `COMPRESS_FILE/DECOMPRESS_FILE` w/ capacity & conflict validation. Speed >> algorithmic elegance.
- **Bank system** ⭐⭐⭐: `create_account`, `deposit`, `pay` → transfers → transaction history w/ filtering → interest/cashback with time-dependent logic (ML-intern/MATS variant).
- Other reported OA families ⭐⭐: Recipe Manager; Task Management System (priorities, worker assignment, dependency resolution, cascading cancellation); Toy App Simulation (TypeScript or Python).

### 2.4 System design questions

| Question | Detail | Conf. |
|---|---|---|
| **Deploy/distribute model weights** | ~500GB artifact to 100–1,000 GPU workers; phone variant: download+upload share 10Gbps — bandwidth allocation, P2P optimal. | ⭐⭐⭐ |
| **LLM batch-inference API** | `batch(list input) -> list output`; "100 requests take same time as 1" — queue + batch, GPU utilization; the most common onsite SD. | ⭐⭐⭐ |
| **Prompt Playground** | Anthropic-Console-like: product phase (features/UI) + technical (streaming, concurrency, global scale). Interviewer probes actively. | ⭐⭐⭐ |
| **1-1 / group chat system** | Trace data end-to-end; very deep on component connections and failure cases. | ⭐⭐⭐ |
| **Token-generation service @ 100K req/s** | Scalable LLM token generation. | ⭐⭐ |
| **File distribution / file cache** | Stream a big file from cloud storage to 1,000 machines under bandwidth constraints. | ⭐⭐⭐ |
| **Distributed rate limiter** | Globally consistent state. | ⭐⭐ |
| **Third-party API wrapper** | Uber-API ride-scheduling wrapper surviving 100x load without crushing the upstream API. | ⭐⭐ |
| **Design Claude chat service / "GPT with multiple questions per thread"** | interviewing.io reported. | ⭐⭐ |
| Others (single reports) | Distributed search (1B docs, 1M QPS); concurrent image-processing service; data-annotation platform; vector search; feature flags; distributed job queue. | ⭐ |

### 2.5 Performance / research-specific

- **Performance take-home (primary source — Anthropic's own blog):** optimize parallel tree traversal on a Python-simulated TPU-like accelerator (scratchpad memory, VLIW packing, SIMD, multicore) → v2 2h cleaner starter → v3 Zachtronics-style minimal instruction count. ~8x speedup expected per jobright; AI tools permitted. ⭐⭐⭐
- **Performance modeling round (onsite):** estimate FLOPs/data transfer/memory for matrix ops on A100; roofline compute-vs-memory-bound reasoning. ⭐⭐
- **RE ML round themes:** QKV/multi-head attention from scratch in PyTorch; debugging broken training code; loss spikes at 100B-scale pretraining; scaling-laws predictions; GRPO familiarity for RL-fundamental round. ⭐⭐
- **"Prompting and Engineering with LLMs" screen:** live prompt writing/improvement, hallucination handling, few-shot vs zero-shot. ⭐⭐⭐
- **ML Configuration System screen:** design + partially implement config system (schemas, inheritance/overrides, validation, reproducibility). ⭐⭐

### 2.6 Culture / values round (the #1 rejection point)

- "Why Anthropic?" / "What's your understanding of Anthropic's philosophy?"
- "Tell me about a time you made a safety-first decision, at a trade-off / at the cost of shipping speed."
- "What's your biggest concern about AI?" / "What concerns do you have with Anthropic's mission or direction?"
- "Tell me about a time you had a moral conflict with the work." / "…built something that went against your values."
- "What would you do if AI were starting to feel sad?" (reported via IGotAnOffer)
- "Most pressing unsolved problem in AI alignment?" / "What would change your mind about AI safety being important?"
- "Describe a technical misjudgment that delayed a project." / "A strongly held view that proved wrong." / "A time you were wrong and how you found out."
- Two interviewers, 3–4 follow-up levels deep; "closer to a therapy session than a job interview"; non-work stories acceptable. One candidate was failed after admitting they'd seen the interview question before.

### 2.7 Anthropic Fellow (AI-safety research) pipeline — CSDN/163 long-form ⭐⭐⭐

~9 hours total: (1) 90-min OA — public-API class to spec, 4 levels unlocked by tests, refactor each level, speed over Big-O; (2) 1-hr live coding — one modified LC-medium; references contacted during this stage (written feedback; proactive phone verification); (3) VO: 15-min research brainstorm with HM — two open-ended creative questions treating the LLM as a black box (3 minutes of silence = cut); 5-hour take-home — Jupyter + Anthropic API key, "probe the mysterious black box," present findings by phone; 1-hr culture fit.

---

## 3. OpenAI

### 3.1 Process by role

- **SWE:** recruiter → tech screen (60–75 min: often 1 multi-part coding + sometimes SD, or two 60-min rounds same day) → VO/onsite 4–6 rounds over 1–2 days: coding, system design ×1–2, **technical deep dive** (45 min, present a past project; "what/why/what-if" probing — hardest round per Blind), HM behavioral → hiring committee → **team matching** (a real hurdle). Senior loops may add a **48-hour paid take-home work trial under NDA (~$1,000)**. Python recommended; no AI tools in live rounds; correctness over cleverness.
- **MLE / Research Engineer:** same skeleton + **ML debugging rounds** (transformer bug-hunts) and ML system design; onsite = 2 debug + 2 coding (75/60 min) in one report. Research screens use the resumable-iterator family with TDD.
- **Research Scientist / DS:** ML coding screen (NumPy-level implementation, data analysis); take-homes for DS; math/stats orals (see §3.4).
- **New "agentic coding" round (beta):** work in an existing codebase on problems "too complex to tackle by hand" — you're graded on driving an AI coding agent. For data roles: A/B-test take-home where using ChatGPT is explicitly encouraged. ⭐⭐

### 3.2 Coding questions (the recurring bank)

| Question | Detail & follow-ups | Conf. |
|---|---|---|
| **Resumable iterator** | Abstract `ResumableIterator` with `get_state`/`set_state`; TDD (≥3 unit tests in the pad); list → file → 2D/multi-JSON-file (`MultipleResumableFileIterator`, empty-file handling) → async coroutines; skip/reset variants. THE classic OpenAI screen. | ⭐⭐⭐ |
| **Time-based / versioned / durable KV store** | Timestamped get/put; serialization w/ length-prefix encoding (values may contain delimiters); file persistence + crash recovery from log; 1KB-per-file constraint → shard across files + meta index; locking discussion: global vs per-key vs optimistic; mock timestamps in tests. | ⭐⭐⭐ |
| **GPU Credits I/II** | Credit grants with expiry; spend oldest-first; balance at timestamp; unordered timestamp arrivals force recompute/backtracking. Also appears as "Account Balance: addGrant/addSpend/getBalance". | ⭐⭐⭐ |
| **Infection / virus-spread grid simulation** | The #1 2025–2026 question. M×N grid, X infects susceptible cells; 5 escalating parts in 60 min: multi-source BFS → immune cells → threshold rules (infected if ≥K of 8 neighbors; die if >K within D days) → dynamic immunity after X days → recovery/multi-phase states. Synchronous updates (snapshot-then-swap) are the trap. Bar ≈ 3 parts clean. | ⭐⭐⭐ |
| **Toy language type system / interpreter** | Types: primitives, generics (T1…), nested tuples `[int, char, [int, T1]]`. Part 1: `__str__` for Node/Function. Part 2: `get_return_type` — bind generics from args, validate, substitute; errors on arg-count mismatch, concrete mismatch ("Expecting int but got str"), binding conflicts, tuple-shape mismatch. Interpreter variant: 75-min lexer/parser/evaluator. | ⭐⭐⭐ |
| **Spreadsheet / Excel engine** | `getCell/setCell` with formula cells + dependency graph; optimize to O(1) reads by pushing updates on write; circular-dependency detection. | ⭐⭐⭐ |
| **In-memory database** | `select(table, where=None, order_by=None)`; multi-column AND, comparison operators; INSERT; SQL-ish ops. | ⭐⭐⭐ |
| **Unix `cd` path resolution** | Resolve `..`, `.`, `~`; symlinks with cycle detection; "longer/more specific path takes precedence." | ⭐⭐⭐ |
| **Count machines in a tree / recover tree topology** | Distributed tree; only async parent-child message passing; count nodes, return topology; "Debugging a Tree class" variant. | ⭐⭐⭐ |
| **Memory allocator** | `allocate`/`free`; first-fit vs best-fit. | ⭐⭐⭐ |
| **IP address problems** | Validation/parsing; IP Iterator; IP-to-CIDR. | ⭐⭐⭐ |
| **Social network multi-part** | Feed/follow graph; A-follows-B queries; friends list; Top-K recommendations; immutable snapshots + follower index variant. 3 parts; most finish 2. | ⭐⭐⭐ |
| **Rate limiter** | Token bucket / sliding-window log; TTL cache variant; distributed extension. | ⭐⭐⭐ |
| **Concurrency problems** | 75-min locks/multithreading round; concurrency debugging in VO. | ⭐⭐⭐ |
| **Dependency version check** | Earliest version supporting a feature; adaptive binary search under noisy observations. | ⭐⭐ |
| Others (1–2 reports) | Cloud IDE implementation; all-reduce; largest sub-grid; shortest path visiting all grid points; balanced tag-pair sequence; Battle Monsters; SnapshotArray; Game of Life; Robot Room Cleaner; Word Ladder; Decode String; binary sequence → musical note durations; chess/crossword solvers. | ⭐ |

### 3.3 System design questions

| Question | Detail | Conf. |
|---|---|---|
| **Webhook delivery system** | The top SD question; ~12K/s avg, 50K/s peak, write-heavy. | ⭐⭐⭐ |
| **CI/CD job scheduler** | Multi-tenant workflow system triggered by git push; K8s/Docker; linear pipeline variant. | ⭐⭐⭐ |
| **Design Sora (video-gen service)** | Long-running GPU-bound jobs, one GPU per job, spot fleet; queueing, **preemption**, status+notify. The hot 2026 onsite question. | ⭐⭐⭐ |
| **POI (point-of-interest) service** | Yelp/Uber `get_poi`; geo-index (QuadTree), closest-N, "怎么建index，如何shard index". | ⭐⭐⭐ |
| **Chess system** | Timer design, matchmaking. | ⭐⭐⭐ |
| **Payment system** | Merchant → payment-provider path only ("不用考虑用户行为"). | ⭐⭐⭐ |
| **Remote/Cloud IDE** | Phone-screen SD. | ⭐⭐⭐ |
| **Design ChatGPT / conversational serving** | 100M MAU → ~600 msg/s; batching, KV-cache management, streaming; chat apps generally. | ⭐⭐⭐ |
| **In-memory DB design + query optimization** | SD flavor of the coding question. | ⭐⭐⭐ |
| **Slack / chat / collaborative editing** | Slack; Google-Docs-style collaboration; OpenAI Playground design (wireframes+API+schema). | ⭐⭐ |
| Others | Versioned KV store; web crawler; review site; conversation-app frontend; distributed training platform; GPU scheduling platform; embedding service w/ per-product resource isolation; RAG retrieval caching w/ model-version drift; NSFW-detection pipeline; enterprise RAG; vector DB; job scheduler; GitHub Actions; notifications; URL shortener; calendar. | ⭐–⭐⭐ |

### 3.4 ML / Research rounds

- **Transformer debugging** ⭐⭐⭐ (the signature MLE/RE round): ~300-line nanoGPT-style codebase with planted bugs in marked regions — positional embedding, causal mask, attention-score computation, output projection; loss plateaus or goes NaN; then **implement KV cache**. Two debug rounds in one onsite reported.
- **ML system design:** ML search/RAG ranking system; classifier trained on noisy human-labeled data (analysis); reliable LLM evaluation pipeline; embedding-drift detection + monitoring for a deployed retrieval system. ⭐⭐
- **Math/stats orals:** worst-case loss of cross-entropy for n classes; minimum possible LM loss (entropy of language); implement KL divergence (continuous); expected iterations of a probabilistic function; distributed averaging under noisy communication; linear algebra + backprop; vanishing/exploding gradients; BatchNorm vs LayerNorm; Bayes puzzles. ⭐⭐⭐
- **Research deep dive:** 45-min past-project presentation; historical (2018, Saining Xie account): hand-written take-home from John Schulman on variance collapse in the cross-entropy method — learn, solve, present. ⭐⭐
- **Behavioral:** "Why OpenAI"; read the Charter and have an opinion; "criteria for releasing a new AI model"; a failure; favorite AI product.

---

## 4. Google DeepMind

### 4.1 Process by role (evolution matters — old 面经 misleads)

- **The famous "Quiz" (2019–2022 canonical):** ~2 hours via Meet/Hangouts, four 30-min oral sections — **Mathematics, Computer Science, Statistics, Machine Learning**; rapid-fire "explain/derive this concept"; recruiter sends a prep PDF and pre-announces coverage.
- **2022+ London RE format:** two macro-rounds; first = **three 1-hour interviews: Math, ML, CS+coding**. Post-2023 merger: process partially aligned with Google (L-levels, hiring committee); some tracks reportedly replaced math/stats quiz with an **ML/AI quiz** (conflicting reports — both still occur). ⭐⭐⭐
- **RE loop (2024–2026):** recruiter → quiz/coding → **2 coding rounds + 2 ML rounds** (depth + breadth) → HM/team-lead + behavioral → (newer) **code-review round**. Coding is Google-style but **code must actually run in CoderPad**. ML design round added since late 2022. ~46 days to hire. AI tools prohibited.
- **RS loop:** paper/research talk (60 min, defend your own paper: methodology, weaknesses, extensions) + 30-min 1:1s with each teammate; oral quiz; ML coding; math & theory; behavioral. 2026 report of full sequence: resume deep-dive 45m → manager 30m → oral quiz 45m → 2× coding 45m → ML implementation 45m → ML debugging 45m → research talk 60m → team leads.
- **SWE:** 2 coding (med-hard DSA) + 1 SD + 1 domain-depth (ML serving/latency/deployment) + behavioral; interns: CS-fundamentals interview + coding interview.

### 4.2 Quiz / oral questions (recovered verbatim)

**Math & Stats:**
- "What is the rank of a matrix, and what does it tell you about the linear map?" · eigenvalues/eigenvectors · "What is a convex function?" · derive the MLE for the mean of a Gaussian · hypothesis testing, distributions · calculus + probability drills · expected fair coin flips until two heads in a row · functional analysis (beyond the prep PDF, for a stats PhD)
- **Bayes "colored balls" opener** ⭐⭐⭐: "bag of colored balls; given observations, probability the next ball drawn is a particular colour" — must show mathematical intuition.

**ML:**
- "Explain why L2 regularization is equivalent to a Gaussian prior on the weights" · **how gradients affect weights in L1 regularization to cause sparsity** ⭐⭐⭐ · derive ELBO for a graphical model · SVM/kernels ("if you mention SVM you must be able to explain SVM — 切忌不懂装懂") · Bayesian networks · regression · LSTM · MDPs/RL basics · compare FLOPs of VGG vs Inception vs AlexNet · derive linear regression by hand.

**CS:**
- OS: deadlocks, threading, virtual memory · floating-point representation · Python GIL · garbage collection (Java/C#), memory leaks · smart pointers · Linux commands · Big-O · 3D rotations: quaternions, gimbal lock (Games team) · code comprehension (read/explain given code).

### 4.3 Coding questions

- LC-medium + follow-ups from Google's internal bank (round 1); **LC-hard not on LeetCode** (round 2) — must run in CoderPad. ⭐⭐⭐
- Reported problems: Trie prefix matching · Snapshot Array (LC 1146) · Best Meeting Point (LC 296) · Find Median from Data Stream · parse & evaluate math expressions · basic filesystem interface in Python · linked-list openers · recursive factorial · bit manipulation · **non-LC geospatial problem whose optimal solution needs R-trees** (~100 LOC) · "write a Python generator yielding numbers from a list, plus unit tests" (software-craft check) · Monte Carlo algorithm themed as robot-vacuum coverage.
- ML coding: implement K-Means from scratch, then adapt for streaming · custom loss functions · attention mechanisms · sampling routines · multi-head self-attention from scratch, causal (no `nn.MultiheadAttention`) · LoRA, KV cache, beam search, autograd implementations (frontier-lab standard per Yuan Meng).
- ML debugging: "training script runs without errors but loss plateaus at 2.3 — find the bugs" · "pretraining loss diverges at step 300k — diagnose."

### 4.4 ML design / applied rounds

- Open-ended applied ML from **machine/fleet telemetry** (temperature, model, read/write load — design the modeling approach) ⭐⭐ — 1p3a thread 825115.
- Chemistry molecule dataset with reaction factors — modeling design. ⭐⭐
- "Training a 100B-param model overflows memory — design data/model parallelism" · distributed-training systems (pipeline/tensor parallelism, ZeRO, DeepSpeed) · evaluation infrastructure (benchmark harnesses, test-contamination handling) · YouTube recommendation · mobile autocomplete + spell-check · Applied AI Engineer: RAG retrieval, quantization/distillation, agent frameworks, evals + an ML debugging interview. ⭐⭐
- Breadth round style: interviewer **keeps adding constraints after each solution**. ⭐⭐⭐

### 4.5 HM / behavioral

- Intro, proudest project, modeling challenges, "which regularization methods," "how do you handle multi-GPU training" (HM round, 1p3a).
- "Have you trained models that use more GPU memory than available?"
- "Are you excited, terrified, or other about AI and the future? If not, why?"
- Half+ of HM time on one specific model from your resume. NDAs commonly cited by candidates.

---

## 5. Cross-company high-confidence question bank

**If you prep only 20 things** (all ⭐⭐⭐, multi-source):

1. OpenAI resumable iterator (+ TDD habit)
2. OpenAI time-based/versioned/durable KV store (+ locking discussion + file persistence)
3. OpenAI GPU credits (grant/spend/expiry)
4. OpenAI infection grid simulation (5 parts; synchronous-update semantics)
5. OpenAI toy-language type system (generics binding)
6. OpenAI spreadsheet engine (dependency graph, O(1) reads)
7. OpenAI cd/symlink resolution + in-memory DB (select/where/order_by)
8. OpenAI webhook delivery + CI/CD scheduler + Sora/GPU-preemption designs
9. OpenAI transformer-debugging round (causal mask, positional embedding, KV cache)
10. Anthropic 4-level CodeSignal in-memory DB (speed!) + bank system
11. Anthropic web crawler (BFS → bounded thread pool)
12. Anthropic LRU cache debug + persistence
13. Anthropic duplicate files / stack-trace profiler events
14. Anthropic distributed mode/median under communication limits
15. Anthropic batch-inference API + deploy-model-weights + Prompt Playground designs
16. Anthropic values round (safety-first stories, mission concerns — prep like a real round, it fails more people than coding)
17. DeepMind quiz: Bayes colored balls, MLE derivation, L1-sparsity intuition, L2-as-Gaussian-prior, eigen/rank, ELBO
18. DeepMind coding: LC-med/hard that must run + K-Means from scratch + attention from scratch
19. DeepMind ML debugging (loss plateau/divergence) + distributed-training design (ZeRO, parallelism)
20. Everywhere: 45–60-min past-project deep dive ("what/why/what-if") + reference checks + team matching

---

## 6. Caveats

- 1p3a thread dates marked "~" are inferred from thread-ID ordering; full bodies often need login/points. The Telegram mirror quotes threads directly and is the freshest free window into them.
- Interview-service sites (programhelp, oavoservice, csoahelp, libaedu) monetize 代面/cheating; their question pools mostly match community reports but contain filler — corroborate before trusting.
- One Telegram aggregator post warns some 小红书-sourced reposts may be fabricated.
- Single-source items (Anthropic "Bootloader," some SD variants) are lower confidence.
- Companies rotate banks when leaked (Anthropic revised its performance take-home 3× per its own blog; OpenAI retired some 2023 questions). Recency matters — prefer 2025–2026 threads.
- These are for **preparation**; using AI assistance or memorized verbatim solutions in live interviews violates these companies' rules (Anthropic explicitly failed a candidate who'd seen a question and one who admitted it — honesty is itself tested).

## Raw source files

- [`sources/openai-1p3a.md`](sources/openai-1p3a.md) — 30 OpenAI 1p3a thread entries
- [`sources/anthropic-1p3a.md`](sources/anthropic-1p3a.md) — 30 Anthropic 1p3a/mirror entries + question bank
- [`sources/deepmind-1p3a.md`](sources/deepmind-1p3a.md) — 22 DeepMind 1p3a entries + corroboration
- [`sources/chinese-sites.md`](sources/chinese-sites.md) — 知乎/CSDN/Telegram/牛客/小红书 sweep, 32 entries + site rankings
- [`sources/github-repos.md`](sources/github-repos.md) — 20 GitHub repos ranked, with extracted questions
- [`sources/english-niche.md`](sources/english-niche.md) — Blind/Glassdoor/interviewing.io/blogs, ~30 entries + site rankings
