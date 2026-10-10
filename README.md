# Repolex Knowledge Graph of aio-libs/aiohttp-sse

RDF knowledge graph data for [aio-libs/aiohttp-sse](https://github.com/aio-libs/aiohttp-sse), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/aiohttp-sse
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a674b62f766d16889b567fc0b685200f07cb5263
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a674b62f766d16889b567fc0b685200f07cb5263
│           └── chunk-001.nq.gz
├── blob
│   ├── 01b6c655d87738cef3b436a045a5158286fb9fdb.nq.gz
│   ├── 077a151581e1f8cfb61bf1572423d14609ce19e8.nq.gz
│   ├── 0b2f7b0655f41276d418ca8302dbaec8b7e7e829.nq.gz
│   ├── 0e3ab35b116b10f3d660760bf1e5471316d98a98.nq.gz
│   ├── 1f234b611d3a42185bf88ac3eaa6662619674ea4.nq.gz
│   ├── 2584d90dc5e9c651feb1df7249882b36eae644b4.nq.gz
│   ├── 2ce4a9f8c47ea2c6ac49f6567d9a28ba8382d349.nq.gz
│   ├── 31c9037229f9b82767ccb00b1796bf4ebaf81dc8.nq.gz
│   ├── 36979982708b367032730848375b2a457cf360b8.nq.gz
│   ├── 52770ed45289b9c5f2556f4b46bb986b5b70ff94.nq.gz
│   ├── 61766d7199a98700055cddb3d7ce4702e632a7dd.nq.gz
│   ├── 78d696335478024249c240f9e9d97eb249c559e8.nq.gz
│   ├── 83793d4d3a9c9025ac1da82a063044b334c40f05.nq.gz
│   ├── 9e318c31350c06df8da53fc0cd8bf8f7a891a730.nq.gz
│   ├── a32314e2221e9bbfd5026fa21746809d90a8ebbc.nq.gz
│   ├── b84493462928a6012d6c34f3d65f21d822ca6519.nq.gz
│   ├── b9c7f4a2a3ed1c505c0dd17438134aec29500956.nq.gz
│   ├── b9fb8a6e0f4a5ce99899eb97d872c6b90f4bb678.nq.gz
│   ├── c71ee95eaca35395a075c7eeb372cba918a25179.nq.gz
│   ├── c733433d0853c1c123ca282e36b636937ab6d45d.nq.gz
│   ├── cdb898355ecbd19dc2ac2018cc7a0afb3f110e17.nq.gz
│   ├── d9dde006c6359a6ebb95088484052c9faf0aea7c.nq.gz
│   ├── da3cb0528508d02f67a2bcdcafc08cd5811a0eb3.nq.gz
│   ├── dda99990d3ef079249273e7cd6d4c11fb794e882.nq.gz
│   ├── e24dd1f98b036e9ba4718f0ee0ac5ce0ffb5c37c.nq.gz
│   ├── e419e32dd7c66dbaeadd90ab6d6f1581e1286ffd.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f107ba3deb95ab5dda50328ea2c11432089d889d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a674b62f766d16889b567fc0b685200f07cb5263.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 36 files
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

[aio-libs/aiohttp-sse](https://github.com/aio-libs/aiohttp-sse)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
