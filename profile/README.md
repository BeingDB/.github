# BeingDB

**Build chatbots that answer from your facts, running entirely in the browser. No enterprise AI, no API keys, no server.**

A small local model in the browser understands the question; BeingDB, compiled to WebAssembly, checks the query and answers it from your facts. Every answer comes from the data, not the model's memory. Nothing leaves the page, and there is no per-query cost: publish the facts and the chatbot as a static site, for example on GitHub Pages.

```
question -> local model (WebLLM) -> BeingDB query -> BeingDB (WASM) validates and runs it -> facts -> answer
```

Your facts live in Git, versioned and reviewable like code:

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

The same engine also runs as a server, and through MCP for AI assistants.

**▶ [Try the in-browser chatbot](https://beingdb.github.io/beingdb-webllm/)** (no install; needs a WebGPU browser such as current Chrome or Edge) · **[Learn the query language](https://beingdb.github.io/beingdb-wasm/tutorial/)**

## Projects

- **[beingdb](https://github.com/BeingDB/beingdb)** — core database and query engine
- **[beingdb-wasm](https://github.com/BeingDB/beingdb-wasm)** — BeingDB running entirely in the browser
- **[beingdb-webllm](https://github.com/BeingDB/beingdb-webllm)** — in-browser chatbot: local LLM + BeingDB, with benchmarks
- **[beingdb-mcp](https://github.com/BeingDB/beingdb-mcp)** — MCP interface for AI assistants and tools
- **[beingdb-rewind-interviews](https://github.com/BeingDB/beingdb-rewind-interviews)** — research/demo dataset ([live site](https://beingdb.github.io/beingdb-rewind-interviews/))
