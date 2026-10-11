# Repolex Knowledge Graph of pytest-dev/pytest-faulthandler

RDF knowledge graph data for [pytest-dev/pytest-faulthandler](https://github.com/pytest-dev/pytest-faulthandler), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-faulthandler
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 11cfc20668db299e5b4002b702c441867c41f3d4
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 11cfc20668db299e5b4002b702c441867c41f3d4
│           └── chunk-001.nq.gz
├── blob
│   ├── 05aaca3f1a3c2fdf08a6ae5f3d779ac5042553a5.nq.gz
│   ├── 1aba38f67a2211cf5b09466d7b411206cb7223bf.nq.gz
│   ├── 2a0b9a100f127aba5369b9ba31f91ba4143ba8df.nq.gz
│   ├── 38badca82a210822bcbe02426afe503e9cae474e.nq.gz
│   ├── 3c6e79cf31da1c0433d2fa666bf50b53f6359f26.nq.gz
│   ├── a8e76db10f1a45420eeb3767d00397b8a575691a.nq.gz
│   ├── cdf47f51821c5aa704ec7e39d759f3a6b8ec0538.nq.gz
│   └── f6031169adbdc51bdaa72228467327de822c3b16.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 11cfc20668db299e5b4002b702c441867c41f3d4.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 16 files
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

[pytest-dev/pytest-faulthandler](https://github.com/pytest-dev/pytest-faulthandler)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
