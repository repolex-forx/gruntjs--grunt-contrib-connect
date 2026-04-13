# Repolex Knowledge Graph of gruntjs/grunt-contrib-connect

RDF knowledge graph data for [gruntjs/grunt-contrib-connect](https://github.com/gruntjs/grunt-contrib-connect), parsed by [repolex](https://repolex.ai).

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
lexq download gruntjs/grunt-contrib-connect
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9d9b2951cfc62945eb9b25e18e3e23bc870a6af6
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 9d9b2951cfc62945eb9b25e18e3e23bc870a6af6.nq.gz
│   └── repolex
│       └── 9d9b2951cfc62945eb9b25e18e3e23bc870a6af6
│           └── chunk-001.nq.gz
├── blob
│   ├── 095ba841026ac4a90e57e9bc8b38f655349dd574.nq.gz
│   ├── 0cf593db311672425ab6ffdd47a9854b7ee36017.nq.gz
│   ├── 1073d15045c5cc10546bb5c91cfdeb84cc460772.nq.gz
│   ├── 13e7e2c2fbf36585e10381074af0f7e70edb11d1.nq.gz
│   ├── 1f63955a4532ae639a0795fb1b9cb27a0b9110eb.nq.gz
│   ├── 205021e49dd1f7342400b8e1254cc4e310fcc4a1.nq.gz
│   ├── 4812751a94a13fdd3cfd1041d5aff21a504d90e8.nq.gz
│   ├── 4825966ac3ab4197c491216208b1459c74053386.nq.gz
│   ├── 53bc33dc989be65c2d85d44e74cc20b5bf642c79.nq.gz
│   ├── 5d126348471c348decba17143ce128130c9f4104.nq.gz
│   ├── 70c379b63ffa0795fdbfbc128e5a2818397b7ef8.nq.gz
│   ├── 722fcc4cdd8a089acc7adb2e43744ade9ef0cd36.nq.gz
│   ├── 7a20929f138f64312ef0b3467cd88e94c989eee0.nq.gz
│   ├── 8547a5b042a638a7909e17aec309736f67fc9bc8.nq.gz
│   ├── 895c25eb69cada821f3d629e08eb6b24ed319816.nq.gz
│   ├── 8adb9a5adc2775120204d4f8cfe14e4a92e72d51.nq.gz
│   ├── 8fbdfc1e69e1e0cc5e1ce33a84f2def0d0ef1eb7.nq.gz
│   ├── 8ff46a626b719e76c1115325667a1c019bc81a7a.nq.gz
│   ├── 93257894f01eaaa3c91036c4efe9b6c343e1d21b.nq.gz
│   ├── 9eb0571374193d826436294102180a81608de501.nq.gz
│   ├── a7e142648f3940766dd820ec888471f5688ea88d.nq.gz
│   ├── d02c7237fe87d4fea79a8d8e72f11845dc172fbd.nq.gz
│   ├── e5a10ccc3d1f4f4e576be0dcc0c9b8e692abf3cd.nq.gz
│   ├── e70f16d7dbcc7d5985eb01f9a485480e1ce187c9.nq.gz
│   ├── e7449c5febd42a6310fa43cdb12db13717166930.nq.gz
│   ├── f942be1175c4ed0eda37327d276c67c8b75e2fac.nq.gz
│   ├── fa88e60a10e1ed31315dfd9761fee0fb7d19d449.nq.gz
│   └── ff888ee38ef45e5cedc0a5d1aae095eff93e9704.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 9d9b2951cfc62945eb9b25e18e3e23bc870a6af6.nq.gz
├── filetree
│   └── 9d9b2951cfc62945eb9b25e18e3e23bc870a6af6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 38 files
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

[gruntjs/grunt-contrib-connect](https://github.com/gruntjs/grunt-contrib-connect)

---
*Parsed on 2026-04-13 by [repolex](https://repolex.ai)*
