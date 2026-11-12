# KarthikLovesBiryani-AI

A self-contained, locally runnable restaurant intelligence demonstration for the fictional Karthik's Biryani Kitchen in Koramangala, Bengaluru. It uses only synthetic records and requires no installation, API key, backend, or network connection.

## Run it

Open `index.html` in a current desktop or mobile browser. The application and dataset generator run in the browser. Approvals and the demo audit trail are saved in that browser's local storage. Use **Demo mode → Reset demo data** to clear those decisions and restore the initial state.

## What is implemented

- Overview dashboard with metrics calculated from 240 generated reviews.
- Exact rating cohorts: 60 historical reviews average 4.3; 120 current reviews average 3.8; 60 simulated post-intervention reviews average 4.1.
- Review search, period filter, pagination, and CSV downloads for reviews, 720 fictional orders, 168 anonymised customer records, menu, packaging, costs, and interventions; JSON KPI export and Markdown SOP export.
- Deterministic in-browser agent workflow with review and document retrieval, complaint summaries, ratings calculations, source IDs, and visible tool trace.
- Searchable local knowledge documents and evidence previews.
- Simulated integration/tool adapter directory; no third-party systems or protocol-level MCP server are connected.
- Recommendation submission, owner approval/rejection, and local audit trail. Decisions do not trigger real-world operations.
- Five-act presentation mode, an owner correction scenario, and a reset action.

## Data and calculation notes

Every review is generated from fixed per-period rating distributions. The dashboard averages the stored review objects rather than displaying hard-coded rating KPIs. Repeat-order share is based on generated order flags. Post-intervention reviews are a separate synthetic cohort; their difference from current ratings is not causal evidence. The cost estimates are fictional and exclude labor, tax, platform commissions, and overhead. Do not use these records as real business results.

## Technical limits

This is a no-dependency classroom prototype, not a production service. Agent responses use deterministic retrieval and simple lexical term matching; there is no LLM, embedding model, vector database, backend, authentication, or protocol-level MCP implementation. The UI labels these limits. Browser local storage is not an authorization boundary: the approval center demonstrates a human decision workflow but does not authenticate an owner.

## Data export

Open **Customer reviews** and choose a dataset from **Download generated data…**. One file is downloaded per selection. Files are regenerated consistently on each page load; IDs and distributions remain deterministic.

## Reset

The reset control clears local approval and audit entries, removes the demo correction, and rebuilds the original generated review set. It does not contact or modify any external service.
