# Repolex Knowledge Graph of executablebooks/mdurl

RDF knowledge graph data for [executablebooks/mdurl](https://github.com/executablebooks/mdurl), parsed by [repolex](https://repolex.ai).

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
rlex download executablebooks/mdurl
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 524d2edbbcb8bb48301ba716c7482827bcabb281
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 524d2edbbcb8bb48301ba716c7482827bcabb281
│           └── chunk-001.nq.gz
├── blob
│   ├── 058dbaaf89e041ad609d6918999c73359e65da0b.nq.gz
│   ├── 0d3752914b1cd192786d1b28d0c77785bbd0f311.nq.gz
│   ├── 18bffe10c25d3a22f65028cb051da12bac8186fb.nq.gz
│   ├── 22309e6e399de7d912da1d609b1faab52ff32942.nq.gz
│   ├── 22ca7cb81a87ba52b40ae12d5a1170ee62774168.nq.gz
│   ├── 29431ec03acb2c9c4704cc104ca2f7e25aa1c1b0.nq.gz
│   ├── 2a920c59d8abdd485a774087915986448495fd7c.nq.gz
│   ├── 5fa8d0afd49eaafb78fc415684590cb8e7f3a87d.nq.gz
│   ├── 6f055500b20176c5818ede4885ac80b272f62ec8.nq.gz
│   ├── 7632ecf77545c5e5501cb3fc5719df0761104ca2.nq.gz
│   ├── 80624d0b57a077ec274f442f63249bb1dc3bf6f7.nq.gz
│   ├── 83d9b133810ec439f3c1e98d7d108bdb2df2859a.nq.gz
│   ├── 8d6474878264905b29424bcbaecad2d6c80f835c.nq.gz
│   ├── a774331ce32c130a4724241dc5c5ebc945574e53.nq.gz
│   ├── aa4ae44648e67a048f0b20280d7cc7a4903f5006.nq.gz
│   ├── b2ca23c6a581c2190076d9c127b533fa92117ebe.nq.gz
│   ├── be3926598466efdad41f7340f516277b7a814772.nq.gz
│   ├── c6dae889c1686c9da052e004c12ec41de6b42ff6.nq.gz
│   ├── c9457babe0d8fa05542ae5661f81dd2717d26962.nq.gz
│   ├── e0e969025cb2fb353b1eef3f7d75ed71e0859073.nq.gz
│   ├── e5cf0ac12dbddd002cff30f72f81e86baa5ce0a7.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f8e4e03cbe98a4ef581e225cb3aa72bc71c5e6df.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 524d2edbbcb8bb48301ba716c7482827bcabb281.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[executablebooks/mdurl](https://github.com/executablebooks/mdurl)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
