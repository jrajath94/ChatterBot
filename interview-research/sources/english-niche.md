# REAL Interview Questions: Anthropic / OpenAI / Google DeepMind — Niche English Sources (non-1point3acres)

Reliability tiers: [FIRSTHAND] named candidate; [FORUM] anonymous reports (Blind/HN/Glassdoor via search summaries — both block direct fetch); [AGGREGATOR] prep-site compilations (cross-check before relying).

## ANTHROPIC

### interviewing.io guide [AGGREGATOR, high quality] — https://interviewing.io/anthropic-interview-questions (2026)
- Process: recruiter (30m) → coding challenge (60–90m CodeSignal, 4 progressive levels — e.g. banking system with multiple transaction types) → onsite: HM call, coding (Python), system design (shared Google Doc), second coding/role-specific, values round.
- SD examples: "Design GPT to handle multiple questions in a single thread"; "Design the Claude chat service"; banking app architecture.
- Themes: concurrency/multithreading, data mutation, hash maps, parsing, LLM inference concepts.
- Values round: "closer to a therapy session than a job interview"; AI use strictly prohibited in interviews.

### Exponent [AGGREGATOR] — https://www.tryexponent.com/blog/anthropic-interview-process (~mid-2026)
- Coding: multithreaded web crawler; longest-running function from stack-trace samples; read & eliminate duplicate files; text justification (justify words within width); serialize/deserialize list of strings; in-memory DB progressive.
- SD: batch inferencing API; batch queries + optimize GPU usage; scalable token-generation service at 100K req/s; file distribution across thousands of machines with bandwidth constraints; file cache system.
- Values (high failure rate, two interviewers, 3–4 follow-up levels): "Tell me about a time you had a moral conflict with the work"; "What concerns do you have with Anthropic's mission or direction?"; "How do you balance delivery speed with security?"; "a time you had to build something that went against your values."

### linkjob.ai "How I Beat 2026 Anthropic Interview" — https://www.linkjob.ai/interview-questions/anthropic-interview-process/ (Dec–Feb 2025-26, offer)
- OA 90m: LRU cache (thread-safe, error handling); task management system (priorities, worker assignment, dependency resolution, cascading cancellation).
- Coding: duplicate files (chunk-based reads); multithreaded crawler; extend LRU cache for variable-length/kwargs; program start/end logs from trace data.
- SD: inference API for LLM serving — variable-length requests, GPU memory, priority queues, streaming.
- Values: Why Anthropic; understanding of Anthropic's philosophy; personal-values vs work conflict.

### Medium — Anqi Silvia, 2025 Anthropic SWE loop [FIRSTHAND] — https://medium.com/@anqi.silvia/my-2025-anthropic-software-engineer-interview-experience-9fc15cd81a99 (Sep 2025)
- 90-min coding: in-memory database 4 levels (SET/GET/DELETE → filtered scans → TTL/timestamps → file compression) — canonical OA, cross-confirmed by Blind + Glassdoor.
- Onsite SD: distributed search for 1B documents at 1M QPS — sharding, caching, GPU memory.
- Behavioral: safety-first decision; a technical misjudgment that delayed a project.

### Blind threads [FORUM] — teamblind.com (2024–2025)
- CodeSignal screen: max 600, need ~550+; 90 min in-memory DB 4 levels; speed matters most.
- Phone screen: LC-easy multi-step in Google Colab; email tells you what to prep.
- "Practical stuff like build a SQL database, implement a k/v store with disk serialization."
- Most common onsite question: batched-inference ("100 requests takes same time as 1") — queue to batch requests.
- Onsite: 4–5 rounds (2–3 coding, 1 design, 1 behavioral); dedicated concurrency-round thread exists.

### Anthropic Engineering Blog — Tristan Hume, "Designing AI-resistant technical evaluations" [PRIMARY] — https://anthropic.com/engineering/AI-resistant-technical-evaluations (Jan 2026)
- Performance Engineering take-home: v1 (Nov 2023): optimize parallel tree traversal on Python-simulated TPU-like accelerator — scratchpad memory, VLIW packing, SIMD, multicore. v2 (post-May 2025, 2h): cleaner starter, no multicore. v3 (post-Opus 4.5): Zachtronics-style tiny instruction set, minimize instruction count. Opus 4.5 hit 1,487 cycles vs best human 1,363.

### Engineering Enablement Substack [AGGREGATOR] — https://engineeringenablement.substack.com/p/anthropic-software-engineer-interview (2026)
- Coding: LRU cache; rate limiter (token bucket, distributed); time-based KV store; parse/validate structured input; thread-safe queue; grid/graph traversal with changing constraints.
- SD: prompt management platform; AI chat application (auth, streaming, monitoring); distributed job queue; vector search service; feature flag platform.

### linkjob.ai Anthropic Research Engineer — https://www.linkjob.ai/interview-questions/anthropic-research-engineer-interview-process/ (2026)
- CodeSignal 90-min take-home (or 60-min live); pair-programming/ML-engineering round; SD on large-scale model training; Transformer components from scratch in PyTorch (multi-head attention), debugging broken training code, loss spikes during 100B pretraining, scaling-laws predictions. Research roles: 48-hour problem-set/dataset take-home (also per aiofferly/finalroundai). Reference checks + team matching.

### SpaceComplexity — https://spacecomplexity.ai/blog/anthropic-onsite-interview (Jun 2026)
- Values verbatim: "Most pressing unsolved problem in AI alignment?"; "safety-first decision at cost of shipping speed"; "What would change your mind about AI safety being important?"; "a situation where you were wrong and how you found out"; "worked on something you had moral reservations about."
- Coding: LRU cache, tokenization engine with text streaming, stack-trace parsing, duplicate files.

## OPENAI

### linkjob.ai "2026 OpenAI Coding Interview Question Bank" — https://www.linkjob.ai/interview-questions/openai-coding-interview/ (8 problems + follow-ups)
1. Time-based KV Store — timestamps, file persistence, custom serialization; multithreading, future timestamps, global vs per-key vs optimistic locking.
2. cd command — relative paths, ~, symlinks with cycle detection; "longer/more specific path takes precedence."
3. Excel/spreadsheet — getCell/setCell w/ dependencies+formulas; optimize to O(1) getCell by pushing updates at setCell.
4. In-memory database — insert + WHERE (multi-column AND, comparisons) + ORDER BY.
5. Resumable iterator — getState/setState over lists and JSON files; multi-file, async coroutines, 2D/3D.
6. Distributed node counting — count machines in tree via parent-child messaging only.
7. GPU credit system — expiration/deduction/balance at timestamps; consume oldest first.
8. Dependency version check — earliest version supporting a feature; adaptive binary search.

### Interview Coder — https://www.interviewcoder.co/blog/openai-software-engineer-interview (2026)
- 6 rounds/4–6 weeks: recruiter → 60-min live coding → 48-hour PAID take-home work trial under NDA (~$1,000) → system design → behavioral/mission → offer + team match.
- 4 coding patterns: LRU cache (TTL), resumable iterator, time-based KV store, rate limiter (token bucket/sliding-window; distributed).
- SD: chat-completion serving at scale (batching, KV-cache mgmt, streaming); API platform (rate limiting, billing, quotas, back-pressure); content-moderation pipeline.
- Behavioral: read the OpenAI Charter, have an opinion.

### Hello Interview — https://www.hellointerview.com/blog/openai-coding-questions (2025) + /guides/openai/l5
- KV store serialize/deserialize w/ length-prefix encoding; time-based KV store; resumable iterator w/ skip/reset; in-memory DB with SQL ops; Unix cd w/ symlinks+cycles; SQL query executor / meeting rooms; multithreaded crawler (dedup + rate limiting); spreadsheet formulas w/ circular-dependency detection.
- L5: screen = 1 coding + 1 architecture; onsite 4–6. SD: OpenAI Playground (wireframes + API + DB schema); Slack; job scheduler; distributed KV store; rate limiter; GitHub Actions; Google Docs collaborative editing.

### crackmlinterview.com — https://crackmlinterview.com/company/openai (36 titles)
- Coding: social network w/ immutable snapshots + followers index; balanced tag-pair sequence; in-memory TTL cache (LRU); Unix cd; dependency version/adaptive binary search; grid infection & immunity; Battle Monsters; resumable iterator; GPU Credits 2; KV store; rate limiter; IP-to-CIDR; distributed cluster count; toy language type system.
- ML/design: transformer debugging; linear algebra (backprop); distributed averaging under noisy communication; noisy human-data classifier analysis; reliable LLM evaluation pipeline; design ChatGPT; distributed training platform; GPU scheduling platform; CI/CD scheduler on K8s; hosted notebook platform; RAG chatbot; chess; crossword solver.

### interviewing.io — https://interviewing.io/openai-interview-questions (2026)
- Math-flavored coding: implement KL divergence for continuous distributions; expected iterations of a probabilistic function; minimum error of a distribution using cross-entropy.
- Niche: time-based structures, versioned stores, coroutines. SD: Yelp/Foursquare/Twitter/notifications.
- New "agentic coding" round (beta): existing codebase, problems "too complex to tackle by hand," using AI coding agents.

### Blind [FORUM] (2024–2026)
- Phone screen = two 60-min rounds same day (coding + SD), different interviewers; coding LC-medium-ish.
- Onsite = 4 interviews (2 technical); project deep-dive hardest; "pre-written code" rounds (debug/extend/review); sometimes extra coding round after onsite.
- Onsite SD: chat apps, streaming platforms, payment processing, job schedulers. Python recommended.
- Data roles: product-analytics take-home on an A/B experiment where OpenAI explicitly encourages using ChatGPT — graded on guiding AI tools.

### CodingBFF Substack [FIRSTHAND] — https://codingbff.substack.com/p/i-failed-openai-senior-software-engineer (Oct 2024)
- Senior SWE (front-end leaning): SD tied to OpenAI's products — "design a chat application."

### Jobright — https://jobright.ai/blog/openai-technical-interview-questions-2026-and-how-to-answer/
- Coding: SnapshotArray; Decode String; Word Ladder; Design File System; Robot Room Cleaner; Game of Life; KV store transactional/time-travel; toy language interpreter (75-min lexer/parser/evaluator).
- SD: web crawler; rate limiter; vector database; NSFW-content detection for ChatGPT outputs; enterprise RAG.
- ML: attention complexity, vanishing gradients, BatchNorm vs LayerNorm, distributed training; Bayes puzzles. Behavioral: Why OpenAI; a failure; favorite AI product.

## GOOGLE DEEPMIND

### Aleksa Gordić [FIRSTHAND, canonical] — https://gordicaleksa.medium.com/how-i-got-a-job-at-deepmind-as-a-research-engineer-without-a-machine-learning-degree-1a45f2a781de (~2021)
- Stages: recruiter → quiz (2 back-to-back interviews) → coding → team lead → senior team lead → people & culture.
- Quiz: CS (algorithms, DS, OS: deadlocks, threading, virtual memory, Big-O), math (linear algebra, calculus, probability), statistics (hypothesis testing, distributions), ML/RL (MDPs, agent-environment).

### Blind — DeepMind RE process [FORUM] — teamblind.com/post/DeepMind-Research-Engineer-Interview-process-WP1gjGYB (~2023–24)
- 2 coding + 2 ML rounds. Coding 1: LC-medium + follow-ups (Google bank). Coding 2: LC-hard NOT on LeetCode; code must actually run in CoderPad.
- ML depth: opens with Bayes — "bag of colored balls, given observations, probability next ball is a particular colour"; mathematical intuition required, e.g. how gradients affect weights in L1 regularization to cause sparsity.
- ML breadth: design-style; interviewer keeps adding constraints after each solution.

### Blind assorted [FORUM] (2024–2026)
- Code review interview (newer RE final-stage round).
- Non-LC geospatial question needing R-trees (~100 LOC).
- Applied AI Engineer ML system design: RAG retrieval, efficiency (quantization, distillation), agent frameworks, evaluation; plus an ML debugging interview.
- RE foundational: 2-hour technical round on CS fundamentals, stats/probability, math, ML/DL/RL (classic quiz).

### carreersupport.com (Glassdoor-derived) — https://carreersupport.com/deepmind-interview-questions/ (~2024)
- RE technical (3-hr stats/ML/CS+coding): "What are eigenvalues and eigenvectors?"; "What is a convex function?"; "Have you trained models that use more GPU memory than it can handle?"
- People & Culture: "Are you excited, terrified, or other about AI and the future? If not, why?" Bayes applications; LC medium-hard.

### techinterview.org — DeepMind Process 2026 — https://www.techinterview.org/post/3233474918/deepmind-interview-process-2026/
- RS: paper discussion (60 min, defend own paper); research problem framing; ML coding (custom losses, attention, sampling); math & theory (probability, linear algebra, optimization, convergence proofs, information theory); behavioral.
- RE: ML coding (pipeline-scale); distributed training systems design (pipeline/tensor parallelism, ZeRO, DeepSpeed); evaluation infrastructure (benchmark harnesses, test contamination); algorithmic coding; behavioral.
- SWE: 2 coding (med-hard DSA), 1 SD, 1 domain-depth (ML serving/latency/deployment), 1 behavioral. AI tools prohibited.

### IGotAnOffer (403; via snippets) — https://igotanoffer.com/en/advice/google-deepmind-research-engineer-interview (~2025–26)
- "The quiz": maths, stats, core ML; format has loosened; recruiters pre-announce coverage; derive concepts (Bayes' formula + example; eigenvalues/eigenvectors) and connect to model behavior.

### Yuan Meng [FIRSTHAND] — https://www.yuan-meng.com/posts/mle_interviews_2.0/ (~2025)
- Frontier-lab LLM coding rounds: debug or implement training/inference code — Transformer encoders/decoders, LoRA, KV cache, beam search, autograd.
- RE roles: job-talk-style research presentation (~10 slides). All frontier labs do pre-offer reference checks.

### Glassdoor (blocked; snippets) — DeepMind quiz-like first interview: infrastructure, DSA, ML (regression, SVM/kernels, Bayesian networks), calculus, probability. OpenAI MTS/RE: 1-hr CoderPad Python w/ passing tests, choice among coding/ML-coding/applied-stats; attention, vanishing gradients, BatchNorm vs LayerNorm. Anthropic: in-memory DB OA, safety-first behavioral.

## RANKED niche-site usefulness (2024–2026)
1. Blind — best raw signal, all three companies; login-walled, use search snippets.
2. Hello Interview — strong current OpenAI; weak DeepMind.
3. interviewing.io — high-quality Anthropic/OpenAI process guides; nothing on DeepMind.
4. linkjob.ai — detailed question banks; unverifiable authorship, cross-check.
5. Exponent — Anthropic guide has genuine candidate-reported questions (~2026).
6. Personal blogs (Anqi Silvia, CodingBFF, Gordić, Yuan Meng) — highest trust per entry.
7. Anthropic engineering blog — primary-source take-home disclosure.
8. Interview Coder — OpenAI page good; Anthropic list mixes in wrong questions.
9. Glassdoor — real + volume but bot-blocked; many pre-2024.
10. crackmlinterview.com — useful OpenAI title inventory.
11. techinterview.org / spacecomplexity.ai / jobright.ai — SEO but some cross-confirmable specifics.
12. IGotAnOffer — fetch-blocked, partially paywalled.
13. HN (Algolia) — scattered anecdotes.
14. aonecode.com — titles only, coaching-gated.
15. Levels.fyi / Prepfully — thin.

Cross-source convergence (highest confidence): Anthropic 4-level in-memory DB OA; duplicate-files, multithreaded crawler, stack-trace-duration, batched-inference-queue; OpenAI time-based KV store, resumable iterator, cd-with-symlinks, spreadsheet, in-memory DB w/ SQL, rate limiter, GPU credits; DeepMind two-coding+two-ML with Bayes colored-balls opener and L1-sparsity intuition.
