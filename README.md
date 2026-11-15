# Andrew Wang · 王施元

MS ECE at Carnegie Mellon University, AI/ML Systems · BS Computer Science, UC Santa Barbara.

I build systems that keep long-lived data, agent-assisted delivery, and the history behind both inspectable. I am looking for **Summer 2027 internships in AI infrastructure, LLM systems, and backend engineering**.

[Website](https://andrew05060414.github.io/) · [LinkedIn](https://www.linkedin.com/in/andrewwanglink/) · [Email](mailto:andrewwangmail@gmail.com)

## What I build

PXRead is the application, Antiochus defines the coordination and delivery boundaries, and Chronicle is the history-retrieval entry point. I use these projects to work on three connected engineering problems: preserving application data, making assisted delivery inspectable, and retaining useful work history. Their source remains private; these are selected public summaries, not a claim that every planned integration is deployed.

**[PXRead](https://andrew05060414.github.io/#project-pxread)** separates a work from its readable editions, so duplicates and later versions do not overwrite one another. A local service stores body files by content hash and applies compare-and-set when advancing an edition's revision head. Imports produce source records, candidate metadata, confidence, and explicit decisions such as append, fork, skip, or send for review. Reading has one EPUB path; annotations use EPUB positions and can be identified as detached when the edition no longer matches. I can discuss the domain model, import decisions, immutable revisions, and annotation tests.

**[Antiochus](https://andrew05060414.github.io/#project-antiochus)** is the control layer around assisted delivery: task intake, risk tiers, reviewer routing, review evidence, and the gates that decide whether a change is ready. A verdict is tied to an exact commit; a newer commit makes the old verdict stale. The controller separates work routing from merge authority, escalates stuck reviews, and records human gates. Planned categories are kept distinct from implemented behavior.

**[Chronicle](https://andrew05060414.github.io/#project-chronicle)** is one command-line entry point for searching and exporting long-lived agent history. A route table dispatches retrieval to AgentsView while preserving arguments and exit codes; outbound text, JSON, and JSONL pass through a redaction wrapper. Tests cover routing, argument quoting, error propagation, and secret stripping. The search engine underneath is third-party work.

## Upstream contributions

These are merged fixes to projects maintained by others, not projects I founded:

- [AgentsView #2439](https://github.com/kenn-io/agentsview/pull/2439) — session format parsing.
- [OpenCodex #8644](https://github.com/lidge-jun/opencodex/pull/8644) — provider model selection.
- [AzurPilot #803](https://github.com/wess09/AzurPilot/pull/803) — configuration I/O side effects.
