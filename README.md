# Repolex Knowledge Graph of scikit-hep/histoprint

RDF knowledge graph data for [scikit-hep/histoprint](https://github.com/scikit-hep/histoprint), parsed by [repolex](https://repolex.ai).

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
rlex download scikit-hep/histoprint
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1539fb05c56f2589cac91f1aca2e95f9628faf00
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1539fb05c56f2589cac91f1aca2e95f9628faf00
│           └── chunk-001.nq.gz
├── blob
│   ├── 08b9a40ada74390f525813c460710e54d04956d7.nq.gz
│   ├── 15eda5394de5bdfa7e8d02221885311ac6313bc5.nq.gz
│   ├── 1ef107f593506d852c6d34bc985eed367963ba61.nq.gz
│   ├── 2e5b8b97dbb00c8dc9b4feb17dc7b73b0402cdfa.nq.gz
│   ├── 48fb9f77893f44920ddacfa19822cb89b95e736c.nq.gz
│   ├── 4d0d8dbba4555f2d18ff00e7560e62b39f2053ee.nq.gz
│   ├── 5304ead7c2fc221a00cbdbe8329ee2fdcff42f1f.nq.gz
│   ├── 534f0f83a376a4831db00ca3733fe1f8cc05fb60.nq.gz
│   ├── 5d42de4495b0f86975b620fe85a2c32c948dc070.nq.gz
│   ├── 62c3b35f47aa388c18b9fa8f0a1f6b2f8a112e16.nq.gz
│   ├── 70bffe414de3558e4376674e76b9dd1cd1a260ee.nq.gz
│   ├── 7378fd4869cd94898b3954a2805cb332c889932f.nq.gz
│   ├── 74f459ebb0552854e030f7c0b02f372ab2ffc3e9.nq.gz
│   ├── 8b13673c14657c63f5a23c7b514f9fca0725174f.nq.gz
│   ├── 982b3196244e90966927e7fd4f7add2c521f8c2c.nq.gz
│   ├── a26c7c8b9452b48ffbdfc6b48e484abcd0ea2e13.nq.gz
│   ├── a6578a30e85b77966d473b65665968c3d0083bdc.nq.gz
│   ├── ab3082407020ca47dee598a00dfe8aa03693665e.nq.gz
│   ├── ab727420b453218c906ac98d33e8ac9de72173f5.nq.gz
│   ├── b0396e4c833cf1e0044945adb2955bf5ea9a872b.nq.gz
│   ├── bb543e57d65f2f4672e2276dc371820664821432.nq.gz
│   ├── c2ee2cab489bc0c99d6e2e2357c3c629e45287f4.nq.gz
│   ├── d26d1a9a9556c6d4488875012e4d9576be781b80.nq.gz
│   ├── e0e42f5d12ca28462879621bda6127f96c0095d6.nq.gz
│   ├── ece066cc80212e96c1f26b3467f517ff36e362c2.nq.gz
│   ├── f4c749af07ac8ff936c62a839572efa73426efc3.nq.gz
│   ├── fa8705509e36725265a457e8ffa33d4637056721.nq.gz
│   ├── fe66f4d0c24fef41488d54b8d1efd490524ee6f4.nq.gz
│   └── ff88315ffc7dc921830dfd04231dc4205c5f440a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1539fb05c56f2589cac91f1aca2e95f9628faf00.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 37 files
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

[scikit-hep/histoprint](https://github.com/scikit-hep/histoprint)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
