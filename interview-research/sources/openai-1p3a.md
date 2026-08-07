# OpenAI Interview Questions — 1point3acres (一亩三分地) Research Findings

Note on method: 1point3acres itself is behind Cloudflare/login-wall (direct fetch returns 403), so details were extracted via search-index snippets of the threads, the Telegram mirror channel "北美跳槽面经" (t.me/s/usinterview, which reposts 1p3a threads with thread numbers), and summary sites that compile 1p3a content. All thread URLs below are the original 1p3a sources.

---

## Entries

### 1. OAI Research Engineer 全套面经 (Full RE loop)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1168926-1-1.html
- **Date:** ~March 2026
- **Role:** Research Engineer
- **Stage:** Full loop (phone + onsite)
- **Questions:** 5 technical rounds + 1 BQ round + 1 project deep-dive round. (Structure corroborated by multiple sources: coding, ML/system design, technical deep dive on past work, HM behavioral.)

### 2. OAI 昂赛挂经 (Onsite reject)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1066512-1-1.html
- **Date:** May 2024
- **Role:** SWE (senior)
- **Stage:** Onsite, 5 rounds
- **Questions:** Two system design rounds, one coding round, one technical deep dive (present a past project), one HM behavioral round.

### 3. Open AI 店面 (Phone screen: POI + Resumable Iterator)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1069592-1-1.html
- **Date:** June 2024
- **Role:** SWE
- **Stage:** Phone screen (店面)
- **Questions:**
  - System design: POI (Point of Interest, Yelp/Uber-style "get_poi"); interviewer drilled into "怎么建index, 如何shard index" (how to build the index, how to shard the index).
  - Coding: Resumable iterator.

### 4. OpenAI 电面挂经 (Phone screen reject: Remote IDE + GPU Credits)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1165242-1-1.html
- **Date:** ~Feb 2026
- **Role:** SWE
- **Stage:** Phone screen
- **Questions:**
  - System design: Design a Remote IDE (cloud IDE).
  - Coding: GPU Credits (credit grant/spend with expiration; deduct from oldest credits first).

### 5. OpenAI research 技术电面 (Research technical phone screen)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1111673-1-1.html
- **Date:** ~Dec 2024–Jan 2025
- **Role:** Research (Research Engineer track)
- **Stage:** Technical phone screen
- **Questions:** Classic resumable iterator, 3 parts:
  1. Define the interface for a resumable iterator (`__init__`, `__iter__`, `__next__`, `get_state`, `set_state`) and write tests.
  2. Implement a concrete resumable list iterator (index-based state).
  3. Implement a 2D resumable list iterator; variant: `MultipleResumableFileIterator` built on an existing `ResumableFileIterator` to iterate multiple JSON files, handling empty files.
  - TDD emphasized: at least 3 unit tests that must pass in the code pad.

### 6. Resumable Iterator + Time-Based KV Store + Concurrency (question-bank entry from a thread)
- **Source URL:** https://www.1point3acres.com/interview/problems/ec3912e2-0511-4700-b01b-5fad7ac3d781 (also https://www.1point3acres.com/interview/thread/1060843)
- **Date:** 2024
- **Role:** SWE
- **Stage:** Technical phone screen
- **Questions:** Implement abstract class `ResumableIterator` in Python supporting saving/restoring iterator state; write ≥3 unit tests; implement a Time-Based Key-Value Store; discuss how to lock in a multithreaded environment and compare efficiency of different lock implementations (global lock vs per-key lock vs optimistic lock).

### 7. OpenAI 店面 (Webhook + Spreadsheet)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1032241-1-1.html
- **Date:** December 2023
- **Role:** SWE
- **Stage:** Phone screen
- **Questions:** System design: Webhook (webhook delivery system); Coding: Spreadsheet (cells with formulas/dependencies).

### 8. 新鲜 OpenAI SWE VO 面经以及注意点 (Fresh SWE VO notes)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1033208-1-1.html
- **Date:** December 2023
- **Role:** SWE
- **Stage:** Virtual onsite, 4 rounds
- **Questions:** Project deep dive, HM behavioral, coding rounds (one candidate reports a transformer-related debugging coding problem). Advice in thread: read all 1p3a OpenAI posts and practice writing solutions by hand; expect new problems.

### 9. 技术筛选 (Tech screen: GPU Credits + linear CI/CD)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1126473-1-1.html
- **Date:** ~mid 2025
- **Role:** SWE
- **Stage:** Technical screen
- **Questions:** Coding: GPU Credits; System design: a linear CI/CD system (CI/CD job scheduler / pipeline).

### 10. 开放爱 ML Debug (Transformer debugging round)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1134115-1-1.html (mirrored at /interview/thread/1134115)
- **Date:** ~Sept 2025
- **Role:** ML Engineer (full-time)
- **Stage:** Tech phone screen (ML debug)
- **Questions:** Debug a Transformer model in PyTorch. Planted bugs/issues included: positional embedding, causal mask (tokens must only attend to earlier positions), output projection, and then implement KV cache as follow-up. Related bank item: minimal causal LM that "trains" but loss never improves / becomes NaN — find every bug and fix.

### 11. OpenAI RE 电面: Transformer Debug + ML search design
- **Source URL:** https://www.1point3acres.com/bbs/thread-1139045-1-1.html
- **Date:** ~Oct 2025
- **Role:** Research Engineer
- **Stage:** Tech phone screen
- **Questions:** Part 1: Transformer debug (find/fix errors in multi-head attention — linear transformations, attention score computation, position encoding). Part 2: ML system design — design an ML search system (retrieval-augmented / search ranking); poster asks whether they can request the "classifier training" question instead.

### 12. OpenAI ML Debugging 面试 (+ Linear Algebra)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1112151-1-1.html
- **Date:** ~Jan 2025
- **Role:** MLE/Research
- **Stage:** ML debugging round
- **Questions:** ML code debugging round; thread discusses linear algebra topics being asked alongside (poster offers to exchange Linear Algebra prep).

### 13. OpenAI onsite 交流 (ML onsite: 2 debug + 2 coding)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1130714-1-1.html
- **Date:** ~Aug 2025
- **Role:** MLE
- **Stage:** Onsite
- **Questions:** Two ML debugging rounds + two coding problems (75 minutes and 60 minutes). Related onsite reports: "ML puzzle + 75-minute concurrency coding (locks, multithreading)" (interview/thread/1154303) and "classifier task with human-labeled data, transformer + linear algebra discussion, backprop" (interview/thread/1147361, 1153717).

### 14. OAI 电面 coding 挂经 (IP address problem)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1165663-1-1.html
- **Date:** ~Feb 2026
- **Role:** SWE
- **Stage:** Phone screen (coding)
- **Questions:** IP address problem (IP address validation/parsing). (Same problem shows up July 2026 paired with Chess system design — thread 1181839.)

### 15. oai面试高频题目总结 — 系统篇 (High-frequency questions: systems)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1149664-1-1.html
- **Date:** October 2025
- **Role:** All engineering
- **Stage:** Compilation across phone screen + onsite
- **Questions:** High-frequency system design list including: Design CI/CD (multi-tenant CI/CD workflow system), Design Webhook delivery system, POI index + sharding (QuadTree/geo-index, closest N points), In-memory database design and query optimization, Versioned KV store, Web crawler, Chess, Sora/video-generation scheduling.

### 16. oai开放爱高频题目总结 — coding篇 (High-frequency questions: coding)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1149658-1-1.html
- **Date:** October 12, 2025
- **Role:** All engineering
- **Stage:** Compilation
- **Questions:** High-frequency coding list, including tree problems ("Count machines in a tree" — distributed tree traversal counting total machines via async parent-child message passing, special root/leaf handling; "Return tree topology"; "Debugging a Tree class"), resumable iterators, KV stores, GPU credit, spreadsheet cell update/optimize, cd-command path resolution (with `..`, `~`, symlinks, cycle detection), largest sub-grid, shortest path visiting all points on grid, all-reduce coding problem, memory allocator.

### 17. OAI system design 高频题总结
- **Source URL:** https://www.1point3acres.com/bbs/thread-1156508-1-1.html
- **Date:** December 2025
- **Role:** SWE
- **Stage:** Compilation
- **Questions:** Design webhook (top item), plus other recurring SD topics.

### 18. OpenAI Coding面经总结（至2024年底） and 系统设计面经总结（至2024年底）
- **Source URLs:** https://www.1point3acres.com/bbs/thread-1112642-1-1.html and https://www.1point3acres.com/bbs/thread-1112645-1-1.html
- **Date:** January 2025 (covers all 2024 reports)
- **Role:** All
- **Stage:** Compilation of all 2024 threads
- **Questions:** Aggregates 2024 coding questions (iterators, KV stores, spreadsheet, GPU credits, in-memory DB, cd command, tree/machine counting) and system design questions (webhook, CI/CD, POI, in-memory DB, review site, conversation-app frontend design).

### 19. 分享开放爱完整玩具语言coding题 (Full toy-language problem share)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1158706-1-1.html
- **Date:** ~Dec 2025–Jan 2026
- **Role:** SWE
- **Stage:** Coding round
- **Questions:** Toy Language Type System, full statement:
  - Grammar: primitives (char, int, float), generics (T1, T2, …), tuples (possibly nested, e.g. `[int, T1, char]`, `[int, char, [int, T1]]`).
  - Part 1: implement `to_str`/`__str__` for `Function` and `Node` classes producing e.g. `"int"`, `"T1"`, `"[int,[str,T1]]"`.
  - Part 2: implement `get_return_type` — bind generics from inputs, validate constraints, return output type with generics substituted; raise errors on argument count mismatch, concrete type mismatch, generic binding conflicts, tuple shape mismatch. (AST construction + recursive structural matching; no parsing required.)

### 20. Infection / virus-spread simulation (the current #1 coding question, multiple 2026 threads)
- **Source URLs:** https://www.1point3acres.com/bbs/thread-1183895-1-1.html, thread-1181047, thread-1181079, thread-1181839, thread-1184484 (thread numbers via Telegram mirror t.me/s/usinterview); bank page: https://www.1point3acres.com/interview/problems/company/openai/infection-spread-cellular-automata
- **Date:** July 2026 (recurring since ~2025)
- **Role:** SWE / MLE (phone screen and onsite)
- **Stage:** Coding (60 min, 5 sub-parts)
- **Questions:** M×N grid with infected cells (X) and susceptible cells (./*); infection propagates each "day" under escalating rules across 5 parts: multi-source BFS baseline; add immune units; infection thresholds; dynamic immunity ("cells become immune after X days"); recovery mechanics / multi-phase states. Passing bar reportedly = first 3 parts with clean BFS; one candidate wrote 4 parts and verbally described the 5th and passed. Difficulty is state-machine design and this-frame-vs-next-frame time semantics, not the algorithm.

### 21. July 2026 phone screens — durable/versioned KV store variants
- **Source URLs:** thread-1181536, thread-1184287, thread-1184346 (https://www.1point3acres.com/bbs/thread-1184346-1-1.html etc., via Telegram mirror)
- **Date:** July 2026
- **Role:** SWE (full-time)
- **Stage:** Phone screen coding
- **Questions:**
  - Versioned KV store; then maintain a friend/follower graph, query whether A follows B; follow-up: friends list and Top-K recommendations (thread 1181536).
  - Durable in-memory KV store with log-file recovery after crash (candidate failed for slow implementation, partial test pass — thread 1184287).
  - Durable KV store writing data to files and reloading; follow-up: each file max 1KB, so split across multiple files with a meta index file mapping keys to files, partial load (thread 1184346; same 1KB-constraint variant reported in a 90-min VO on programhelp.net mirror together with "Design Slack" system design).

### 22. July 2026 full loops — Chess / Sora / payment system designs
- **Source URLs:** thread-1181608, thread-1181839, thread-1181247, thread-1185208 (via Telegram mirror of 1p3a)
- **Date:** July–August 2026
- **Role:** SWE (full-time)
- **Stage:** Phone screen + onsite
- **Questions:**
  - Phone: GPU Credit II coding; Onsite: Infection coding + Design a Chess system (timer design, player matching probed) (1181608, 1185208).
  - Phone: IP address coding + Chess system design; Onsite: Infection (5 parts) + "Design Sora" with focus on GPU scheduling and job preemption (1181839, 1183895 — "Sora 系统设计, 重点是 preemption").
  - Phone SD: "Payment system between merchants and payment providers, excluding user behavior" — flagged as a high-frequency question (1181247).
  - Onsite coding also seen: "Social Media" multi-part problem (parts 1–2 of 3 completed) (1184859, 1185208); "Cloud IDE (non-browser) implementation" as coding part 2 (1184484).

### 23. OpenAI Fulltime SWE Onsite: Design Sora
- **Source URL:** https://www.1point3acres.com/interview/thread/1177128
- **Date:** May–June 2026
- **Role:** SWE (full-time)
- **Stage:** Onsite system design
- **Questions:** Design a video-generation scheduling service like Sora: users submit text prompts; generation is long-running (minutes) and GPU-bound (one full GPU per job) on a fleet of spot instances; users view status of all their generations and get notified on completion; discuss job scheduling, queueing, preemption, GPU fleet management. Paired VO coding reported as concurrency debugging problems (thread-1142359 area, "OpenAI VO debug 的题目", Aug 2025+).

### 24. Memory allocator phone screens
- **Source URLs:** https://www.1point3acres.com/interview/thread/1151558, https://www.1point3acres.com/interview/thread/1153768
- **Date:** ~Nov–Dec 2025
- **Role:** SWE (full-time)
- **Stage:** Tech phone screen
- **Questions:** Implement a memory allocator with `allocate` and `free` operations; strategies discussed: first-fit and best-fit.

### 25. OpenAI Applied SDE 电面 / Applied Engineer phone screen
- **Source URLs:** https://www.1point3acres.com/bbs/thread-1127065-1-1.html, https://www.1point3acres.com/bbs/thread-1111716-1-1.html
- **Date:** Jan–Jul 2025
- **Role:** Applied Engineering SWE
- **Stage:** Phone screen
- **Questions:** Resumable iterator plus LeetCode-style problems (1127065); Applied Engineer screening experience (1111716).

### 26. openai MLE 一轮游经 + 店面题目汇总 (MLE one-round exit + phone-screen question compilation)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1115238-4-1.html
- **Date:** ~Feb 2025
- **Role:** MLE
- **Stage:** Phone screen
- **Questions:** Poster compiles known OpenAI 店面 questions (resumable iterators, KV store, GPU credits, spreadsheet, transformer debug) after failing their round.

### 27. OpenAI DS 面经 (Data Science)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1168616-1-1.html
- **Date:** March 2026
- **Role:** Data Scientist
- **Stage:** Early stages
- **Questions:** Recruiter LinkedIn outreach → take-home assignment → technical phone screen.

### 28. OpenAI RE onsite exchange / team-match threads
- **Source URLs:** https://www.1point3acres.com/interview/thread/1166666, https://www.1point3acres.com/interview/thread/1169014, thread-1181194
- **Date:** Feb–July 2026
- **Role:** Research Engineer (one specifies AAI org)
- **Stage:** Onsite + post-onsite
- **Questions:** 45-minute Technical Deep Dive round — candidate picks a past project/topic and presents; interviewer explores depth ("what/why/what-if" pattern: summary, justify alternatives, fallback plans). Team-matching after hiring-committee pass frequently discussed as a separate hurdle (threads 1181608, 1184523).

### 29. OpenAI ML Coding screening (Research Scientist adjacent)
- **Source URL:** https://www.1point3acres.com/bbs/thread-1087415-1-1.html
- **Date:** September 2024
- **Role:** Research Scientist / ML
- **Stage:** Screening
- **Questions:** ML coding screen (NumPy-level implementation / data analysis / debugging emphasis rather than complex model implementation).

### 30. Other individual phone screens (2024–2025)
- **Source URLs:** thread-1049384, thread-1062239, thread-1090804, thread-1099485 ("Open AI 店面挂经 coding + system design"), thread-1105851, thread-1110720, thread-1120322, thread-1127519, thread-1131721, thread-1134619 (all https://www.1point3acres.com/bbs/thread-XXXXXXX-1-1.html)
- **Date:** 2024–2025
- **Role:** SWE
- **Stage:** Phone screen / VO
- **Questions (as surfaced in snippets):** Account Balance class — implement `addGrant`, `addSpend`, `getBalance` with timestamp tracking (GPU-credit family); versioned KV store + webhook design; custom iterator class design (senior/staff SDE onsite); in-memory database implementation ("select(table_name, where=None, order_by=None)", AND-only conditions, comparison operators); network-protocol-flavored SD.

---

## Cross-thread recurring question bank (as reported on 1p3a)

- **Coding:** Resumable iterator (list → file → 2D/multi-file, getState/setState, TDD), Time-based/versioned/durable KV store (serialization, 1KB multi-file, log recovery, locking), GPU Credits I/II (grants with expiry, spend oldest-first, unordered timestamps requiring backtracking on query), Infection/virus grid simulation (5 parts), Toy language type system / interpreter (type inference, generics), Spreadsheet/OpenSheet (formulas, dependency graph, O(1) reads via cached updates, cycle detection), In-memory database (select/where/order_by), cd/path resolution (.., ~, symlinks, cycles), Count machines in a tree (async message passing), Memory allocator (first/best fit), IP address validation, Social media graph (multi-part), Cloud IDE, concurrency debugging, all-reduce.
- **System design:** Webhook delivery, multi-tenant CI/CD workflow / job scheduler, POI geo-index + sharding (QuadTree, closest-N), Design Sora / video-generation GPU scheduling with preemption, Chess (timer, matchmaking), Payment system (merchant↔provider), Remote/cloud IDE, Slack/chat, in-memory DB design, web crawler, review site, ChatGPT-backend POI, conversation-app frontend.
- **ML rounds (MLE/RE/RS):** PyTorch transformer debugging (positional embedding, causal mask, output projection, KV cache, NaN loss), backprop questions, classifier training with human-labeled data, ML search / RAG system design, linear algebra discussion, ML puzzles, NumPy implementations.
- **Other rounds:** 45–60 min technical deep dive on a past project (research-director/bar-raiser style what/why/what-if probing), HM behavioral, team matching after hiring committee. No-AI-tools rules explicitly enforced; phone screens often one multi-part problem for the full 60–75 minutes; correctness prioritized over algorithmic cleverness.

## Best source links

1. https://www.1point3acres.com/bbs/thread-1149658-1-1.html — coding high-frequency compilation (Oct 2025)
2. https://www.1point3acres.com/bbs/thread-1149664-1-1.html — systems high-frequency compilation (Oct 2025)
3. https://www.1point3acres.com/bbs/thread-1112642-1-1.html and thread-1112645 — full 2024 coding/SD summaries
4. https://www.1point3acres.com/bbs/thread-1168926-1-1.html — Research Engineer full loop (2026)
5. https://www.1point3acres.com/bbs/thread-1158706-1-1.html — complete toy-language problem statement
6. https://www.1point3acres.com/interview/problems/company/openai — 1p3a's structured OpenAI question bank (196 questions; login-walled)
7. https://t.me/s/usinterview?q=%23openai — Telegram mirror of 1p3a threads with thread numbers (freshest 2026 data, no login)
8. https://www.libaedu.com/questions/4477_37.html — mirror listing 50 OpenAI CS questions compiled from 1p3a
9. https://www.linkjob.ai/interview-questions/openai-coding-interview/ — detailed statements of the 8 core coding problems
10. https://learncswithus.com/2026/04/04/openai-interview-problem/ — 2026 process + question-category breakdown

Caveat: thread dates marked "~" are inferred from thread-ID ordering and snippet metadata; 1p3a login-walls full bodies, so per-thread details come from search-index snippets and the Telegram mirror, which quote the threads directly.
