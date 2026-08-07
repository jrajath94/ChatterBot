# Real AI-Lab Interview Questions from Chinese-Language Sources (non-1point3acres)

## OPENAI

**Telegram 北美跳槽面经 (t.me/s/usinterview?q=%23openai) — rolling 2025–2026, freely accessible:**
- SWE phone screen (passed): Coding "GPU Credit II"; SD: design a Chess system (国际象棋).
- SWE phone screen: Coding "Versioned KV store"; "Maintain a friend follower/followee graph" (维护关注/被关注社交图).
- SWE onsite (passed): IP address problem; SD: Chess; design Sora with GPU 调度/preemption (抢占) follow-ups.
- SWE phone screen (passed): "感染" (Infection) problem, 4 parts — multi-source BFS with escalating rules; SD: Sora focusing on preemption.
- SWE phone screens: in-memory KV store with log-file recovery (系统重连后从 log file 恢复); durable KV store with file persistence + reload, follow-up 1KB file size limit (shard values across files).
- SWE phone SD: "支付系统，不用考虑用户行为，纯纯考虑商家到 payment provider" (merchant→payment-provider only).
- SWE onsite: "Social Media" multi-part problem (parts 1–3, many finish only 2); ML round: find all bugs in given model code (one candidate failed); plant infection (2.5 parts); Cloud IDE round; onsite = 4 rounds over 2 days incl. project deep dive; pipeline = phone screen → VO → hiring committee → team match.
- Research Engineer, AAI org, onsite: 45-min "technical deep dive" presentation on own project; recruiter provides onsite problem prompt in advance.

**知乎 zhuanlan (403 to fetchers; via search index):**
- https://zhuanlan.zhihu.com/p/1954883564152788970 — MLE round 1 (2025): detecting embedding drift / embedding quality degradation in a retrieval system; retrieval signals; monitoring strategies for deployed models.
- https://zhuanlan.zhihu.com/p/1924254174306100468 — Applied SDE phone (2025), 60–75 min, two engineers: SD payment system; coding: implement an IP Iterator; interviewer scoring-rubric discussion.
- https://zhuanlan.zhihu.com/p/1922101111503975390 — "小南瓜的面经笔记：OpenAI面试到底在考什么" (claims OpenAI question-design involvement): "设计带产品线资源隔离的 embedding 服务平台"; "RAG 向量检索缓存 + 模型版本漂移"; thesis: OpenAI tests bounded exploration, not memorized LeetCode.
- https://zhuanlan.zhihu.com/p/701144651 + /p/1952559408946062164 — SWE onsite fail (ex-Google) / Data Engineer phone fail (2025): 75-min coding on HackerRank-like platform; questions 偏门 (obscure), engineering-modeling not LC.

**Media/other:**
- https://m.thepaper.cn/newsDetail_forward_31507133 — Saining Xie 谢赛宁's 2018 OpenAI research interview: take-home RL problem on variance collapse in the cross-entropy method (handwritten by John Schulman); learn-solve-present in notebook; whiteboard coding + 5-hour onsite.
- https://www.libaedu.com/questions/4477_37.html — 篱笆教育 OpenAI CS bank (first ~5 free/category): Design CI/CD Job Scheduler (K8s/Docker); KVStore class w/ serialization; multi-tenant CI/CD triggered by git push; webhook delivery; POI indexing/query; in-memory DB + query optimization; Resumable Iterator; QuadTree closest-N; custom iterators; spreadsheet formula cells; "Largest Sub-Grid"; "Shortest path to visit all points on a grid"; tree topology.
- https://www.libaedu.com/questions/4477_41.html — OpenAI Data/Research bank: "Worst loss in cross-entropy for n-class classification?"; "Explain KL-Divergence"; "Minimum possible loss for a language model" (entropy of language); expectation calc; research taste from resume; ML design: build a classifier to mine data; behavioral: "tell me an experiment you've done."
- https://oavoservice.com/en/articles/openai-interview-loop-infection-bfs-type-inference-system-design — Infection-spread BFS 5 parts/60 min (immune cells, thresholds — die if >K infected neighbors within D days, recovery, synchronous snapshot-then-swap update; bar ≈ 3 parts clean); toy-language type inference (AST, structural matching, binding conflicts); SD: chat, URL shortener, payment, calendar, online games — digs into implementation and bottlenecks. Loop: recruiter → 2 tech rounds → onsite (coding, SD, technical deep dive, HM), 4–5 weeks.
- https://programhelp.net/vo/openai-interview-experience-a-must-read/ — CAUTION: cheating-service ad; plausible pool: binary sequence → musical note durations coding; Transformer attention math vs RNN limits; vanishing/exploding gradients + 3 solutions; SD: ChatGPT-like conversation system end-to-end; distributed AI training platform; BQ: technical-disagreement story. Process: recruiter 30 min → 1-hr tech screen → 3–6 onsite rounds.

## ANTHROPIC

**Telegram 北美跳槽面经 (t.me/s/usinterview?q=%23anthropic) — 2025–2026:**
- SWE technical phone screen: "写一个 claude agent loop，用 tools 回答股票价格计算问题" (implement a Claude agent loop using tools for stock-price calculation — agentic tool-use coding).
- SWE VO: Coding new question "Bootloader"; SD: "Prompt Playground" (Anthropic-Console-style prompt testing platform); project discussion round.
- SWE phone screens: image processing (图像处理, multi-part pixel manipulation); tokenization implementation; "Generate Function Profiling Events — 给一串带 timestamp 的 stack sample" (function enter/exit events from timestamped stack samples); "给一堆 job 的开始时间和时长，用最少 worker 处理完所有 job" (min workers for jobs w/ start times/durations); file-processing project round in built-in IDE.
- SWE onsite SD variants: deploy/distribute model weights; 1-1 chat system; "下载模型" — model download under bandwidth constraints; Prompt Playground; culture/values round + tech deep dive. Full-loop rejection: tokenization → image processing → Prompt Playground → deep dive → culture ("都是地里的面经题目，但很可惜还是挂了").
- MLE: 55-min "Prompting and Engineering with LLMs" screen; MLE onsite: Why Anthropic, cloud capacity management/optimization, dataset analysis, project presentation. IC7 infra loop via referral (skipped OA/screen); HM 40 min: intro, career goals, most impactful projects.

**CSDN/portals:**
- https://www.163.com/dy/article/JOMTOEL20511FQO9.html (mirror of CSDN csdnnews 145718708, 2025-02-18) — Anthropic Fellow (AI safety research), ~9 hours total:
  1. OA 90 min: build a public-API class to spec, 4 progressive levels unlocked by passing tests, refactor each level; speed over Big-O.
  2. Live coding 1 hr: one modified LeetCode-medium; Anthropic contacts references for written feedback during this stage (references required upfront).
  3. VO: (a) research brainstorm 15 min with HM — two open-ended creative questions, LLM as black box (author froze ~3 min, cut); (b) 5-hour take-home: Jupyter + Anthropic API key, "探索神秘黑箱", present findings by phone; (c) 1-hr culture fit. Portal access revoked within an hour of failing.
- https://www.sohu.com/a/862277837_413980 ("Anthropic 是如何做招聘的？", 2025-02) — corroborates the above incl. mandatory referee contacts w/ proactive phone verification.
- https://programhelp.net/vo/anthropic-interview-experience-sharing/ — CAUTION cheating-service ad; plausible pool: process LLM-generated texts (remove duplicate sentences ending .!?, filter <10-word texts, sort by length desc); distribute messages evenly across server_count servers; filter predictions below confidence threshold as "unknown"; allocate annotation tasks by difficulty/time; SD: 设计分布式 AI 训练数据标注平台 (millions of texts, real-time collab, automated QC of conflicting labels, multimodal); values: AI-ethics tradeoffs, stance on AI safety.

## GOOGLE DEEPMIND

**Telegram 北美跳槽面经 (t.me/s/usinterview?q=DeepMind) — 2025–2026:**
- RE (ML), physics PhD + 2.5-yr MLE, LinkedIn-sourced: coding round → ML round → HM + behavioral. HM topics: intro, proudest project, modeling challenges, regularization methods, multi-GPU training handling.
- RE London (Gemini post-training): recruiter round → quiz/coding 轮. Another London RE: "第一大轮是三个一小时的面试，分别是 math, ML, cs+coding".
- ML/RE coding round: "写一个 python generator 生成 list 里的数字，并写 unit tests" (non-LeetCode, software craft). ML design: modeling on a chemistry molecule dataset with reaction factors. Note: 5–6-year-old 面经 now useless — format changed.

**知乎/media:**
- https://zhuanlan.zhihu.com/p/983167020 "谷歌DeepMind面试惊险通过！面试官不让多问！" (~2024): opened with simple linked-list question then escalated; interviewer restricted clarifying questions.
- https://cloud.tencent.com/developer/news/745423 + https://xie.infoq.cn/article/8b6e812d602742affe9afdce6 "去 DeepMind 面试是怎样一种体验？" (2018, Mountain View SWE): phone 1 (app dev + design patterns), phone 2 (algorithms + teamwork); onsite 4 rounds: (1) implement a Monte Carlo algorithm themed as robot-vacuum coverage; (2) ML basics + math; (3) system design (Distinguished Engineer); (4) culture fit.
- Cross-source (2021–2025): the "Quiz" round — ~2 hours over Meet, four 30-min sections: Mathematics, CS, Statistics, ML; textbook fundamentals with derivations/intuition; recruiters pre-announce coverage; then two back-to-back Google-style coding interviews. RS loops add 60-min own-paper discussion (methodology, weaknesses, extensions) + open-ended research framing.

## RANKED SITE USEFULNESS (Chinese, non-1p3a)
1. **Telegram 北美跳槽面经 (t.me/s/usinterview)** — best: free, hashtag-searchable (#openai #anthropic #deepmind), dense 2025–2026 first-hand 面经, effectively a live 1p3a mirror.
2. **知乎 zhihu.com** — highest-quality long-form; zhuanlan 403s automated fetchers; OpenAI volume >> Anthropic/DeepMind.
3. **Interview-service sites (programhelp.net, learncswithus.com, oavoservice.com, libaedu.com)** — free and question-rich but they are 代面/OA代做 (interview-fraud) service ads; mix real pool with filler; use as corroboration only.
4. **CSDN + portal mirrors (163, sohu, thepaper, sina, tencent cloud, infoq.cn)** — CSDN 521-blocks bots but mirrors fetch freely; best long-form Anthropic process detail in Chinese.
5. **牛客网 nowcoder** — domestic companies only; near-zero A/O/D; login/JS-walled bodies.
6. **掘金 juejin** — author-composed prep listicles, JS-walled; not real reported interviews.
7. **huaren.us** — 403 to fetchers; sparse.
8. **脉脉 / 小红书** — login-walled, poorly indexed; likely has recent posts visible only in-app.

**Cross-source consistency:** OpenAI infection BFS, KV-store family, resumable/IP iterators, Sora-with-GPU-scheduling appear independently on Telegram, 知乎 snippets, libaedu, service sites. Anthropic Prompt Playground, tokenization/image-processing, agent-loop coding, references+take-home pipeline appear on Telegram, CSDN/163, sohu. DeepMind 2-hour four-section quiz + math/ML/CS trio + Python-generator-with-unit-tests appear on Telegram and tech-media reposts.
