# Repolex Knowledge Graph of UKPLab/clpsych2025-questmf

RDF knowledge graph data for [UKPLab/clpsych2025-questmf](https://github.com/UKPLab/clpsych2025-questmf), parsed by [repolex](https://repolex.ai).

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
rlex download UKPLab/clpsych2025-questmf
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3776a2bb84927b2613abf5686322b63957158c68
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3776a2bb84927b2613abf5686322b63957158c68
│           └── chunk-001.nq.gz
├── blob
│   ├── 0100bcfdd73ab5ae8dbca280bae7a8641fe23743.nq.gz
│   ├── 02e49678493a8c6ffe43c5e48cd4851d3b580db1.nq.gz
│   ├── 1081fc99a80a4217709ced76ed44a71514985cab.nq.gz
│   ├── 12097738598894797fe04729ed74a725ce270d62.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 45fcfd3030bc76219c65fc6a3c19f108fa00ad55.nq.gz
│   ├── 4d9d30b46a1ef0248ec2e3e5f3678592b9875bc8.nq.gz
│   ├── 5298a8c0932be647ab2b19d79c766026bec1cab8.nq.gz
│   ├── 5c066c14b5c333cf16aac4207cfc75afb5d03836.nq.gz
│   ├── 64b0dc8f3f53e00ef7e67f741ea69f955e896d9f.nq.gz
│   ├── 6618160ba7a9500dfafc3744474d018c543394dd.nq.gz
│   ├── 6c321722701b486111502d2fc7872ace813fb051.nq.gz
│   ├── 705e36073282949adf3988bf8cde20578b5e0fef.nq.gz
│   ├── 7fa4784b442708873a7291c21e23a977fe2bfb01.nq.gz
│   ├── 88aeb27c4c838c354c57971e36325827daa92a64.nq.gz
│   ├── 8d7cde4cc408252b0ed0c35a158616360b9103f7.nq.gz
│   ├── 944dd545a95627bc4a15b46d2dc059079364a576.nq.gz
│   ├── 94a0ec8b1b1e4226fa0f4bd9e853902fff7f6769.nq.gz
│   ├── 97509b85f150e855f58d34cf88877013811f0923.nq.gz
│   ├── a0e36c5f477ee2b02eb80094866c343ca555a960.nq.gz
│   ├── a40f5facae5e9c3f3e45627fb066c96d6248243c.nq.gz
│   ├── b6b0a8df29975576559063114e767c99d320f515.nq.gz
│   ├── b833f5c848d559c4a8f3d846f6eb53c9d922a99e.nq.gz
│   ├── c1ed1f071ed1a666a79b9005dea365d7e64050e2.nq.gz
│   ├── cd54f79b758a8ba946b069789cdc295b506dc771.nq.gz
│   └── e1ce915e8024f66b9d402d7ffedf276a44b86f49.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3776a2bb84927b2613abf5686322b63957158c68.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 33 files
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

[UKPLab/clpsych2025-questmf](https://github.com/UKPLab/clpsych2025-questmf)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
