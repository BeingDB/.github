# BeingDB

**AI as an interface, not as the database.**

LLMs are great at understanding questions but unreliable as a source of truth. BeingDB keeps your facts in Git, versioned and reviewable like code, and answers queries deterministically. The model helps phrase the query; BeingDB validates it, runs it and returns the facts.

```prolog
created(tina_keane, shadow_of_a_journey).
year_created(shadow_of_a_journey, @1979).
```

```
find Artist, Work, Y
where
  created(Artist, Work)
  year_created(Work, Y)
  Y >= 1970
```

Runs on a server or entirely in the browser via WebAssembly. No account needed, and queries never leave the page.

**▶ [Try it in your browser](https://beingdb.github.io/beingdb-wasm/tutorial/)** (no install) · **[Local AI demo](https://beingdb.github.io/beingdb-webllm/)**

## Projects

- **[beingdb](https://github.com/BeingDB/beingdb)** — core database and query engine
- **[beingdb-wasm](https://github.com/BeingDB/beingdb-wasm)** — BeingDB running entirely in the browser
- **[beingdb-webllm](https://github.com/BeingDB/beingdb-webllm)** — local LLM + BeingDB experiments and benchmarks
- **[beingdb-mcp](https://github.com/BeingDB/beingdb-mcp)** — MCP interface for AI assistants and tools
- **[beingdb-rewind-interviews](https://github.com/BeingDB/beingdb-rewind-interviews)** — research/demo dataset ([live site](https://beingdb.github.io/beingdb-rewind-interviews/))
