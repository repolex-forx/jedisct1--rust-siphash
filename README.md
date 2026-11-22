# Repolex Knowledge Graph of jedisct1/rust-siphash

RDF knowledge graph data for [jedisct1/rust-siphash](https://github.com/jedisct1/rust-siphash), parsed by [repolex](https://repolex.ai).

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
rlex download jedisct1/rust-siphash
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── db8172048a1c9bdef0dcec782d965c236161af13
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── db8172048a1c9bdef0dcec782d965c236161af13.nq.gz
│   └── repolex
│       └── db8172048a1c9bdef0dcec782d965c236161af13
│           └── chunk-001.nq.gz
├── blob
│   ├── 017962a19b89de706758c2968f66e9d885f55f01.nq.gz
│   ├── 125afacdb23a50bc1f5fb3db159fb0281ff8d291.nq.gz
│   ├── 14b8ac801a8a276e3ce5c02ed8c772974873c6a8.nq.gz
│   ├── 6f973fbe147cc0cd7e12c5e39a3255417a42c40a.nq.gz
│   ├── a8f44fc5a49b82c2c1f1034a7f309bf277a51b4d.nq.gz
│   ├── b66177e36005087830f714ce95a64ded4e4d7f03.nq.gz
│   ├── c11601fecaae21cc1795e1c9105bc5b0e4340150.nq.gz
│   ├── c5bf53073f2dc1c4604db2c8409789c20b233c1a.nq.gz
│   ├── ce9fde2e9548d100f4ed996bbd1eb5de9008748b.nq.gz
│   ├── e485ab4130a7098ff3ca6c9ca86568162689a50f.nq.gz
│   ├── e5146efc36c59f241742a1d93559299a0d7f461f.nq.gz
│   └── f65e1ba0980f3eaf077c246e127990f7a350f82e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── db8172048a1c9bdef0dcec782d965c236161af13.nq.gz
├── filetree
│   └── db8172048a1c9bdef0dcec782d965c236161af13.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 22 files
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

[jedisct1/rust-siphash](https://github.com/jedisct1/rust-siphash)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
