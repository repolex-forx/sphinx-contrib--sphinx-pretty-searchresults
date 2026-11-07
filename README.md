# Repolex Knowledge Graph of sphinx-contrib/sphinx-pretty-searchresults

RDF knowledge graph data for [sphinx-contrib/sphinx-pretty-searchresults](https://github.com/sphinx-contrib/sphinx-pretty-searchresults), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download sphinx-contrib/sphinx-pretty-searchresults
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 65fc8133f0fab70627c665e1ccfc6a5d45d16fc3
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 65fc8133f0fab70627c665e1ccfc6a5d45d16fc3
│           └── chunk-001.nq.gz
├── blob
│   ├── 19910ebdd9d1010d4c69af08dabd27cd1f06541b.nq.gz
│   ├── 1ccc7d204a265357b7197f2bd768497c2388ea53.nq.gz
│   ├── 297ed8132eff49d613266833ba425bcd40b80d0d.nq.gz
│   ├── 2e4bc4bb10f1111477cc9289f4194906efb337d0.nq.gz
│   ├── 3b28fdd0d8d8a362bdea3041dfa3f6971fc73aec.nq.gz
│   ├── 4f21613ec08f57a4238ad5883ac6dcde538ba42a.nq.gz
│   ├── 547183eab8626785253a3468998d49eb99a6e2fe.nq.gz
│   ├── 5d7da1909bc351c520b3b7dbd6292108fdffd117.nq.gz
│   ├── 6190eb2565c224e2db0afc5c48c8c24e0462e2d3.nq.gz
│   ├── 6c34f77b269462dd8226e40d6d1baf00e18dc75d.nq.gz
│   ├── 82d73ca88ca3ac5de66a754c3fc694efe34a5464.nq.gz
│   ├── 90823284978546f7f374fc5b23c31561a83e374a.nq.gz
│   ├── 9c8317c4510812c42d632f2b905fc8fdd88e0c4d.nq.gz
│   ├── bbea6cacdff82fba802fe3e9d99c9f0019531564.nq.gz
│   ├── c497e54a03c5363b80fd08aafaf99f0a893bee16.nq.gz
│   ├── cf746234a79fd1b2603a547db20b86892c27b565.nq.gz
│   ├── d522d785571c438af3d98fb9d4f52e29f232c329.nq.gz
│   ├── ded9ed4cd7bb7e47d0d7dbaecca8993fe0321bd5.nq.gz
│   ├── e8565c41ab0b4c1ab601394d7085430bf373314d.nq.gz
│   ├── e939b16a0728460817bde74bee954c5c325fc917.nq.gz
│   ├── ed6e30b0db2dfad252ad7c5f34cbf23893f11802.nq.gz
│   └── f99e145bd8aed69f86a2202d7303826ae1996b27.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 65fc8133f0fab70627c665e1ccfc6a5d45d16fc3.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[sphinx-contrib/sphinx-pretty-searchresults](https://github.com/sphinx-contrib/sphinx-pretty-searchresults)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
