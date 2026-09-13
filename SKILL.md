---
name: obzo
description: Builds or extends evidence-grounded research and learning systems in Obsidian, including bounded authoritative paper discovery, learning or engineering routes, teaching-oriented knowledge notes, canonical paper notes, and mirrored Zotero collections with verified PDFs. Use when creating a domain knowledge base, improving an existing learning/project folder, finding a compact authoritative paper route, organizing derivations and experiments, or synchronizing Obsidian with Zotero.
---

# OBZO

Build a compact, authoritative research route first; store and teach it second. Do not turn a topic into an unbounded paper dump.

## Core contract

- The user owns the topic, route boundary, time range, venues, paper budget, target depth, and final academic judgment.
- Inspect existing Obsidian and Zotero state before proposing structure. Preserve useful notes and make the smallest coherent change.
- Separate source facts, full-text findings, agent synthesis, and open questions. Never invent papers, metadata, conclusions, paths, or Zotero keys.
- Prefer route completeness over paper count: cover the necessary lineage, core mechanisms, representative branches, evaluation, and current direction.
- A bounded route is not a systematic review. Do not claim exhaustive coverage unless a documented systematic-review protocol was requested and completed.

## Select the mode

Choose one mode from the request and existing files:

1. `extend-learning`: improve an existing learning folder and learning route.
2. `extend-engineering`: improve a project/engineering folder with prior work, decisions, baselines, datasets, metrics, and implementation checkpoints.
3. `build-system`: create a complete topic knowledge base when the user asks or no usable structure exists.
4. `add-papers`: ingest a user-specified paper list without redesigning the whole route.
5. `audit`: check authority, completeness, broken links, duplicates, missing PDFs, and route gaps without expanding automatically.

If the request mixes modes, use the smallest primary mode and add only the necessary secondary work.

## Start every task

1. Read local instructions, target folder, route/project notes, paper notes, templates, indexes, derivations, and experiment records.
2. Discover the actual Zotero data/collection state. Do not guess paths or configuration.
3. Resolve the scope contract from the request: topic, audience, goal, included/excluded branches, time window, paper budget, source/venue limits, output root, Zotero/PDF expectation, and whether structure creation is allowed.
4. If a high-impact preference is missing, ask one grouped question before searching. Do not ask for facts that local inspection can answer.
5. State the target files and concise plan before editing or running import commands.

User-specified scope overrides every default below. Do not silently expand beyond it.

## Default search boundary

When the user does not set limits:

- Build `3–7` route nodes.
- Keep `8–15` core papers; hard cap `20` for one topic pass.
- Use at most `3` discovery source classes, selected for the domain.
- For each route node, prefer one foundational/canonical paper, one representative development, and one current or unifying paper when they materially differ.
- Treat citation count as a discovery clue, not proof of quality or relevance.
- Stop when every required node has authoritative support, two query/citation passes reveal no missing route node, and new results only duplicate or refine existing nodes.

Read [WORKFLOW.md](WORKFLOW.md) before any literature discovery, route construction, Zotero import, or full knowledge-base build.

## Source and evidence rules

Use sources in this order:

1. Official proceedings, journal/publisher pages, OpenReview, PubMed/PMC, or another domain primary index.
2. Author/institution pages and arXiv or another recognized preprint repository.
3. Crossref, OpenAlex, Semantic Scholar, DBLP, or equivalent scholarly indexes for discovery, citation traversal, and metadata cross-checking.
4. Surveys, courses, documentation, and expert tutorials for orientation or teaching support.
5. Blogs and videos only as optional explanations; never as the sole evidence for a paper claim.

For every core paper record:

- `source_verified`: title, authors, year, venue, DOI/arXiv, landing page, and PDF checked against a primary source.
- `evidence_status`: one of `metadata-only`, `abstract-read`, `full-text-read`, or `user-read`.
- `route_role`: one or more of `foundation`, `canonical`, `branch`, `unifying`, `benchmark`, `critical`, or `current`.
- `selection_reason`: why this paper is necessary to the route, not merely related.

Do not write detailed method claims from metadata alone. Label preprints and unresolved venue information explicitly.

## Build the route before the library

Create a route that answers:

- What prerequisite concepts must be learned first?
- What problem caused each method branch to appear?
- Which papers introduced, stabilized, unified, challenged, or evaluated the branch?
- What should the learner derive, implement, compare, or verify at each checkpoint?
- Which claims remain disputed, weakly evidenced, or outside scope?

Organize synthesis by concepts and dependencies, not by a chronological list alone. Each route node should contain:

- learning/engineering objective;
- prerequisite nodes;
- core concepts or design decisions;
- 1–3 canonical paper links with one-sentence roles;
- a derivation, implementation, experiment, or review checkpoint;
- common confusion and an exit criterion.

## Obsidian behavior

- Extend the existing hierarchy when it is coherent. Do not rename or move user files without explicit permission.
- For a learning folder, retain `学习里途.md`, `相关论文/`, and `推导笔记/`; add an index, practice notes, terminology, or search log only when required.
- For an engineering folder, ensure there is a route/overview note, related papers, decisions, implementation or experiment records, and links between claims and evidence.
- In `build-system` mode, use the minimal scaffold in [TEMPLATES.md](TEMPLATES.md), adapted to the existing vault conventions.
- Paper filename: `Model-Year-Venue.md`, such as `DDPM-2020-NeurIPS.md`. Use `arXiv` only when no verified venue exists.
- Preserve the user's prose in route files. Add readable links and concise teaching context instead of replacing their thinking with generic summaries.
- Keep one canonical note per paper. Link a paper from multiple routes rather than duplicating the note.
- Every paper note must place `## 领域背景与技术缺陷` immediately before `## 核心方法` (or `## 核心方法 Method`). It must bridge the period's field status, the relevant prior limitation, and why this paper's method is a response.
- Build that bridge from the note's verified metadata, abstract, introduction, branch placement, and existing reading notes. If the local note is insufficient, mark the missing detail as `需回看原文引言/实验`; do not invent historical claims or silently expand the search.

Read [TEMPLATES.md](TEMPLATES.md) before creating a new system, route file, engineering route, or paper note.

## Teaching and knowledge synthesis

Teach the route, not just the bibliography:

1. Explain the motivating problem before formulas or architecture details.
2. Connect each paper to what came before and what limitation it resolves.
3. Keep notation consistent across paper notes and derivation notes.
4. Include the minimum derivation needed to understand the mechanism; link deeper derivations rather than duplicating them.
5. Add common misconceptions, method boundaries, and a concrete self-check or implementation task.
6. Compare branches by assumptions, representation, objective, inference, compute, evidence, and failure modes.
7. Mark contradictions and gaps as open questions; do not manufacture consensus.

For each paper explanation, use this order: `一句话核心 → 基础信息/摘要 → 领域背景与技术缺陷 → 核心方法 → 创新点 → 证据与限制 → 学习或复现检查点`. The background section is an orientation bridge, not a second literature review.

## Zotero mirror and PDF ingestion

1. Deduplicate by DOI, arXiv ID, then normalized title.
2. Mirror the approved Obsidian topic hierarchy in Zotero; reuse existing collections and never delete legacy collections without request.
3. Store complete parent-item metadata and the verified primary abstract/landing URL.
4. Download only legally accessible original/author PDFs. Validate `%PDF`, nontrivial size, and readable page metadata before attachment.
5. Attach the PDF to the parent item with a readable filename and record the real Zotero key/URI in Obsidian.
6. Prefer Zotero's supported import/API path. Never write an active Zotero SQLite database. If a local database operation is unavoidable, close Zotero normally, back up SQLite plus journal/WAL files, use one transaction, validate, and reopen.

## Completion gates

Do not call the task complete until:

- all required route nodes are covered and optional branches are clearly labeled;
- every core-paper claim has a traceable source and evidence status;
- all Obsidian links resolve and canonical paper notes are unique;
- requested Zotero collections, items, metadata, and PDFs are present without duplicates;
- the route contains learning/engineering checkpoints rather than only descriptions;
- the user receives a concise change summary, unresolved gaps, search boundary, and next recommended checkpoint.

## Usage

Read [USAGE.md](USAGE.md) when the user asks how to invoke the skill, when scope is ambiguous, or before starting a new knowledge base. It contains copyable prompts for learning, engineering, ingestion, audit, and full-system modes.
