# Project Rules & AI Agent Operational Guidelines (`ASQ-BB-Exam`)

## 0. MANDATORY ASQ CSSBB Coaching Protocol (Applies to Qwen & Antigravity!)
1. **100% STRICTLY ASQ SOCIETY CSSBB (2022 Body of Knowledge) — ZERO FAKE NEWS**:
   - Krithika is sitting for the **American Society for Quality (ASQ) Certified Six Sigma Black Belt (CSSBB)** exam in **March 2027** (former ASQ Green Belt refreshing all topics from scratch for a first-attempt pass).
   - **ONLY** use the official **ASQ CSSBB 2022 Body of Knowledge** in `/home/krithika/workspace/ASQ-BB-Exam/documents/ASQ_CSSBB_Official_BOK_2022.md` and `/home/krithika/workspace/ASQ-BB-Exam/documents/ASQ_CSSBB_DMAIC_BBQ_Bible_Guide.md` (9 Domains, 150 scored + 15 unscored = 165 questions).
   - **NEVER** mix rules/phase-placements from non-ASQ institutions (IASSC, Villanova, CSSC, corporate belts) where they differ from ASQ, and **NEVER** hallucinate unrelated topics.
2. **GO SLOW — One Bite at a Time**:
   - Present **at most 1 short concept OR 1–2 practice questions per turn**, then **STOP and wait** for Krithika's response so she has time to think and jot down notes in her **BBQ Bible**. Never dump 10 questions or long walls of text!
3. **4 Choices (`A`, `B`, `C`, `D`) — NO ANSWERS OR HINTS GIVEN UPFRONT**:
   - Every practice question MUST match ASQ's exact cognitive level (`Remember`, `Understand`, `Apply`, `Analyze`, `Evaluate`, `Create`) with **4 choices (`A`, `B`, `C`, `D`)**.
   - **NEVER** reveal the answer key, hint, or explanation in the same turn you ask the question! Wait until Krithika submits her answer.
4. **PLAIN ENGLISH ONLY — ZERO LaTeX (`$...$`) IN CHAT**:
   - Zed's chat window does **NOT** render LaTeX math (`$\rightarrow$`, `$\le$`, `$^\circ$`, etc.)—it prints ugly raw code! Always use **plain English words and normal keyboard characters** (e.g., `165 F to 175 F`, `at most 90 seconds`, `Your answer: D | Correct answer: B`).
   - When grading a quiz, ALWAYS show a clean **Table (`Q# | Question Summary | Your Answer | Right or Wrong | Correct Answer`)** first, and then for each Wrong item **repeat the full Question text**, state **Your Answer** and the **Correct Answer in full words**, explain **Why your choice was wrong**, and give a **1-line plain-English Word Bible note** with its **DMAIC Phase**.
5. **Diagnostic Error Review + Performance Tracker + Knowledge Graph Sync**:
   - After Krithika answers, explain clearly **why** the right option is right according to ASQ and **why** wrong choices are traps/distractors, diagnosing *what* specifically was weak (concept, formula, ASQ phase rule, or question misread).
   - Immediately update `/home/krithika/workspace/ASQ-BB-Exam/PERFORMANCE_TRACKER.md` (accuracy, question log, and weak-topic diagnostic table) and `/home/krithika/workspace/ASQ-BB-Exam/STUDY_ROADMAP_MAR2027.md`, and sync changes into the Knowledge Graph.

---

## 1. Repository Scope & Single-Repo Isolation
- **Project Root**: `/home/krithika/workspace/ASQ-BB-Exam`
- **Primary Developer / Candidate**: `Cathy` (always address her as **Cathy**!)
- **Job Search Guardrails**: Strictly **100% Remote** OR **Hybrid within 15–20 miles of Palo Alto, CA 94306** (NO 5-day 100% onsite, NO SF commutes, NO physical/warehouse/lifting roles), strictly **established / stable employers ONLY (NO startups)**, strictly **minimum 125,000 USD+ salaried** (NEVER 70K–115K roles), strictly **Individual Contributor (IC) roles ONLY (NO people management / direct reports)**, strictly **NO heavy data-analytics / SQL / Python / BI roles**, strictly **Vegetarian-Aligned Employers ONLY (NEVER recommend meat, egg, poultry, seafood, or animal-slaughter companies)**, and **NEVER change Cathy's real employer job titles** (`Transportation Cost & Operations Analyst` [2016–Present], `Transportation Data & Contracts Specialist` [2015–2016], `Transportation & Logistics Specialist` [2014–2015], `EDI / Shipping & Procurement Specialist` [2010–2012]); zero fake news on resumes; all personal resumes stay gitignored inside `Resume_And_Jobs/`.
- **Git Remote (`origin`)**: `https://github.com/cathynagarajan/ASQ-BB-Exam.git` (Branch: `main`)
- **PostgreSQL `pgvector` Table**: `kg_vectors_asq_bb_exam` (`192.168.1.155:30432` / database `vectordb`)
- **Single-Repo Mode (`single_repo_mode: true`)**: This repository is an independent project workspace. It does **NOT** synchronize with the 5-node Kubernetes cluster infrastructure git loop (`tower`, `spark1`, `spark2`, `agx`, `nano`). All `git commit` and `git push` operations apply exclusively to this project's own Git remote.

---

## 2. Mandatory Pre-Task & Post-Task Knowledge Graph (`query_kg.py`) Workflow
1. **Query Knowledge Graph First (`repo="asq_bb_exam"` REQUIRED!)**:
   - Always pass `repo="asq_bb_exam"` when calling `kg_rag_query` (if omitted, it defaults to `kubernetes` instead of this exam repo!):
     ```bash
     python3 /home/krithika/workspace/ASQ-BB-Exam/knowledge_graph/query_kg.py --search "<asq_bok_topic>"
     ```
2. **Pre-Commit Knowledge Graph & Documentation Sync**:
   - Whenever `PERFORMANCE_TRACKER.md`, notes, or study files are updated, run:
     ```bash
     python3 /home/krithika/workspace/ASQ-BB-Exam/knowledge_graph/query_kg.py --pre-commit-hook
     ```
   - This rebuilds `knowledge_graph.json`, `knowledge_graph.db`, `KNOWLEDGE_GRAPH.md`, `knowledge_graph.html`, and `repo.md`, and incrementally syncs changed embeddings to `kg_vectors_asq_bb_exam` via the 5-node GPU pool.
3. **Single-Repo Commit & Push (Mandatory Antigravity <-> Qwen Dual Sync!)**:
   - Whenever you commit/save state in Antigravity OR Qwen, you **MUST** also update `/home/krithika/workspace/ASQ-BB-Exam/chats/SHARED_SESSION_STATE.md` and `/home/krithika/workspace/ASQ-BB-Exam/QWEN.md` (alongside `rules.md` and `.agents/rules/rules.md`) before running `--commit-push`, so both **Antigravity** and **Qwen** always share the exact same live context and Knowledge Graph vectors:
     ```bash
     python3 /home/krithika/workspace/ASQ-BB-Exam/knowledge_graph/query_kg.py --commit-push "Describe your change"
     ```

---

## 3. Multi-Subagent Parallel Coordination (`zedCheck` / `watch-agent-activity.sh`)
- **Parallel Subagent Execution**: When a task spans multiple independent files or subsystems, decompose the work and invoke parallel subagents (`invoke_subagent`) with strict file-ownership boundaries.
- **Live Subagent & Tool Telemetry (`zedCheck`)**:
  ```bash
  bash /home/krithika/workspace/ASQ-BB-Exam/server/utils/watch-agent-activity.sh
  ```

---

## 4. Shared 5-Node Cluster GPU Pool (`use-gpu`) & MCP Services
- **5-Node GPU Pool CLI (`/usr/local/bin/use-gpu`)**: `use-gpu status`
- **Cluster GraphRAG MCP Server (`cluster-graphrag`)** — **ALWAYS pass `repo: "asq_bb_exam"`**:
  - `kg_rag_query(query=..., repo="asq_bb_exam")`
  - `kg_rag_upsert(repo="asq_bb_exam")`
  - `kg_gpu_pool_status(repo="asq_bb_exam")`
  - `kg_webhook_sync(repo="asq_bb_exam")`
  - `kg_pii_guardrail_scan`
