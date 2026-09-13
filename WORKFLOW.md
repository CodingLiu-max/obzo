# Research workflow

## 1. Register the task

Record a short scope contract before searching:

```yaml
mode: extend-learning
topic: diffusion models
audience: graduate student
goal: understand the theory lineage and implement DDPM
include: [DPM, score matching, DDPM, continuous-time SDE]
exclude: [text-to-image products, editing applications]
time_range: through current date
paper_budget: 12
source_limit: 3
route_depth: theory-and-implementation
output_root: discovered from existing vault
zotero: mirror-and-attach-pdf
```

Infer values from the request and local files. Ask only about missing preferences that change the result.

## 2. Inspect the current system

Inventory existing folders, indexes, route/project notes, paper notes, local PDFs, Zotero collections, and duplicate records. Classify current content as:

- keep;
- link;
- enrich;
- verify;
- candidate for removal, requiring user approval.

Do not start with a new taxonomy when the current one can be extended.

## 3. Design the route map

Decompose the topic into `3–7` nodes. Use dependency order rather than popularity order.

For a learning route, check these coverage dimensions when relevant:

- prerequisites and notation;
- origin/foundation;
- canonical formulation;
- major alternative branches;
- unifying theory;
- efficient/practical development;
- evaluation, limitations, and open questions.

For an engineering route, check:

- task definition and constraints;
- closest prior work;
- datasets and preprocessing;
- metrics and evaluation scripts;
- baseline and current competitors;
- implementation components and interfaces;
- reproducibility, ablations, risks, and stop conditions.

Not every topic needs every dimension. Mark excluded dimensions rather than filling them with weak papers.

## 4. Run a bounded search

Use no more than three source classes unless the user requests a systematic review.

Default CS/AI stack:

1. OpenAlex or Semantic Scholar for discovery and citation graph traversal.
2. arXiv, DBLP, OpenReview, or the relevant venue index for field-specific coverage.
3. Official proceedings/publisher pages and Crossref for final verification.

Adapt the stack by domain, for example PubMed/PMC for biomedicine. Use available tools; do not invent access to an unavailable database.

Search in passes:

1. `seed`: exact topic, established acronym, one recent survey/tutorial, and known canonical works.
2. `node`: one focused query per route node using 2–4 discriminative terms.
3. `citation`: backward references and forward citations from the strongest seed papers.
4. `challenge`: recent top-venue work, benchmark papers, negative results, or competing branches that could invalidate the proposed route.

Keep a search log with query, source, date, filters, result count, and screening decision when the user requests reproducibility or a full system.

## 5. Screen and freeze the core corpus

Deduplicate in this order:

1. DOI;
2. arXiv or repository ID;
3. normalized title plus first author and year.

For each candidate, record:

- direct relevance to a route node;
- publication/venue status;
- route role;
- primary-source availability;
- evidence status;
- code/data availability when relevant;
- inclusion or exclusion reason.

Default core corpus is `8–15` papers, hard cap `20`. A candidate pool may be larger, but only core papers enter the main learning/engineering route. Put useful extras in a clearly optional reading section.

Freeze the corpus when:

- each required route node has at least one authoritative source;
- foundation, canonical formulation, major branch, and evaluation/current state are represented where relevant;
- two search/citation passes add no missing node;
- the paper budget is reached.

If coverage remains weak at the cap, report the gap and ask to narrow or authorize another topic pass.

## 6. Read and synthesize

Use the strongest available evidence:

- `metadata-only`: bibliographic placement only;
- `abstract-read`: problem, high-level method, claimed result, and relevance only;
- `full-text-read`: detailed method, equations, experiments, limitations, and verified comparisons;
- `user-read`: preserve the user's judgment and ask before contradicting it; verify factual metadata independently.

Synthesize by node and question, not by repeating abstracts. Create:

- lineage and dependency explanation;
- branch comparison;
- contradiction/limitation notes;
- knowledge gaps and route exclusions;
- teaching checkpoints.

Before explaining the method, write a short `领域背景与技术缺陷` bridge: summarize the field state visible in the paper's introduction and current note, identify the relevant prior limitation, and state why the paper's problem formulation is a response. Treat it as orientation, not a new survey. If the existing note lacks evidence, record `需回看原文引言/实验` and do not expand the search under an extension-only request.

## 7. Write Obsidian artifacts

Use [TEMPLATES.md](TEMPLATES.md). For existing systems, make local edits only:

- add missing links where the concept is introduced;
- keep paper information in canonical paper notes;
- keep derivations in derivation notes;
- keep implementation decisions and results in project/experiment notes;
- keep route files concise and navigational.

For a new system, scaffold only after confirming the root and naming conventions.

## 8. Mirror to Zotero

Create/reuse the matching collection hierarchy, deduplicate items, import complete metadata, attach verified PDFs, then backfill actual Zotero URIs in Obsidian. Do not leave placeholder keys in completed notes.

## 9. Validate

Check:

- route-node coverage and paper budget;
- source/evidence fields;
- filename convention;
- all Obsidian links;
- duplicate notes/items;
- Zotero collection membership;
- attachment existence and PDF validity;
- unresolved metadata and scope exclusions.

Report what was searched, why the selected corpus is sufficient for the bounded route, and what was intentionally excluded.
