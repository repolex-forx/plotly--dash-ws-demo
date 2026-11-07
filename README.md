# Repolex Knowledge Graph of plotly/dash-ws-demo

RDF knowledge graph data for [plotly/dash-ws-demo](https://github.com/plotly/dash-ws-demo), parsed by [repolex](https://repolex.ai).

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
rlex download plotly/dash-ws-demo
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 8c0f0352eb4c31f9c145f6a712fce9bd61a1ca21
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 8c0f0352eb4c31f9c145f6a712fce9bd61a1ca21
│           └── chunk-001.nq.gz
├── blob
│   ├── 0589540441491e7187713d65f6eccd5336b69694.nq.gz
│   ├── 09dce390b45f89427ca200543fcb821a8c96d120.nq.gz
│   ├── 0fdbdfb571def65d0bbd3cc76098a8af1b7e2ffa.nq.gz
│   ├── 2542d8dbdf7901afba8974de47b04a4c66ea505f.nq.gz
│   ├── 2dc0c6eb6e073e93176ad9ab3b39e3e71085adf0.nq.gz
│   ├── 2fe7050b4ac6f4f5994e127d13844dd37dac930a.nq.gz
│   ├── 391cab769b0b7ba189c8b494ede2db2400cf3ad3.nq.gz
│   ├── 463a987dcd5fcad6fcdc0a8a0ff35e4e44209a88.nq.gz
│   ├── 49c0b5e9a441abd2dd160d4f84b18c88fa479474.nq.gz
│   ├── 4d9948dc2d43f3fd1b29b4cf0c712d5f41445b82.nq.gz
│   ├── 5cbe850b53942c903ffdab8178d0eeebd5aa11bc.nq.gz
│   ├── 70acf3ea0cd6be96e9d7421bcb4252eef65546ba.nq.gz
│   ├── 7843df423e5b4bf261c8e0b3658239a380298cfe.nq.gz
│   ├── 80bb0d2788da8a8a537defeaf919c2a0d1a5990e.nq.gz
│   ├── 859b7e0bb98dfde2bc80b9536879b118f796995d.nq.gz
│   ├── 870cf943b7507a5ca480b1c277f02aedc418c9c5.nq.gz
│   ├── 926d645c2bc643a0a8ef93c2df586d2cc53d6b71.nq.gz
│   ├── a1f47ad630881aeffd9a22254e14c702799a33f9.nq.gz
│   ├── a9a83c7ea6920d81d26dd465fa6220407f58263f.nq.gz
│   ├── b9e4bb9a0330fbd7b86d01026f68639f7cc39e83.nq.gz
│   ├── bdda5be250eaa66c1b94350389710a16dcb11547.nq.gz
│   ├── e288618f281878165186654c1c0e318126a288c3.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f9033fc85f022431748f3afb18d290ff6c89c31a.nq.gz
│   └── ff6a65d2ba7a415604f1eea34d317fee3ff49d02.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 8c0f0352eb4c31f9c145f6a712fce9bd61a1ca21.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
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

[plotly/dash-ws-demo](https://github.com/plotly/dash-ws-demo)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
