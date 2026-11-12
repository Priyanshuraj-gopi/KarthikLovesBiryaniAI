# Agent workflow

The in-browser agent takes a question, retrieves matching current-period reviews and synthetic business documents, logs simulated tool calls, and composes a deterministic response from those records. Rating and repeat-order questions are answered from calculated dataset metrics. Responses display retrieved review and document identifiers where applicable.

The workflow is intentionally inspectable and bounded. It is not a general-purpose LLM agent and does not infer unsupported causal explanations. Business changes are proposals; purchase, recipe, price, supplier, operating procedure, or customer communication changes must remain subject to an owner decision.
