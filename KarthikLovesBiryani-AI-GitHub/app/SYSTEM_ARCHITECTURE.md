# System architecture

This deliverable is a single static browser application (`index.html`). The JavaScript creates deterministic synthetic reviews, orders, menu items, and supporting datasets at startup. Rendered dashboard metrics are calculated from those records.

```text
Generated synthetic records ──> local analytics ──> dashboard / exports
             │
             ├──> lexical review + SOP retrieval ──> deterministic agent response + source IDs
             └──> local tool adapter trace ──> recommendation proposal ──> owner decision + audit
```

The “integration” layer is an in-app mock adapter pattern. It is not an MCP client/server. No external APIs, accounts, or services are accessed. Browser local storage persists the demo approval and audit records.
