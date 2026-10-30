# Graph Report - ggrf-brand-assets  (2026-10-29)

## Corpus Check
- Corpus is ~40,403 words - fits in a single context window. You may not need a graph.

## Summary
- 6 nodes · 5 edges · 2 communities
- Extraction: 60% EXTRACTED · 40% INFERRED · 0% AMBIGUOUS · INFERRED: 2 edges (avg confidence: 0.95)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- (root) · GGRF e-mail signature
- (root) · E-mail template (plain)

## God Nodes (most connected - your core abstractions)
1. `E-mail template (plain)` - 3 edges
2. `GGRF e-mail signature` - 2 edges
3. `Images hotlinked from raw.githubusercontent.com (public repo)` - 2 edges
4. `E-mail template (before job)` - 1 edges
5. `E-mail template (after job)` - 1 edges
6. `index.html (identical to signature)` - 1 edges

## Surprising Connections (you probably didn't know these)
- `E-mail template (before job)` --semantically_similar_to--> `E-mail template (plain)`  [INFERRED] [semantically similar]
  template-before.html → template.html
- `E-mail template (after job)` --semantically_similar_to--> `E-mail template (plain)`  [INFERRED] [semantically similar]
  template-after.html → template.html
- `E-mail template (plain)` --references--> `Images hotlinked from raw.githubusercontent.com (public repo)`  [EXTRACTED]
  template.html → signature.html
- `index.html (identical to signature)` --semantically_similar_to--> `GGRF e-mail signature`  [EXTRACTED] [semantically similar]
  index.html → signature.html

## Communities (2 total, 0 thin omitted)

### Community 0 - "(root) · GGRF e-mail signature"
Cohesion: 0.67
Nodes (3): index.html (identical to signature), GGRF e-mail signature, Images hotlinked from raw.githubusercontent.com (public repo)

### Community 1 - "(root) · E-mail template (plain)"
Cohesion: 0.67
Nodes (3): E-mail template (after job), E-mail template (before job), E-mail template (plain)

## Knowledge Gaps
- **3 isolated node(s):** `E-mail template (before job)`, `E-mail template (after job)`, `index.html (identical to signature)`
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 3 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `E-mail template (plain)` connect `(root) · E-mail template (plain)` to `(root) · GGRF e-mail signature`?**
  _High betweenness centrality (0.100) - this node is a cross-community bridge._
- **What connects `E-mail template (before job)`, `E-mail template (after job)`, `index.html (identical to signature)` to the rest of the system?**
  _3 weakly-connected nodes found - possible documentation gaps or missing edges._

---

## Build notes (audit 29.10.2026, Perplexity Computer)

- Built at commit `6936720a963a`, graphify 0.9.92 (pinned checkout 86c57be), **directed** graph, full rebuild (no --update).
- Corpus: 12 files detected (0 code, 5 document, 0 paper, 7 image, 0 video). Excluded directories: graphify-out, node_modules, vendor, dist, build, .next, __pycache__, .venv, venv.
- Extraction: 0 AST nodes / 0 AST edges (tree-sitter, deterministic); 6 semantic nodes / 5 semantic edges written by the Computer model from 5 key documents only (listed below). Images, PDFs, spreadsheets and most Markdown files did **not** get semantic extraction.
- Raw extraction (all nodes, edges, relation types, confidence, source paths/locations, `_origin`) preserved in `graphify-out/extraction.json`.
- Graph after reduction: 6 nodes, 5 edges, 2 communities. A graph path is not a call chain; communities are heuristics.
- Community labels were generated **heuristically** (dominant top-level directory + highest-degree node label), not curated by hand.
- Token counters are 0 because semantic extraction ran inside the Computer session and was not metered; this is "not measured", not "free".
- Health check: Graph health: OK (no dangling/missing/collapsed edges).

```
[graphify] MultiDiGraph edge-collapse diagnostic
input: <in-memory>
input_stage: provided JSON (normal graph.json is post-build)
effective_directed: <direct-call>
nodes: 6
unverified_code_nodes: 0
raw_edges: 5
valid_candidate_edges: 5
missing_endpoint_edges: 0
dangling_endpoint_edges: 0
external_reference_edges: 0
self_loop_edges: 0
exact_duplicate_edges: 0
directed_unique_endpoint_pairs: 5
directed_same_endpoint_collapsed_edges: 0
undirected_unique_endpoint_pairs: 5
undirected_same_endpoint_collapsed_edges: 0
same_endpoint_group_count: 0
relation_variant_groups: 0
source_file_variant_groups: 0
source_location_variant_groups: 0
context_variant_groups: 0
post_build_graph_type: DiGraph
post_build_edges: 5
producer_suppression_sites: 12
producer_suppression_examples:
  - L1789 seen_ids arity=unknown
  - L2353 seen_ids arity=unknown
  - L2355 seen_doc_refs arity=unknown
  - L3022 seen_ids arity=unknown
  - L3169 seen_ids arity=unknown
  - L4179 seen_keys arity=unknown
  - L4365 seen_keys arity=unknown
  - L7608 seen_ids arity=unknown
note: normal graph.json is post-build; raw producer loss must be measured earlier.
```

- Files skipped as sensitive by the detector: none.
- Documents with semantic extraction: `index.html`, `signature.html`, `template-after.html`, `template-before.html`, `template.html`
