# Anthropic Interview Questions — Real Reports from 1point3acres (一亩三分地) and Mirrors

**Access note:** 1point3acres URLs return HTTP 403 to fetchers and are login/points-walled (some threads require >200 forum points). Content recovered via Google search snippets, the Telegram mirror channel 北美跳槽面经 (t.me/s/usinterview), and secondary sites quoting 1p3a threads (linkjob.ai, prachub.com, csoahelp.com, jobright.ai, sundeepteki.org).

**Context confirmed across many threads:** Anthropic runs a small, transparent, numbered question bank ("题号" Q1–Q6+). Recruiters often tell you which question family you'll get in advance. Because everyone has seen the questions on 1p3a, error tolerance is "几乎为零" (near zero). The culture/AI-safety round is the single most common rejection point even after passing all technical rounds. No LeetCode-style algorithms; practical build/debug/scale problems.

## The reported coding question bank (esp. thread 1134248 "Anthropic VO面经 + 题号/题目猜测")

- **Q1 — Web Crawler**: same-domain crawler with provided `get_urls(url)`/`htmlParser.getUrls(url)`. Single-threaded BFS first, then parallelize (threads/ThreadPoolExecutor/processes/async). Follow-ups: threads vs processes, scheduling, politeness/rate limiting, distributed scaling, dedup of URL fragments/content. CodeSignal env; success ≈ crawl <100 URLs. (Threads 1111667, 1112541, 1116057, 1130596.)
- **Q2 — LRU Cache (debug + extend)**: existing Python LRU cache; find bug in cache-key construction from args/kwargs; add crash-resilient persistence (disk write, restore on restart). Follow-ups: CPU vs I/O bound, distributed version. "New Q2" replacing dedup files ~late 2025 (thread 1143852).
- **Q2 (older) — Find Duplicate Files**: duplicate content in a directory tree via hash; handle large files without full memory reads; follow-ups: nested dirs, distributed processing. (Threads 1123616, 1141385, 1146855; Telegram 24305.)
- **Q3 — Stack-trace / Profiler Events**: timestamped sampling-profiler stack samples → start/end trace events (nested ends before enclosing). Follow-ups: functions in ≥N consecutive samples (min_count de-noising), recursion, (depth, function_name) keys. (Telegram 29053, 24305; csoahelp Apr 2025.)
- **Q4 — Distributed Mode / Median**: huge multiset across 10 workers; primitives send/recv/barrier; find mode. Constraints: local read 10 bytes/sec, send/recv 1 byte/sec (minimize communication). Follow-up: median (several failed it). (Threads 1102889, 1148586.)
- **Q5 — Profiler Trace variant**: unlimited execution changes between samples; follow-up: functions occurring continuously N times or over period t.
- **Q6 — Tokenizer debug + implement**: buggy tokenize/detokenize; fails on chars not in vocab; implement improved version with UNK-token support; shorter-token matching efficiency, UNK literal-string collisions. (Thread 1152158 pairs Q6 with Prompt Playground SD at onsite.)
- **Image Processing ("Q1" in 2026 reports)**: grayscale, scale ops; multithreading; follow-ups thread vs process, distributed. (Thread 1171459 Apr 2026; Telegram 29098, 28946.)
- **Bootloader (new)**: "代码轮新题Bootloader没见过" — details hidden. (Telegram 28821.)
- **Job Scheduling**: jobs as (start, duration) "1030 30"; min workers; print each job's worker. (Telegram 29096, onsite.)
- **Claude Agent Loop (new phone screen)**: "写一个claude agent loop，用 tools 回答股票价格计算的问题" — agent loop with provided tools. (Telegram 28809; thread 1178346 "LLM Agent Coding Interview".)
- **AI-enabled coding round (onsite)**: "This interview will evaluate your ability to write and review code using AI tools. You'll have access to the Claude Code CLI…" (Telegram 28968.)

## The reported system-design question bank
- **SD Q1 — Deploy Model Weights**: distribute ~500GB model to 100–1,000 GPU workers; phone variant "下载模型，download和upload共用10Gbps带宽" — bandwidth allocation, P2P-style optimal solutions. (Telegram 29184, 29098; prachub.)
- **SD — Prompt Playground**: Anthropic-Console-like playground: product phase (features, UI flow) then technical (real-time execution, streaming, concurrency, global scaling). Interviewer probes actively. (Thread 1152158; Telegram 28821/28904/28946.)
- **SD Q4 — 1-1 / Resilient Chat System**: direct + group chat; trace data end-to-end; extremely deep on component connections/failure cases. (Telegram 29046, 29098.)
- **SD — LLM Batch API** (Infra SDE phone, 55 min): `batch(list input) -> list output`; request coalescing, batching, queuing, GPU utilization. (Thread 1147020, failed.)
- **SD — Concurrent Image Processing Service**: one processor safely → scale to multiple. (prachub.)
- **SD — Distributed Rate Limiter** (globally consistent) and **Uber-API ride-scheduling wrapper** (handle 100x increase; protect third-party API). (linkjob VO report.)
- **SD/analysis — Cloud capacity dataset**: dataset analysis on cloud capacity management + why anthropic + project presentation. (Telegram 28976.)

## Per-thread entries (selected)
1. thread-1134248 (~mid-2025, SWE VO) — canonical question-number thread mapping Q1–Q6; "题目都是地里的原题，容错率几乎为零".
2. thread-1111667 (~early 2025, SWE phone, fail) — web crawler w/ htmlParser.getUrls, BFS→parallel.
3. thread-1102889 (2024-25, SDE phone) — distributed mode/median.
4. thread-1147020 (~late 2025, Infra SDE phone, fail) — LLM batch API design.
5. thread-1088828 (Sep 2024, SWE OA, CodeSignal 90 min) — in-memory database 4 levels: L1 SET/GET/DELETE; L2 SCAN, SCAN_BY_PREFIX; L3 timestamps + TTL (SET_AT, SET_AT_WITH_TTL, GET_AT, SCAN_AT…); L4 COMPRESS_FILE/DECOMPRESS_FILE with capacity/conflict validation.
6. thread-1078644 (Jul 2024) — CodeSignal progressive OA, same family.
7. thread-1165574 (~mid-2026, RE/RS phone) — candidate picks one of four formats: (1) Coding problem-solving, (2) Coding & Design, (3) ML Configuration System (schemas, inheritance/overrides, validation, reproducibility), (4) Prompting and Engineering with LLMs (live prompt writing/improvement, hallucinations, few-shot vs zero-shot).
8. interview/thread/1147266 (~late 2025, Research/ML phone) — "Prompting and Engineering with LLMs": 55-min in Colab.
9. thread-1143852 (~late 2025, SWE VO) — new LRU cache Q2 (O(1) get/put, key-gen bug, crash-resilient persistence, distributed follow-up).
10. interview/thread/1141385 + 1146855 + 1123616 (2025, phone) — file dedup, several didn't finish follow-up.
11. interview/thread/1145608 (~late 2025, SWE/Performance) — Performance Modeling: GPU matrix computation on A100 — estimate FLOPs, data transfer, memory constraints; roofline reasoning (compute vs memory bound).
12. interview/thread/1137727 + 1138904 (Aug 2025, EM full VO) — 5 rounds: culture, leadership, coding, project presentation, performance modeling/design review, AI-safety culture.
13. thread-1171459 (Apr 2026, SWE phone) — image processing Q1.
14. thread-1130596 (~2025, SWE full loop fail) — crawler DFS→multithreaded.
15. thread-1116057 (~2025, SWE full loop) — crawler sync+async, duplicate files, design + culture.
16. thread-1161406 (~2026, ML fulltime VO) — CodeSignal prompt: pure Python (classes, lists, dicts, sets, sorting, hashing, binary search); no ML libs.
17. interview/thread/1162037 (~2026, ML onsite) — Python coding, screen share, explicitly NOT LLM knowledge.
18. interview/thread/1125621 (~2025, ML intern MATS CodeSignal) — multi-level bank system: create_account, deposit, pay; transfers, transaction history w/ filtering, interest/cashback with time logic.
19. Telegram 28809 / thread 1178346 (~2026 phone) — Claude agent loop w/ tools (stock prices).
20. Telegram 28821 (~2026 VO) — Bootloader coding + Prompt Playground SD + 20-min project deep dive.
21. Telegram 28946 (~2026 full loop fail) — tokenization phone → image processing, Prompt Playground, deep dive, culture; all known questions, still rejected.
22. Telegram 28968 — AI-enabled coding round w/ Claude Code CLI.
23. Telegram 29053 — Generate Function Profiling Events.
24. Telegram 29096/29098 — job scheduling; images Q1 + deploy weights SD + chat SD + "最莫名其妙的culture轮".
25. Telegram 29184 — model download SD, 10Gbps shared bandwidth.
26. Telegram 29046/29051 — 1-1 chat SD deep probing; Staff+ track first round is system design.
27. Telegram 24305 (~2025 full loop passed) — phone Q3; VO day 1: Q2 dedup + culture; day 2: tech project + SD Q1.
28. thread-1141359 (~late 2025) — rejected AFTER reference check.
29. jobright.ai 2026 guide (cites 1p3a) — Performance Engineer 2-hour timed take-home: GPU kernel optimization (loop unrolling, memory coalescing); AI tools permitted; ~8x speedup expected.
30. thread-1073090 (2024, SWE full loop fail) — 5-page discussion.

## Behavioral / culture round questions reported
- "Why Anthropic" / 为什么人类学; self-intro; most impactful project + obstacles.
- "Tell me about a time you made a safety-first/safety-related decision, even at a trade-off."
- "What's your biggest concern about AI / perspective on AI risks?"
- "Describe a technical misjudgment that delayed a project; what did you learn?"
- "What would you do if midway through a project you realized it was unfeasible?"
- "Describe a strongly held technical/product view that proved wrong." (prachub, Jul 30 2026)
- HM behavioral: impact, conflict, cross-functional, influencing without authority (STAR).
- One candidate failed at HR/culture stage after admitting they'd seen the question before.

## Best source links
1. https://t.me/s/usinterview?q=%23anthropic — Telegram mirror (posts 24302–29184, 2025–2026).
2. https://www.1point3acres.com/bbs/thread-1134248-1-1.html — question-number/bank thread (login-walled).
3. https://www.linkjob.ai/interview-questions/anthropic-coding-interview/ — 6-question bank writeup matching 1p3a numbering.
4. https://www.linkjob.ai/interview-questions/anthropic-software-engineer-interview/ — full 2026 loop + 4-level in-memory DB OA spec.
5. https://csoahelp.com/2025/04/06/anthropic-interview-breakdown-... — Q3 stack-trace walkthrough.
6. https://prachub.com/companies/anthropic — 182-question indexed bank (many locked), dates through Jul 2026.
7. https://www.sundeepteki.org/advice/anthropic-codesignal-assessment-guide — OA format, scoring (520+/600 advances), LLM anti-cheat note.
8. https://www.1point3acres.com/interview/problems/company/anthropic — 1p3a's indexed 103 Anthropic questions (login-walled).

Caveats: 1p3a dates approximate (thread IDs/snippets); Telegram post 28963 warns some XHS-sourced reposts may be fabricated; single-source items (Bootloader, job scheduling) lower confidence than multi-source ones (crawler, dedup, stack trace, distributed mode, in-memory DB OA, Prompt Playground, model-weights deployment).
