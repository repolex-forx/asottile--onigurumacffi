# Repolex Knowledge Graph of asottile/onigurumacffi

RDF knowledge graph data for [asottile/onigurumacffi](https://github.com/asottile/onigurumacffi), parsed by [repolex](https://repolex.ai).

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
rlex download asottile/onigurumacffi
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 601c9b1b560e1907f61912e2f4eda1e835a5c95b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 601c9b1b560e1907f61912e2f4eda1e835a5c95b
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c5a37eb0adeb312718e533d0a4fbcbea6880056.nq.gz
│   ├── 2b7f71d5e6d23b73f507ecc520bcff641c5c123a.nq.gz
│   ├── 43d6447bc04960e79eb2658cd0022591cd274810.nq.gz
│   ├── 5411a5a563371451e7aebc85e90b7136f6eaf858.nq.gz
│   ├── 5c33625ee9bb41388c4511effe46317efe33cd0f.nq.gz
│   ├── 705f435f5081677d9c70fbf860964157fc41f15d.nq.gz
│   ├── 71a94918ea3c5780e27ec29ef8c6f5e8e9bc5ed6.nq.gz
│   ├── 9614f6b6e4ef49cb5001330c31617e14abcf29c8.nq.gz
│   ├── 9844cbc04909ce1852c4841c5af1c01514e88bfe.nq.gz
│   ├── 9a2fd90bd15492029a959ac5d2686e4b4e86ae5b.nq.gz
│   ├── a907cb0f7097ec87c89775d23ec4401436c59817.nq.gz
│   ├── ae935282359ec52dbd09b7f6b88b00ba55b296a5.nq.gz
│   ├── b0ac8453e0196589accc06ac3b295400c8db8e40.nq.gz
│   ├── b1447c3015af9511f2dee402ca4b5ad62adf5dce.nq.gz
│   ├── b6c2693071afdfc05b396e4c087145783ad3d0d7.nq.gz
│   ├── cb0ee7117dd14286840dc8d4719db39e061e9b13.nq.gz
│   ├── ce4e06e1c37871b4cc2ad81f45fccd512bca3b43.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 601c9b1b560e1907f61912e2f4eda1e835a5c95b.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 26 files
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

[asottile/onigurumacffi](https://github.com/asottile/onigurumacffi)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
