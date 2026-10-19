# Repolex Knowledge Graph of warner/python-ed25519

RDF knowledge graph data for [warner/python-ed25519](https://github.com/warner/python-ed25519), parsed by [repolex](https://repolex.ai).

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
rlex download warner/python-ed25519
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d57b8f2c7edffff3419d58443ccc29a4fa399a71
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d57b8f2c7edffff3419d58443ccc29a4fa399a71
│           └── chunk-001.nq.gz
├── blob
│   ├── 04940c9105c6e588b9bc1b794513608638eee497.nq.gz
│   ├── 07b33ecb6d1fdbede2bcac268b061b8d4b991daa.nq.gz
│   ├── 0b486e5360918ae925e0a58b20ff7c94cd434130.nq.gz
│   ├── 0ea7f15ad2f027871e61cc6706aa738f22e96fa6.nq.gz
│   ├── 18519d246939564d11e2dacdbaabf5b09664c0d3.nq.gz
│   ├── 1d0c9889605bb98f60c7e2864ff95e512c45077d.nq.gz
│   ├── 21020d7b57083e8d7d26bf9adf847c6597e58fe1.nq.gz
│   ├── 23c94a4eb13e4072b7ff689db03df283dba63e92.nq.gz
│   ├── 279f1c9d7477fb9e61f3e32e24f509849c8ed254.nq.gz
│   ├── 2803174830a8a5546adc2aef28f4d5ebb91b4de5.nq.gz
│   ├── 35620f2971ebc17f5c662ef93a93fdee320469d5.nq.gz
│   ├── 37376b15de15141e0f0cf4dc9833846cd6a3757b.nq.gz
│   ├── 4b10ca795a3d70f1ebd94563ee705551e1c8a2a1.nq.gz
│   ├── 4c304307534cd323ad18dbaec4b6b163be01717f.nq.gz
│   ├── 4d620e5dbf146411f002c18d9a96757602766dbd.nq.gz
│   ├── 69b0d3ba37df7e1f3ddfd6d54d0ba1db8a71e41d.nq.gz
│   ├── 69e5b3080cc1ce3ee120fec570897371e00e2b4d.nq.gz
│   ├── 7ad9cd860cc7976aa666702c0d3b2143da93400d.nq.gz
│   ├── 7f8613b8d830f38239a0b43b7adfeb67784b7a16.nq.gz
│   ├── 8d9f63d43f3e1809bbd9112148c0ffdd0b10013e.nq.gz
│   ├── 8dea618fbdb6031f24a2e2be8408725df8ab76e5.nq.gz
│   ├── 925b89457ad712b43caabeda6b36fdfa1750d6d9.nq.gz
│   ├── 95a092582d2df810b7ebf6eecb0b888f94ed4106.nq.gz
│   ├── a04186b60704eb5be889b3876739a8e682112c13.nq.gz
│   ├── a40b040a0304ab3c519798965bc3befca2eac2cc.nq.gz
│   ├── ad265c7a3fbb1cc4e6908ea15fb24f69537f6b8d.nq.gz
│   ├── afed20821cf5839b3dc89f466a2767e5d7ab9c8a.nq.gz
│   ├── b96764cf72daa39148cdd8ca3e4411d4f074b749.nq.gz
│   ├── bb6d92a7a644a60932a5a89466ab4a05213d710a.nq.gz
│   ├── bbab0e6fe5d9254c8344451f13a9d572bb8c358a.nq.gz
│   ├── c010f63e3ead851cb35e4d4cc8bc958b8be76ab0.nq.gz
│   ├── c8dbf0d35187a9fb355ec161f2342d5d3897dd9f.nq.gz
│   ├── cae135e6e200736258227d2cdae8fc0f5d549836.nq.gz
│   ├── ccfce2dbd2e0502a083681c62c05d53a7395dfb3.nq.gz
│   ├── d2ef2c13060fe84ad313a19f6f459227254e625b.nq.gz
│   ├── e9442dfecdb0afe0c2a53e687f065b4065bfc3a3.nq.gz
│   ├── ef338e867297584c8c76679650969d5f536fcdce.nq.gz
│   ├── f2f292505cc4ef5a1b9b128046d98f8aa3ba7bc7.nq.gz
│   └── fbfe1f5447252ae368b9f28d25edff7eb59c65ce.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d57b8f2c7edffff3419d58443ccc29a4fa399a71.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 47 files
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

[warner/python-ed25519](https://github.com/warner/python-ed25519)

---
*Parsed on 2026-10-19 by [repolex](https://repolex.ai)*
