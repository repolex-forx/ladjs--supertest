# Repolex Knowledge Graph of ladjs/supertest

RDF knowledge graph data for [ladjs/supertest](https://github.com/ladjs/supertest), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download ladjs/supertest
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d7997513dcfb2f918e617f48ea4d56006aa0c3c3
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── d7997513dcfb2f918e617f48ea4d56006aa0c3c3.nq.gz
│   └── repolex
│       └── d7997513dcfb2f918e617f48ea4d56006aa0c3c3
│           └── chunk-001.nq.gz
├── blob
│   ├── 020b1fac6cf419811a3590a693f0a983c5f2890c.nq.gz
│   ├── 0ad1d21a1f3fbfc5888885c5b2e6d736d68a588a.nq.gz
│   ├── 1291ee7a1be25479a362706bf3ef2b3786ad76fb.nq.gz
│   ├── 1d5b890d7268ed2380abcdafcfc357d19195c236.nq.gz
│   ├── 3844a33df98bbc70fb27c679eb7c7b62d36d8a6b.nq.gz
│   ├── 52b7fe63a193ac5c065d5b92afa13860ca498201.nq.gz
│   ├── 5cd5590fa64c24ca496282fb91299270cf5da109.nq.gz
│   ├── 6492a5171064d64bfcaa325ac05576b56811cdb2.nq.gz
│   ├── 73e175f2b378097f027e2e75f7ac124b39598825.nq.gz
│   ├── 7575a39d5b50a1f6975bb0db2a1bd803d143ddfd.nq.gz
│   ├── 87acf58dd881b66a7c164e299cd80e625b3b0ac2.nq.gz
│   ├── 889dee0e371297eaba3bfb4ec1290b48f30c23e4.nq.gz
│   ├── c23a18c3a57c2f8b1746cd3033b0d8d7b29ff022.nq.gz
│   ├── c34aa79d07217e793f497d4e04968506c8a190c0.nq.gz
│   ├── c6c5ab13c9fd8e29a0c1fb9505b5bcff05e64ec3.nq.gz
│   ├── ca1368b18a060cfcbae5495f7cd888d6a770775b.nq.gz
│   ├── cafe685a112d33947d986be8cc156e0cab38068d.nq.gz
│   ├── cd42a35b93fb4c32fa28172ba3a16e9147b0b192.nq.gz
│   ├── ce7ee5261dbb8ce17a100080d9f8b2c2ea8577db.nq.gz
│   ├── d84904feae7f508c467d56837319234bcf036823.nq.gz
│   ├── e95d4c72fbd97cb9ae7e9e504e95905121a78cc7.nq.gz
│   ├── ec8f250facf40c3658e7b05f4490dfbc31aed1ad.nq.gz
│   ├── eee7159d3c5e313b93634dd9246b3ae75e530f93.nq.gz
│   └── f83008811ab1aee6242d60b8b6fcc09b93e8396c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── d7997513dcfb2f918e617f48ea4d56006aa0c3c3.nq.gz
├── filetree
│   └── d7997513dcfb2f918e617f48ea4d56006aa0c3c3.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 34 files
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

## Source repository

[ladjs/supertest](https://github.com/ladjs/supertest)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
