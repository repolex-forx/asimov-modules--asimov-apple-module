# Repolex Knowledge Graph of asimov-modules/asimov-apple-module

RDF knowledge graph data for [asimov-modules/asimov-apple-module](https://github.com/asimov-modules/asimov-apple-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-apple-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0ab8888d3b30f68177ca5a7a47dff34e3bfeb41f
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 0ab8888d3b30f68177ca5a7a47dff34e3bfeb41f.nq.gz
│   └── repolex
│       └── 0ab8888d3b30f68177ca5a7a47dff34e3bfeb41f
│           └── chunk-001.nq.gz
├── blob
│   ├── 0f9313d63eaddd339a813841e540ed99130ca574.nq.gz
│   ├── 21bf3a4b25c8874a1673cfafa602d027519a23dd.nq.gz
│   ├── 2391f73aa051d3804285ce744f2e9a1c7e08993d.nq.gz
│   ├── 2756b58bec9edb2c82f87d400b36f26639d5601b.nq.gz
│   ├── 2b0c788e2596d934456a7ce78cc4e7f3fe40e217.nq.gz
│   ├── 5f5cf896c81688e4360b37f1bcda92f7bc6f7423.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 775b37f2025b0b0c44365b5ed0671d9f24131855.nq.gz
│   ├── 8acdd82b765e8e0b8cd8787f7f18c7fe2ec52493.nq.gz
│   ├── 9cb41bbd756a6a8a8b5eece06343701a4a063c6b.nq.gz
│   ├── aae8c665b2ea862d8c80e87294a9323592fe30b7.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   ├── f973f5cacf16b59ba4c930de206273d58d533b47.nq.gz
│   ├── f99b3913a34e5e1ab42c7e031d51d59e45ffc649.nq.gz
│   └── ffb0a428d9ac743562cb27dcd367c66d17ab5ac1.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 0ab8888d3b30f68177ca5a7a47dff34e3bfeb41f.nq.gz
├── filetree
│   └── 0ab8888d3b30f68177ca5a7a47dff34e3bfeb41f.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 27 files
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

[asimov-modules/asimov-apple-module](https://github.com/asimov-modules/asimov-apple-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
