# BeingDB

**Structured facts. Deterministic queries. AI-friendly interfaces.**

BeingDB is an open-source database for storing structured facts in Git and querying them with a small, readable declarative language.

It is designed for systems where data should stay **versioned, inspectable and deterministic**, while still being easy to use from modern AI tools.

Language models can help formulate queries, but BeingDB remains authoritative for validation, execution and results.

```text
Natural language
      ↓
BeingDB query
      ↓
validate / execute
      ↓
structured results
```

## Projects

- **[beingdb](https://github.com/BeingDB/beingdb)** — core database and query engine
- **[beingdb-wasm](https://github.com/BeingDB/beingdb-wasm)** — BeingDB running entirely in the browser
- **[beingdb-webllm](https://github.com/BeingDB/beingdb-webllm)** — local LLM + BeingDB experiments and benchmarks
- **[beingdb-mcp](https://github.com/BeingDB/beingdb-mcp)** — MCP interface for AI assistants and tools
- **[beingdb-rewind-interviews](https://github.com/BeingDB/beingdb-rewind-interviews)** — research/demo dataset

## Try it

**Browser tutorial:**  
https://beingdb.github.io/beingdb-wasm/tutorial/

**Local AI demo:**  
https://beingdb.github.io/beingdb-webllm/

> **AI as an interface, not as the database.**
