# KarthikLovesBiryani-AI

Restaurant feedback intelligence demo and TLM AI Studio Cinema project

KarthikLovesBiryani-AI is a local demonstration of how a restaurant team could turn customer feedback into a traceable investigation and a proposed operational improvement. The project includes a browser-based dashboard and deterministic agent demo, synthetic restaurant datasets generated on demand, an approval workflow, and a five-act presentation video.

> **Fictional project:** Karthik's Biryani Kitchen is an invented cloud kitchen in Koramangala, Bengaluru. All reviews, customers, orders, costs, ratings, interventions, and performance results in this repository are synthetic examples. They do not describe an operating business or actual customer experience.

## Contents

| Path | Purpose |
|---|---|
| `app/index.html` | Self-contained dashboard and local agent demo |
| `app/*.md` | Architecture, data, workflow, safety, business impact, and demo documentation |
| `film/KarthikLovesBiryani_AI_Studio_Film.mp4` | Final 4:45 film following the supplied TLM worksheet timing |
| `film/KarthikLovesBiryani_AI_Studio_Film.pptx` | Editable PowerPoint source for the film |
| `film/Narration_and_Presentation_Script.md` | Film timing, narrative, and Q&A defence notes |

## Run the application

No package installation, API key, server, or network access is required.

1. Download or clone this repository.
2. Open `app/index.html` in a current browser.
3. Navigate with the left sidebar. Start with **Overview**, then try **AI Agent** or **Demo mode**.

The application stores approval decisions and demo audit entries in the browser's local storage. Use **Demo mode → Reset demo data** to clear those entries and restore the initial state.

## What the demo does

- Shows rating, complaint, review, dish, and illustrative repeat-order metrics calculated from generated records.
- Searches reviews by period, dish, text, and complaint category; filtered review records can be exported.
- Provides a deterministic agent workflow that retrieves matching review and operating-document evidence, calculates rating comparisons, and displays source IDs and a simulated tool trace.
- Offers a small local knowledge base with review and document search.
- Shows local simulated adapters for review, order, menu/cost, inventory, reporting, and approval workflows.
- Lets a presenter submit a proposal and record an owner approval or rejection in a local audit trail.
- Guides the presenter through the five required film acts, including a deliberate misclassification and owner correction.
- Exports generated CSV datasets, a business-metrics JSON file, and SOP text from the Customer Reviews page.

## Synthetic data and metrics

The browser generates 240 customer reviews in three cohorts:

| Cohort | Reviews | Rating distribution | Mean rating |
|---|---:|---|---:|
| Historical baseline | 60 | 30×5★, 21×4★, 6×3★, 3×2★ | 4.3 |
| Current period | 120 | 36×5★, 48×4★, 18×3★, 12×2★, 6×1★ | 3.8 |
| Simulated after | 60 | 30×5★, 12×4★, 12×3★, 6×2★ | 4.1 |

The dashboard computes the average from review records rather than displaying a separate fixed rating value. It also generates 720 fictional orders and 168 anonymised customer records. Generated records are reproducible on each app load.

The simulated-after cohort is a classroom scenario. Its difference from the current cohort does not prove that an intervention caused an improvement. Repeat-order share is based on generated repeat flags, not measured customer retention. Cost estimates exclude labor, taxes, platform commissions, and overhead.

## Agent, retrieval, and integrations

The demo is designed to make its boundaries visible:

- **Agent:** deterministic in-browser workflow; there is no external LLM configured.
- **Retrieval:** local lexical term matching across generated reviews and bundled documents; there are no embeddings or vector database.
- **Tools:** in-app simulated adapters; no external restaurant, delivery, inventory, Google, or messaging system is connected.
- **MCP:** this project does not implement a protocol-level MCP client or server.
- **Approval:** the browser demonstrates proposal review and an audit trail; local storage is not an authentication or production authorization system.

See the documentation in `app/` for further detail on architecture, retrieval, data fields, responsible use, and the presentation flow.

## Film

The final film is 4 minutes 45 seconds, aligned to the activity worksheet:

| Time | Segment |
|---|---|
| 0:00–0:40 | Act 1 — The Pain |
| 0:40–1:20 | Act 2 — The Agent Arrives |
| 1:20–2:30 | Act 3 — Under the Hood: RAG and MCP |
| 2:30–3:30 | Act 4 — Something Goes Wrong |
| 3:30–4:30 | Act 5 — The New Normal |
| 4:30–4:45 | AI tools credits |

The Q&A defence to “What happens if your agent is wrong?” is included in Act 4 and in the companion script. It covers inspecting evidence, correcting the finding, investigating the process, and requiring owner approval before consequential action.

## Project documentation

- `app/SYSTEM_ARCHITECTURE.md` — application structure and data flow
- `app/RAG_ARCHITECTURE.md` — local evidence retrieval and its limits
- `app/MCP_ARCHITECTURE.md` — simulated adapter and MCP status
- `app/DATA_DICTIONARY.md` — generated records and key fields
- `app/AGENT_WORKFLOW.md` — deterministic agent workflow
- `app/RESPONSIBLE_AI.md` — limitations and safeguards
- `app/BUSINESS_IMPACT.md` — KPI definitions and assumptions
- `app/DEMO_GUIDE.md` — five-act demonstration walkthrough

## Repository notes

This repository is a static classroom prototype. It is not intended for production use with real customer data. Before adapting it for a real business, replace the synthetic data with authorised sources, add a secure backend and authentication, implement appropriate access controls, validate business calculations, and review all food-safety and legal requirements with qualified people.

The film is included as a convenient project artifact. GitHub supports files up to 100 MB, but if the video grows beyond that in future edits, use Git LFS or publish the video separately and link to it from the repository.
