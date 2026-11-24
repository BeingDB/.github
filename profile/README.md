# BeingDB

**Build chatbots that answer from your facts, running entirely in the browser. No enterprise AI, no API keys, no server.**

A small local model in the browser understands the question; BeingDB, compiled to WebAssembly, checks the query and answers it from your facts. Every answer comes from the data, not the model's memory. Nothing leaves the page, and there is no per-query cost: publish the facts and the chatbot as a static site, for example on GitHub Pages.

```
question -> local model (WebLLM) -> BeingDB query -> BeingDB (WASM) validates and runs it -> facts -> answer
```

Your facts live in Git, versioned and reviewable like code:

```prolog
written_by(emma, jane_austen).
published_in(emma, @1815).
```

```
find Book, Year
where
  written_by(Book, jane_austen)
  published_in(Book, Year)
```

The same engine also runs as a server, and through MCP for AI assistants.

**▶ [Make your own chatbot](https://github.com/beingdb/beingdb-chatbot-template)**: click *Use this template*, add your facts, and GitHub Pages publishes it. · **[Try the demo](https://beingdb.github.io/beingdb-chatbot-template/)** (needs a WebGPU browser such as current Chrome or Edge) · **[Learn the query language](https://beingdb.github.io/beingdb-wasm/tutorial/)**

## Projects

**Start here**

- **[beingdb-chatbot-template](https://github.com/beingdb/beingdb-chatbot-template)** — make an in-browser chatbot over your own facts, published on GitHub Pages

**Core**

- **[beingdb](https://github.com/beingdb/beingdb)** — core database and query engine
- **[beingdb-wasm](https://github.com/beingdb/beingdb-wasm)** — BeingDB running entirely in the browser
- **[beingdb-mcp](https://github.com/beingdb/beingdb-mcp)** — MCP interface for AI assistants and tools

**Research example: the REWIND artists' interviews**

A larger, real dataset: facts about British and international video artists, extracted from the [REWIND](https://rewind.ac.uk/) interview archive.

- **[beingdb-rewind-interviews](https://github.com/beingdb/beingdb-rewind-interviews)** — the facts and how they were extracted ([query them in the browser](https://beingdb.github.io/beingdb-rewind-interviews/))
- **[beingdb-webllm](https://github.com/beingdb/beingdb-webllm)** — the chatbot over those facts ([try it](https://beingdb.github.io/beingdb-webllm/)), with benchmarks of how well local models write BeingDB queries
