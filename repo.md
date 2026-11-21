# Repository Top-Level Parent Folders Processed by Knowledge Graph (`repo.md`)

This file maintains the authoritative inventory of all **top-level parent folders** in `/home/krithika/workspace/ASQ-BB-Exam` that are scanned, parsed, and indexed by [`knowledge_graph/query_kg.py`](knowledge_graph/query_kg.py).

- **Repository Root**: `/home/krithika/workspace/ASQ-BB-Exam`
- **Top-Level Parent Folders Processed**: `3` (plus repository root `.` files)
- **Total Indexed Files**: `97`
- **Total Knowledge Graph Nodes**: `956`

---

## 1. Top-Level Parent Folders Processed by Knowledge Graph

| # | Top-Level Parent Folder | Absolute Path | Indexed Files | Extracted KG Nodes | Key Subfolders | Description & Scope |
| :---: | :--- | :--- | :---: | :---: | :--- | :--- |
| 1 | [`Resume_And_Jobs/`](Resume_And_Jobs) | `/home/krithika/workspace/ASQ-BB-Exam/Resume_And_Jobs/` | `77` | `367` | — | Top-level repository folder `Resume_And_Jobs/` indexed by Knowledge Graph |
| 2 | [`chats/`](chats) | `/home/krithika/workspace/ASQ-BB-Exam/chats/` | `1` | `175` | — | Exported or synced Zed/Antigravity AI assistant chat transcripts and conversation logs indexed into the Knowledge Graph |
| 3 | [`documents/`](documents) | `/home/krithika/workspace/ASQ-BB-Exam/documents/` | `15` | `410` | — | Multi-modal documents, PDFs, Office files (`.docx`, `.pptx`, `.xlsx`), CSV/TSV datasets, OCR images, and audio recordings indexed into the Knowledge Graph |

### Repository Root (`.` Top-Level Files)

| Location | Absolute Path | Indexed Root Files | Extracted KG Nodes | Description |
| :--- | :--- | :---: | :---: | :--- |
| `.` (Root Files) | `/home/krithika/workspace/ASQ-BB-Exam/` | `4` | `4` | Repository root configuration, rules, and entrypoints (`network_config.json`, `rules.md`, `resources.md`, `repo.md`, `global.md`, `CLAUDE.md`, `README.md`, `query_kg.py`) |

---

## 2. Entity Breakdown by Top-Level Parent Folder

| Top-Level Parent Folder | Extracted Entity Types (`type: count`) |
| :--- | :--- |
| `Resume_And_Jobs/` | `document`: 45, `document_file`: 32, `document_section`: 182, `topic_entity`: 108 |
| `chats/` | `chat_session`: 6, `chat_turn`: 48, `topic_entity`: 121 |
| `documents/` | `document`: 4, `document_file`: 10, `document_section`: 111, `html_template`: 1, `topic_entity`: 284 |
| `.` (Root Files) | `document`: 4 |

---

## 3. Excluded Top-Level & Generated Directories

The following directories are intentionally excluded from Knowledge Graph source indexing to avoid recursion, virtual-environment bloat, or binary cache scanning:

| Excluded Directory | Reason |
| :--- | :--- |
| `.git/` | Git version control internals |
| `.mypy_cache/` | Mypy type-checking cache |
| `.pytest_cache/` | Pytest execution cache |
| `.venv/` | Python virtual environment |
| `__pycache__/` | Compiled Python bytecode cache |
| `jvm/` | Extracted SAPJVM runtime binary archive |
| `knowledge-graph/` | Legacy Knowledge Graph directory alias |
| `management_venv/` | Python virtual environment for cluster-management |
| `node_modules/` | Node.js dependency directory |
| `pgvector_repo/` | External cloned pgvector source repository |
| `retire/` | Archived/retired node scripts preserved for reference |
| `venv/` | Python virtual environment |
| `wheels/` | Pre-built Python binary wheel archive |

---

## 4. Synchronization Rule

Whenever a top-level folder is added, renamed, or removed in `/home/krithika/workspace/ASQ-BB-Exam`, running:
```bash
python3 /home/krithika/workspace/ASQ-BB-Exam/knowledge_graph/query_kg.py --update
```
automatically updates `repo.md` alongside the Knowledge Graph stores.
