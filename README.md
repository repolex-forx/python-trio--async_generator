# Repolex Knowledge Graph of python-trio/async_generator

RDF knowledge graph data for [python-trio/async_generator](https://github.com/python-trio/async_generator), parsed by [repolex](https://repolex.ai).

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
lexq download python-trio/async_generator
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2c5e2e201c4dcd40b112eb3193c73f2c2b84d263
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 2c5e2e201c4dcd40b112eb3193c73f2c2b84d263.nq.gz
│   └── repolex
│       └── 2c5e2e201c4dcd40b112eb3193c73f2c2b84d263
│           └── chunk-001.nq.gz
├── blob
│   ├── 0b8742117b6e3b88e430d2ee4a094d443522848d.nq.gz
│   ├── 104c402ebf17ef55f9cdca2114f0a4449f6dd039.nq.gz
│   ├── 16961d1210b291c38ff01271e5c650680722c8a4.nq.gz
│   ├── 1f64eb2f6b6f468ff35b12fd04e1c98be67fa96c.nq.gz
│   ├── 2b4a8b1337f818e191b2f87554821aafd366e86f.nq.gz
│   ├── 2c71c9d662a8386fb39cb4c7d1bd35c67ea1275e.nq.gz
│   ├── 3f53032f69475deafd721aed577f5cb0f7ce1882.nq.gz
│   ├── 461f37f629b1a288f51ff82a63cd2fda5dca14cd.nq.gz
│   ├── 49da75e0beb39cf7431ba963c25eca34f08f08fe.nq.gz
│   ├── 4bee4cf26a5219ce23298591919caff7577e3460.nq.gz
│   ├── 651ca6af9a5a814c1d6024baaf0ca03e719052a4.nq.gz
│   ├── 67898ba6f5cffa770a3110d8c996c8203cbbdc26.nq.gz
│   ├── 6c42d450ffc26b5cf7692dd92b86e6990cdcc138.nq.gz
│   ├── 6ff5c25c5a4b77ac9cce49f44778c1585d19133f.nq.gz
│   ├── 74636639dbf3d8ff4fb40b87ba58660bf4326c13.nq.gz
│   ├── 82aef324c9ca08bc3bffeb8d5ecbe604a1256481.nq.gz
│   ├── 8425d38d482669795b7402d7e38276cecae4fd6d.nq.gz
│   ├── 90facc45794380bba9b12ae0b66d8ced7c869e1b.nq.gz
│   ├── 992e7a218a4aec4c3bdfcee0a0ab329833ef6724.nq.gz
│   ├── 9955deccd941f6c55582dcec1e96d1caf2e1980f.nq.gz
│   ├── aa6f1138950d87a7d0b2741a6ee757ed76a6faee.nq.gz
│   ├── ae9cde089a6bc055aed1cb15deda08cc5d05ece8.nq.gz
│   ├── b8bb97185926d7daed314609753173945ed4ff1a.nq.gz
│   ├── bb438dad3656a71817d57bd3363c304f26587fe4.nq.gz
│   ├── c090581f88d141b44980809e58944fe0ff1a0362.nq.gz
│   ├── cf8906089349d57ff28f739b419d87f0d0d4a03d.nq.gz
│   ├── d01e930f244d317bafea7da6789109eb1aaa0ab1.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── da6abdf2ce977fc22ed876f6b16a95a7fa4341da.nq.gz
│   ├── dff66bb6d5ddd5a0300fbde74d394f804b5ad18a.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e81a8fe8c5fe84d6d9a485c90a5ae5118f3b2e6b.nq.gz
│   └── f38c5167733eb2fd1cb677450f876788a4aa603e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 2c5e2e201c4dcd40b112eb3193c73f2c2b84d263.nq.gz
├── filetree
│   └── 2c5e2e201c4dcd40b112eb3193c73f2c2b84d263.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 43 files
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

[python-trio/async_generator](https://github.com/python-trio/async_generator)

---
*Parsed on 2026-04-09 by [repolex](https://repolex.ai)*
