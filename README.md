# Repolex Knowledge Graph of modelcontextprotocol/experimental-ext-triggers-events

RDF knowledge graph data for [modelcontextprotocol/experimental-ext-triggers-events](https://github.com/modelcontextprotocol/experimental-ext-triggers-events), parsed by [repolex](https://repolex.ai).

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
rlex download modelcontextprotocol/experimental-ext-triggers-events
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6682596d65eec778fe0b8b1f43b4e89d2fe2c546
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 6682596d65eec778fe0b8b1f43b4e89d2fe2c546
│           └── chunk-001.nq.gz
├── blob
│   ├── 5c74e84974b913e5ddc7fde14e9eb6ddb4aae81b.nq.gz
│   ├── 631e6355f77d0070283ecf97e081e42d35beb76e.nq.gz
│   ├── 97a4db96d7352fce0aa27eebd24438a0dc078fc5.nq.gz
│   ├── a8cf76ccde0ec0eacf8b8ea686f53cbff50f0208.nq.gz
│   ├── d1b78ec21cf27924d738797d91434b5590e8ab51.nq.gz
│   └── d6b130cf3de22c031b818e6f8d8ec358d2ad9987.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6682596d65eec778fe0b8b1f43b4e89d2fe2c546.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 14 files
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

[modelcontextprotocol/experimental-ext-triggers-events](https://github.com/modelcontextprotocol/experimental-ext-triggers-events)

---
*Parsed on 2026-10-09 by [repolex](https://repolex.ai)*
