# Retrieval and evidence notes

Five small, synthetic business documents are bundled in the page. At runtime, a query is tokenized and matched against document and review text. Matching review records are ranked by the number of overlapping query terms. The agent can display review IDs and document IDs with excerpts.

This is a transparent lexical retrieval demonstration. It does not use embeddings, a vector store, semantic search, an external model, or generated claims from an LLM. A missing match is reported as missing evidence. Matching does not prove a cause.
