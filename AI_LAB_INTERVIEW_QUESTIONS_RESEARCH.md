# AI Lab Interview Questions — Deep Research Report
### Anthropic · OpenAI · Google DeepMind (+ xAI, Mistral, Meta FAIR)
**Compiled: 2026-08-07** · Sources: 1point3acres (一亩三分地), Telegram mirrors, csoahelp/voprep, 知乎, GitHub repos, Blind, Glassdoor, and ~60 niche prep sites, searched in both Chinese and English.

> **How to read this:** Part 1 is the source directory (where the questions live, with links and access notes). Part 2 is the compiled question bank per company and role, cross-verified across multiple independent sources. Part 3 is a freshness/reliability assessment. Content attributed to login-gated sites (1point3acres, Blind, Glassdoor, Zhihu) was recovered via search snippets and public mirrors and is flagged as such.

---

## PART 1 — SOURCE DIRECTORY

### 1.1 The core Chinese source: 1point3acres (一亩三分地)

1point3acres is the canonical Chinese-language source for US AI-lab 面经. Thread **bodies require login + 大米 (points)**, but titles/dates/roles are visible via search, and content leaks through free mirrors (§1.2).

| Link | What it is | Volume |
|---|---|---|
| https://www.1point3acres.com/bbs/tag/anthropic-9878-1.html | Anthropic company tag hub | ~519 面经 posts, 7,300 replies |
| https://www.1point3acres.com/bbs/tag/openai-9407-1.html | OpenAI company tag hub | ~700 面经 posts, 14k+ replies |
| https://www.1point3acres.com/bbs/tag/deepmind-3761-1.html | DeepMind tag hub | Dozens of threads, active thru 2026 |
| https://www.1point3acres.com/interview/problems/company/anthropic | Structured question bank — "Anthropic Interview Questions (103 questions)" | 2026-labeled |
| https://www.1point3acres.com/interview/problems/company/openai | Structured question bank — "OpenAI Interview Questions (196 questions)"; companion page claims "735 real OpenAI interview questions from 2026" | 2026-labeled |
| https://www.1point3acres.com/interview/company/DeepMind | Aggregated DeepMind question page | 2025-labeled |
| https://jobs.1point3acres.com/companies/anthropic/interview | Job多多 aggregate — 274 shared Anthropic interview experiences | live |

Notable individual threads (login-gated; captured via snippets):
- OpenAI: thread-1149658 「oai开放爱高频题目总结-coding篇」(Oct 2025 high-frequency coding list), thread-1149664 「系统篇」, thread-1156508 「OAI system design 高频题总结」, thread-1168926 「OAI Research Engineer 全套面经」(2026), thread-1165242 「OpenAI 电面挂经」, thread-1127065 「Applied SDE 电面」
- Anthropic: thread-1134248 「Anthropic VO面经+题号」, thread-1147020 「电面挂经 — design an LLM API」, thread-1165574 「Research engineer/scientist 店面问题」, /interview/thread/1152158 「SWE Onsite: Prompt Playground + Coding Q6」(2026)
- DeepMind: /bbs/interview/deepmind-machine-learning-540650.html (the canonical RE quiz 面经), thread-878129 「Google DeepMind Research Engineer 面试（进行时）」megathread (344 replies, active Jan 2026), thread-1147017 「RE 挂经」(Sep 2025)

### 1.2 Free public mirrors of 1point3acres content ⭐ (best login-free windows)

| Link | What it is | Freshness |
|---|---|---|
| **https://t.me/s/usinterview?q=%23anthropic** (also `?q=%23openai`) | Telegram channel「北美跳槽面经」— republishes 1p3a 面经 posts publicly, tagged by company, with round-by-round detail | Mid-2026, rolling |
| **https://csoahelp.com/** | Interview-assist site publishing real OA/VO write-ups (Anthropic Fellows OA May 2026, Anthropic stack-trace, OpenAI infection-grid, etc.). Question DB moved to https://voprep.com | 2023 → Jun 2026 |
| https://voprep.com/ | csoahelp's question DB — OpenAI VO series: Memory Manager, Credits w/ expiration (Oct 2025), Spreadsheet w/ dependencies | Oct–Nov 2025 |
| https://programhelp.net/ | Anthropic + OpenAI VO experience write-ups (e.g. OpenAI Design-Slack + KV-store VO, Nov 2025; Anthropic 6-stage process) | 2025–26 |
| https://learncswithus.com/2026/04/04/openai-interview-problem/ | 「OpenAI 面经汇总」— full pipeline + question taxonomy | Apr 2026 |
| https://medium.com/@programhelp/anthropic-interview-questions-2026-oa-technical-interview-breakdown-08d68034a47d | Anthropic OA breakdown (in-memory DB 4 levels incl. TTL boundary bug, bank system w/ merging) | Apr 2026 |
| https://interview-aid.com/vo/anthropic-vo-oa/ | 「Anthropic SDE 面经 2026 OA+VO 全流程」 | 2026 |
| https://oavoservice.com/articles/openai-interview-breakdown-four-interviewer-styles-project-deep-dive | OpenAI interviewer archetypes; bar-raiser round carries 40%+ weight | Jun 2026 |
| https://www.bigocodes.com/ | 面经高频题 by company/month | monthly |

⚠️ csoahelp / programhelp / interview-aid / oavoservice are interview-cheating (代面) services — their reposted questions corroborate 1p3a content, but treat marketing claims skeptically.

### 1.3 GitHub repositories

**Tier A — real, company-specific AI-lab questions:**

| Repo | Contents |
|---|---|
| **https://github.com/harry-the-nerd/interview-notes-questions** (206★) | Free mirror of darkinterview.com — per-company real questions + scaffold code: OpenAI (toy-language type system), Anthropic (multithreaded web crawler), xAI (weighted LRU cache), plus Databricks, Perplexity, Stripe, etc. Active 2025–26. **Best single repo.** |
| **https://github.com/anthropics/original_performance_takehome** (4,090★) | Anthropic's own retired Performance Engineering take-home, officially published Jan 2026 |
| **https://gist.github.com/nito-Q/3b0e09676de3b1176f85e2db3d09a9ad** | Anthropic SWE prep gist: web crawler, stack-trace conversion, duplicate file finder, LRU cache w/ persistence; OA→onsite coverage. Updated Mar–Jul 2026 |
| https://github.com/ombharatiya/FAANG-Coding-Interview-Questions (5,674★) | Company-tagged lists now incl. Anthropic, DeepMind, xAI, Mistral, Perplexity; updated Aug 2026 |
| https://github.com/fiigii/ai-comp | A compiler someone built to solve Anthropic's take-home (Feb 2026) |

**Tier B — big LLM-interview 八股 repos (great theory prep, NOT lab-specific real questions):**
- https://github.com/wdndev/llm_interview_note (14.9k★, updated Aug 2026) — largest Chinese 大模型算法岗 knowledge base
- https://github.com/alirezadir/AIMLInterviews (8.7k★, pushed Jul 2026) — ML system design + LLM/agentic additions
- https://github.com/khangich/machine-learning-interview (12.8k★) — **stale since Aug 2023**
- https://github.com/km1994/LLMs_interview_notes (2.6k★) · https://github.com/aceliuchanghong/FAQ_Of_LLM_Interview (2k★) · https://github.com/jackaduma/awesome_LLMs_interview_notes (1.3k★) · https://github.com/ckd0817/LLM-Interview-Code (771★, 手撕 code) · https://github.com/Lau-Jonathan/LLM-Agent-Interview-Guide (641★, incl. 中国大厂真题) · https://github.com/WeThinkIn/AIGC-Interview-Book · https://github.com/datawhalechina/hello-agents (Extra01 面试问题总结)

**1p3a-linked repos (pattern exists, mostly stale):** zhstark/crawler_1point3 (1p3a 面经 crawler), ersushantsood/google-prep (22 Google questions extracted from 1p3a 2026.4–5 面经 — proof the pipeline works), dotastar/interview-questions-1point3acres, WeizhengZhou/mianjing.

### 1.4 Other Chinese platforms

| Site | Finding |
|---|---|
| 知乎 Zhihu | First-person accounts: OpenAI 面试总结(挂了) https://zhuanlan.zhihu.com/p/658886757 · 2025 OpenAI MLE 一面 https://zhuanlan.zhihu.com/p/1954883564152788970 · OpenAI SDE 电面 https://zhuanlan.zhihu.com/p/1924254174306100468 · DeepMind「面试惊险通过」 https://zhuanlan.zhihu.com/p/983167020 · AIGC 大模型面经汇总 https://zhuanlan.zhihu.com/p/694464483. Blocks non-CN fetchers; readable in browser. |
| 牛客网 Nowcoder | Rich in **Chinese-company** LLM 面经 (Moonshot/字节/阿里), sparse on US labs. 大模型面经 topic: https://www.nowcoder.com/creation/subject/8603768d1f224b6bbaa48c6b32880a1a |
| 小红书 / 脉脉 | App-gated, weak SEO — their 面经 content resurfaces via 1p3a/Telegram; no directly linkable posts found |
| CSDN / juejin / blogs | 「入职OpenAI啦! AI Research面试指南」 https://blog.csdn.net/qq_27590277/article/details/150437471 (Aug 2025, by a new hire) · 26道LLM硬核题 https://juejin.cn/post/7596864700508667938 (Jan 2026) · xiaolincoding AI 面试题: https://xiaolincoding.com/other/ai.html · kamacoder 大模型面经: https://notes.kamacoder.com/interview/llm/ · meiguo.blog OpenAI offer 攻略 (2024) |

### 1.5 Western niche sites worth bookmarking

- **https://darkinterview.com/** — verified real questions for OpenAI/Anthropic/xAI/Databricks/Perplexity etc.; multiple-independent-report verification, 12-month freshness window, freemium
- **https://www.hellointerview.com/blog/openai-coding-questions** + /guides/openai/l5 — 8 real OpenAI coding write-ups
- **https://staffengprep.com/companies/openai/** — Senior/Staff-specific: 7 coding + 4 design questions
- **https://prachub.com/companies/openai** and /companies/anthropic — dated question feeds (entries through Aug 1, 2026)
- **https://www.linkjob.ai/interview-questions/anthropic-coding-interview/** (+ openai-coding-interview, anthropic-software-engineer-interview, anthropic-research-engineer-interview-process) — 2026 question banks
- **https://www.sundeepteki.org/company-guides.html** — RE/RS playbooks for OpenAI/Anthropic/DeepMind incl. the Anthropic CodeSignal guide (updated Jun 2026)
- https://www.tryexponent.com/guides/openai-research-engineer-interview-guide (+ anthropic, xai, FDE guides) — updated ~Jun 2026
- https://interviewing.io/anthropic-interview-questions and /openai-interview-questions
- https://www.cleverprep.com/companies/openai/research-engineer and /companies/anthropic/security-engineer (Jul 2026)
- https://www.techinterview.org/post/3233474918/deepmind-interview-process-2026/ (May–Jul 2026) · https://www.jobmentis.com/en/interviews/deepmind/swe (Aug 2026) · https://jobsbyculture.com/blog/deepmind-interview-prep-2026
- https://igotanoffer.com/en/advice/anthropic-interview-questions (+ openai, google-deepmind-research-engineer variants)
- https://www.coditioning.com/blog/23/openai-swe-take-home-assessment (May 2026) — OpenAI 48-h paid work-trial breakdown
- Blind threads (login req.): Anthropic megathread `6estt896`, batched-inference question `hbpacdad`, staff loop `gm5x52jt`; OpenAI coding samples `lwudq15f`, RE `6t4pl5jc`; DeepMind RE process `WP1gjGYB`; xAI weighted-LRU `3ssbshjt`; darkinterview announcement `gl33ramp`
- Glassdoor: Anthropic E8109027 · OpenAI E2210885 · DeepMind RE EI_IE1596815 pages (rolling, contribute-to-view)
- First-person write-ups: https://medium.com/@anqi.silvia/my-2025-anthropic-software-engineer-interview-experience-9fc15cd81a99 · https://medium.com/@tomzat/how-i-prepared-for-my-openai-interview-and-what-actually-helped-a185eefbafe6 · https://medium.com/@zackhui52/i-didnt-get-the-anthropic-fellowship-but-i-got-a-story-and-a-cigar-4615fea6edc0 (full Fellows loop) · https://gordicaleksa.medium.com/how-i-got-a-job-at-deepmind-as-a-research-engineer-without-a-machine-learning-degree-1a45f2a781de · https://omarreid.substack.com/p/how-to-destroy-the-deepmind-research (the Quiz) · https://trirpi.github.io/posts/anthropic-performance-takehome/
- Official: https://openai.com/interview-guide/ · https://www.anthropic.com/engineering/AI-resistant-technical-evaluations (Anthropic's own post on its take-home, Jan 2026) · DeepMind candidate PDF: https://storage.googleapis.com/deepmind-media/DeepMind.com/Assets/Docs/interviewing-at-google-deepmind.pdf

---

## PART 2 — COMPILED QUESTION BANK

## 2A. ANTHROPIC

### Process skeleton (2025–2026 consensus)
Recruiter screen (30 min, mission alignment, can fail) → **CodeSignal OA** (90 min, 4 progressive levels; sometimes waived) → HM screen → virtual onsite 4–5 hrs: 2 coding + 1 system design + experience deep-dive + **values/culture round** → 2 live reference calls → team match. Staff+ loops: ~8 interviews across two stages. 6-month cooldown on rejection. No AI tools in live rounds; LLM-based cheating detection on the OA.

### OA (CodeSignal, one evolving problem, 4 levels; ~520+/600 to advance, Fellows ≈460–600)
1. **In-memory database** (most common): L1 SET/GET/DELETE → L2 SCAN / SCAN_BY_PREFIX → L3 TTL (SET_AT/GET_AT — known trap: expiry boundary is `ts < start+ttl`, not `<=`) → L4 backup/restore or COMPRESS_FILE/DECOMPRESS_FILE
2. **Banking system**: accounts/deposits → transfers → **account merging** (balances + txn history) → cashback/interest
3. **File-system simulator**: create/read → permissions → symlinks
4. **Task management system** (4 stages, 2026)
5. Also in rotation: package manager, build system, text editor, cloud storage, inventory, logger rate limiter, hit counter
6. **Fellows OA variants**: debug a broken Extremely Randomized Trees implementation (60 min, fix crashes + accuracy, no sklearn); hand-write a **DNS resolver** (CNAME, NS fallback, caching, concurrent resolution)

### Live coding (practical "no-LeetCode" style, Python, Google Colab/CoderPad; community numbers them Q1–Q6)
1. **Web crawler** (highest frequency): BFS from seed URL, same domain, `get_urls()` helper, dedupe → make it multithreaded/async; follow-ups on threading vs multiprocessing, GIL
2. **Stack-trace / profiler samples → start-end events**: convert timestamped stack snapshots into nested start/end trace events; edge cases: single-sample flickers, recursion, functions still open at last sample; variant: longest-running function from samples
3. **LRU cache**: find a planted bug in cache-key generation → extend to disk persistence / crash recovery (refreshed version post-Sep 2025)
4. **Tokenizer**: longest-match tokenize/detokenize with unknown-token (UNK) merging; debugging variants
5. **Distributed mode-finding**: mode of a huge dataset across 10 nodes with send/recv/barrier primitives; disk 10 B/s vs network 1 B/s trade-off
6. **Bootloader** (new 2026): fix a bootloader program by swapping one instruction to avoid an infinite loop
7. **Claude agent loop** (new 2026): implement an agent loop that uses tools to answer stock-price calculation questions
8. Also reported: duplicate-file finder, text justification, serialize/deserialize string lists, job scheduling, image-processing pipelines, producer-consumer/rate limiter with concurrency follow-ups

### System design
- **Batched inference API** (the canonical Anthropic SD question): single GPU, ≤100 inputs/batch, synchronous callers — queue → batch → GPU → route responses ("100 requests take the same time as 1")
- Token-generation service at 100k RPS
- **Distribute large model weights to thousands of GPU workers** under bandwidth constraints (P2P distribution)
- **Prompt Playground / prompt-sharing product** (2026 onsite)
- Design an LLM API (+ safety layer); 1-on-1 resilient chat system (2026); concurrent image-processing service (Jul 2026); distributed search over 1B docs @ 1M QPS; GPU scheduling with credits; distributed rate limiter / job queue / KV store; ad-click aggregator (2026 VO)

### Research Engineer / Scientist
- Loop: recruiter → technical screen (CodeSignal format, **problem area emailed in advance**) → take-home (5–7 days, open-ended) → onsite: ML coding/debugging + systems + research discussion + paper discussion + culture
- Reported: build a transformer component from scratch in PyTorch; attention/BPE/sampling from scratch; "broken neural net" training-dynamics debugging; parse URLs + count domain matches → async + scaling follow-ups; scale a token-generating function to 100k RPS; critique a paper's experimental weaknesses and design a follow-up study; "design an experiment to test for an emergent capability/bias in an LLM"; "most pressing unsolved problem in alignment"; phone screen offers a choice of coding / design / ML-systems / LLM-prompting tracks

### MLE / Applied (incl. Prompt-Engineer flavor)
- 55-min hands-on **"Prompting and Engineering with LLMs"** round (Colab; build an agent loop with tool use)
- Real 2025–26 loop questions: MCP tool-planning scenario; context-window management for long-running tasks; long-context PDF reliability; guardrails/governance; Claude API design for regulated industries; hardest fine-tuning problem. Distinctive: some rounds have you use Claude as a collaborator and grade how you work with the model.

### Performance Engineer (public take-home)
- Official repo: https://github.com/anthropics/original_performance_takehome — optimize batched binary-tree traversal (256 items × 16 rounds, 6-stage hash) on a simulated VLIW SIMD machine (12 ALU, 6 VALU, 2 LOAD, 2 STORE, 1 FLOW; 1,536-word scratchpad). 2-hr timed, AI tools allowed, >600/1000 to advance; open challenge: beat 1,487 cycles → email performance-recruiting@anthropic.com. History and v2/v3 evolution: https://www.anthropic.com/engineering/AI-resistant-technical-evaluations

### Security Engineer (Jul 2026 patterns)
Detection systems for cloud-native envs; suspected-breach response; **securing ML training infra / model weights**; threat modeling; secrets management; API security at scale; supply-chain defense; LLM app security; incident-handling behaviorals.

### Culture/values round (all roles — highest failure rate)
45 min, anti-STAR. Expect: a safety-related decision you made despite trade-offs; technical misjudgment → delay; "what concerns do you have with Anthropic's mission?"; speed-vs-safety balance; ethical risks of agentic AI; "a strongly held view that proved wrong"; familiarity with Dario Amodei's essays / Constitutional AI helps. Deep-dive: https://ridhimakhurana.substack.com/p/inside-anthropics-culture-interview

---

## 2B. OPENAI

### Process skeleton
Recruiter → tech phone screen (60–75 min, sometimes 2 interviewers: coding + SD) → virtual onsite 4–6 rounds over 1–2 days: coding, system design, technical deep-dive, HM behavioral, project presentation (45 min); some loops add a **48-hour paid take-home work trial under NDA** (3–6 h real work; test rigor weighted most). Bar-raiser/Research-Director round carries ~40% of the decision. Team match after passing; downleveling common; feedback opaque. No AI tools (except a beta "agentic coding" pilot round).

### Coding (signature style: one problem, 3–5 escalating parts, 60–75 min, real test cases, high code volume)
1. **Resumable Iterator** (most-reported): iterator with `getState()`/`setState()` → over JSON files → multi-file with empty files → async version + tests
2. **In-memory SQL database**: single table → INSERT → SELECT+WHERE (AND → OR → comparison ops) → multi-column ORDER BY → joins; keep the API backward-compatible
3. **Versioned / time-based KV store**: `get(key, timestamp)` → thread-safety → persistence + custom serialization (length-prefix encoding); variants: durable KV with 1KB file segmentation + meta-index; log-based recovery
4. **GPU credit system**: add credits with expiry, spend oldest-first, balance at timestamp → out-of-order event arrival (event replay) → negative-balance failure state
5. **Unix `cd` + symlink resolution**: `..`, `~`, symlink substitution with cycle detection, longest-match precedence
6. **Spreadsheet with formula dependencies**: setCell/getCell → recursive evaluation → circular-dependency detection → O(1) reads via incremental caching
7. **Grid infection spread** (multi-source BFS, 4 parts, state-machine extensions)
8. **Memory manager** (implement malloc/free; first-fit/best-fit)
9. **Multithreaded web crawler**; **distributed-tree node counting** (async parent-child messages, failures); **dependency version check** (binary search for earliest supporting version); **SnapshotArray**; **toy-language interpreter** (lexer+parser+evaluator in 75 min); **IP-address iterator**; **token streaming buffer** (Jun 2026)
10. LC-ish tail: meeting rooms, decode string, word ladder, robot room cleaner, game of life, LRU cache, lexicographically-smallest topological order

### System design (drilled to component level, not template diagrams)
Design Slack (fan-out) · Webhook delivery @ 1B events/day · POI/Yelp search 100M+ places (index build + sharding) · **Payment system** (exactly-once charging; hold→charge→settlement) · Distributed rate limiter · **Design Sora / fault-tolerant video-gen platform / GPU job scheduler** (2026) · ChatGPT for 100M users · online chess · social graph with milestones · CI/CD system · vector DB · NSFW-detection workflow · web crawler for training data

### Research Engineer
- Loop: recruiter → 2 tech screens → 2 ML coding rounds (1 PyTorch, 1 NumPy) + 2 general coding + ML debugging → HM behavioral → 60-min past-project presentation
- Reported: hierarchical binary search for latest package-supporting Python version; instrument-notation→music-notation conversion (multi-part); implement `all_gather` over noisy channels (information-theory optimized); **find 4 bugs in a ~300-line transformer, then add KV caching**; KV-store serializer with offline state restoration; implement attention from scratch; masked cross-entropy with label smoothing; 1-NN classifier in NumPy; KL divergence for continuous distributions; expected iterations of a probabilistic function

### Research Scientist
Pre-sent paper to analyze · 20-min presentation of your work to 5–8 interviewers + Q&A · 45-min research deep-dive (derive equations, critique limitations, propose follow-ups) · coding bar shared with RE

### MLE / Applied / Infra / FDE
- MLE (2025 一面, via 知乎): serve a 20B-param model at low latency; defend against adversarial prompts; layered inference-cost optimization (caching, quantization, dynamic routing); LLM evals; embeddings
- Infra: distributed training platform design (sharding, fault tolerance, checkpoint consistency); observability across thousands of nodes; deep "why" drilling on Kubernetes/Kafka internals
- Forward-Deployed Engineer: ~1-week customer-facing take-home case study → AI-tools-allowed production coding → LLM-deployment system design → customer-empathy behaviorals
- Theory bank (juejin's 26 LLM 硬核题 + jobright): RoPE, Chinchilla scaling, KV cache, MoE, LoRA, distillation, continuous batching, RLHF/DPO/PPO, RAG + hallucination, CoT, catastrophic forgetting, eval frameworks

### Behavioral
"Why OpenAI" / mission; a failure story; favorite AI product; cross-team conflict; views on AI progress; 3-layer project interrogation (what → why-not-alternatives → what-if-it-fails)

---

## 2C. GOOGLE DEEPMIND

### Process skeleton (2026)
Recruiter → HM screen → 1–2 tech phone screens → 5–7-round loop → hiring committee (non-interviewers review standardized "Strong no hire"→"Strong hire" packets) → offer. 6–10 weeks (research tracks 2–5 months). Coding→ML rounds often gated by weeks of waiting. AI assistants banned in technical rounds. Separate loop from Google; post-2023 Brain merger unified it.

### Research Engineer — the canonical loop
1. **2 Google-style coding screens** — code must actually run in CoderPad. R1: LC-medium → med/hard follow-up → LC-easy → follow-up; R2: LC-hard "not on LeetCode". Reported: implement a Trie; bit-manipulation med-hard; derive encoding/decoding equations for bit packets; DP/CTCI-level
2. **"The Quiz"** (DeepMind's signature round; historically 2 hrs = 4 × 30-min sections, now loosened into "ML breadth"):
   - **CS**: threading, deadlocks, virtual memory, sorting complexities, paradigms, networking, Big-O
   - **Math**: eigenvalues/eigenvectors (formal definitions!), differentiate AND integrate by hand (chain rule, integration by parts), convex functions, numerical methods
   - **Stats/Probability**: balls-in-bag Bayes problems, distributions, hypothesis testing, expected value
   - **ML**: L1 vs L2 — explain sparsity via gradients; KL divergence properties; PCA ↔ largest eigenvalue of covariance; SVM/kernel SVM; Bayesian networks; MDPs/RL theory; CNNs; loss functions; "have you trained models exceeding GPU memory?"
3. **ML depth/design round**: design question with constraints added progressively; distributed training (Megatron, FSDP, ZeRO, pipeline/tensor parallelism); eval infrastructure (contamination, reproducibility)
4. Team-lead research discussion + **Googleyness / People & Culture** ("Why DeepMind, not just Google?"; "excited or terrified about AI?")
- RE-Applied (robotics) variant: kinematics, filtering, control, sensors, simulation, RL/IL quiz + easy Python coding + ML fundamentals

### Research Scientist (2026 loop)
Paper discussion (60 min, your recent work — methodology, assumptions, extensions) · research problem framing (design an investigation: experiments, metrics, falsification) · ML coding (implement attention / custom loss / sampling **without libraries**) · math & theory (probability, linear algebra, optimization, convergence proofs, KL divergence) · behavioral. HR screen → technical quiz → 2–5 (up to 9) discussion interviews with research scientists. PhD effectively required.

### SWE (incl. Staff)
2–3 coding (LC med-hard) + 1 system design + domain-depth + behavioral. Verbatim (Aug 2026, jobmentis): real-time anomalous-usage detection from interaction streams with limited memory; data structure with O(efficient) insert/delete/median; distributed real-time telemetry from AI training jobs; collaborative-editing vs async version control for model configs; shortest path in a DAG of training-task dependencies; debugging from verbose unstructured logs. One report: the "system design" round was actually a deep dive on a recent project. Staff/L6+: dedicated technical-leadership round.

### MLE / DS flavor
Implement gradient descent for logistic regression; hash map from scratch; merge intervals; cycle detection; bias-variance; imbalanced data; recsys design (YouTube/music); scale a model to billions of QPS; fault-tolerant AI app; AI-ethics behaviorals.

---

## 2D. BONUS LABS

- **xAI**: **Weighted LRU cache** (size-aware eviction; follow-ups must extend without rewrite) — harry-the-nerd repo + Blind `3ssbshjt`; guides: tryexponent xAI SWE, aiofferly xAI ML
- **Mistral**: transformer/MoE internals deep-dive; inference-at-scale design; quantization/KV-cache/batching coding; reading CUDA/vLLM code — interviewcoder.co/blog/mistral-ai-interview-questions
- **Meta FAIR**: research-design round + back-to-back research discussions; RS coding screens — 1p3a threads 1097553, 1046619, 1098164

---

## PART 3 — FRESHNESS & RELIABILITY ASSESSMENT

**Freshest (≤3 months, mid-2026):** 1p3a question banks (2026-labeled) and mid-2026 threads · Telegram t.me/s/usinterview (rolling; Anthropic threads 1180045–1184945 = mid-2026) · prachub (entries to Aug 1, 2026) · jobmentis DeepMind (Aug 5, 2026) · cleverprep (Jul 17, 2026) · csoahelp Anthropic Fellows OA (May 17, 2026) · tryexponent RE guides (~Jun 2026) · sundeepteki CodeSignal guide (Jun 2026 note re: expanded 6-part OA) · techinterview.org DeepMind (Jul 2026) · oavoservice (Jun 2026) · coditioning (May 2026) · learncswithus (Apr 2026).

**Fresh (H2 2025):** voprep OpenAI Credits (Oct 2025) · programhelp OpenAI VO (Nov 2025) · 1p3a OAI 高频总结 threads (Oct 2025) · linkjob banks · CSDN OpenAI insider guide (Aug 2025) · medium@tomzat (Nov 2025).

**Historical but load-bearing:** DeepMind Quiz first-person accounts (2019–2021 — format has since loosened; treat 4×30-min structure as baseline) · Zhihu OpenAI 面经 (2023) · early Blind threads.

**Reliability notes:**
1. **Cross-validation is strong**: the core question pools (Anthropic: crawler/stack-trace/in-memory-DB/batched-inference; OpenAI: resumable-iterator/KV-store/SQL-DB/GPU-credits/spreadsheet; DeepMind: run-your-code coding + math-stats-ML quiz) recur **independently** across Chinese and English sources from 2024→Aug 2026 — a stable pool with 2026 additions (Anthropic: bootloader, agent loop, prompt playground; OpenAI: Sora/video-gen design, memory allocator, agentic-coding beta; DeepMind: AI-training-infra-flavored SWE design).
2. **Access reality**: 1point3acres bodies need login + 大米; Zhihu/Blind/Glassdoor block scrapers. The free mirrors (Telegram channel, csoahelp/voprep, darkinterview's GitHub mirror) are the practical login-free route, and their content matches the gated snippets.
3. **Labs actively rotate questions**: Anthropic publicly documents retiring formats as Claude gets stronger (AI-resistant-evaluations post), has moved to a 6-part OA per Jun 2026 reports, and has rejected candidates suspected of having seen a question before. Treat this bank as *format + likely pool*, not a guaranteed paper.
4. **代面 caveat**: csoahelp/programhelp/interview-aid/oavoservice are interview-cheating services. Their published questions are corroborated and useful as data; their services violate every lab's interview policy (LLM-based cheating detection is confirmed at Anthropic).
5. **Negative findings**: csoahelp has no DeepMind content; Nowcoder/小红书/脉脉 have essentially no US-lab 面经 (their strength is Chinese-company LLM roles); the famous big-star ML repos (khangich, alirezadir, wdndev) contain no real lab questions.
