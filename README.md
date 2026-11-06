# Repolex Knowledge Graph of chrisjsewell/markdown-it-pyrs

RDF knowledge graph data for [chrisjsewell/markdown-it-pyrs](https://github.com/chrisjsewell/markdown-it-pyrs), parsed by [repolex](https://repolex.ai).

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
rlex download chrisjsewell/markdown-it-pyrs
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 86cf6f4c87bdbc7eac9cf03c0095a48c10a9f597
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 86cf6f4c87bdbc7eac9cf03c0095a48c10a9f597
│           └── chunk-001.nq.gz
├── blob
│   ├── 0d274e7b595f379888ca854a5548e28fff61f771.nq.gz
│   ├── 23825e5d2191888d2b3958370e1e86e017e6cce1.nq.gz
│   ├── 24cfb2806e4067557a30c4e55ed1a933d07a128f.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 2917ee8f9076fbf418c709a9e892e0cbc1799f0c.nq.gz
│   ├── 2da5b5493db84a31ed88d58cd94bed2bb76e6a8b.nq.gz
│   ├── 2e592836b37f9882f6fb741446abd88706f77da2.nq.gz
│   ├── 30421fa88992dbf73b5fe2b9a442ccb1329e3371.nq.gz
│   ├── 31a51a727ca8d42d20fe68a4245726a38a352cbb.nq.gz
│   ├── 39d1eab16faa85b6f6070649655b0e6191f473f1.nq.gz
│   ├── 47aadc729e50fb9393b1857c977aa10066c6c7ed.nq.gz
│   ├── 4ff12c9f5e270f4286a5ecc8c97dd09a20284575.nq.gz
│   ├── 5f49ccfa35e0bf0cef581dc67874c82cdc1a3938.nq.gz
│   ├── 691116629f9ed62aec90f9a56064691b61a4db43.nq.gz
│   ├── 6c9e1ad6bc0fd11a35354d8974fee0ba4fed3345.nq.gz
│   ├── 7d7062662aa8e9359471dad41a853461600ab70b.nq.gz
│   ├── 81c6cb195a32c4927e8ba1840c70559e19ed1afa.nq.gz
│   ├── 849714dce8d89d52b66774b54ea3adac3acc075a.nq.gz
│   ├── 8ed314e2285a8916bf9152037bf0689c3958272f.nq.gz
│   ├── 901a268c0e9deb1902c6b1f33e64658f54028143.nq.gz
│   ├── 92410fec704eddece91d327edf5af048191f61ff.nq.gz
│   ├── 9567830fedd06507921623b26a9010eeefa048c2.nq.gz
│   ├── ac06ce0a9d7dd34c1ca5634c14aee48acf3b114d.nq.gz
│   ├── b2b0139661106a6ceea78c8bbc2ab85b44d81daa.nq.gz
│   ├── b64379d2aacfdd026f4af18473f411835dc7ae5d.nq.gz
│   ├── b6c45820698e453b2bf74d63612273e50afc41fc.nq.gz
│   ├── bd7561a22cc2f3d309a49f8ca5605b6534ca6fc8.nq.gz
│   ├── be430d42f9466ac0dec958fdb763336ac77cfd8f.nq.gz
│   ├── ca15b6ff00c687f7a794898d0052c0ba3653ee7d.nq.gz
│   ├── cf83708beeebd42eb593aecc35261e6cc59ef2bb.nq.gz
│   ├── d193f648317d60c18effd266233d7f1cbc1ef7c0.nq.gz
│   ├── d6b189ccf9945df860ad2c94d2fc2b583b07d138.nq.gz
│   ├── dfe778a0b1807efd66985d55878d7dc480def919.nq.gz
│   ├── e49f4d987272c05372fd655a012323b2731cbc6b.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f19ce513d6e4a7ee8c5831955fb68dd7bef3643b.nq.gz
│   ├── f70b7ddaa33abbe2ccd3d5aafc7cb5844dffc8cb.nq.gz
│   └── faf01b17dfc762cbe4f0a78b969b9841bca10ece.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 86cf6f4c87bdbc7eac9cf03c0095a48c10a9f597.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 46 files
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

[chrisjsewell/markdown-it-pyrs](https://github.com/chrisjsewell/markdown-it-pyrs)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
