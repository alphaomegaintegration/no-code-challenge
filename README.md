# new-code-challenge
The Obsolescence of Traditional Federal Code Challenges in the AI Era

## Architecture and code map

**Architecture diagram.** The diagram shows the repo's contents: the README thesis and the three framework documents (executive summary, alternatives, financial analysis).
- Source: [`docs/architecture/architecture.json`](docs/architecture/architecture.json) (an [archify](https://github.com/tt-a1i/archify) spec).
- Rendered view: the `architecture` workflow builds it on every change and uploads `architecture-diagram` (open the latest run under Actions → architecture, download the artifact, open `architecture.html`).
- Locally: `node <archify>/bin/archify.mjs deliver architecture docs/architecture/architecture.json docs/architecture/architecture.html --quality showcase --open` (or ask Claude Code to use the archify skill). The HTML is gitignored.

**Knowledge graph (graphify).** `graphify-out/GRAPH_REPORT.md` (key concepts and connections) and `graphify-out/graph.html` (clickable graph) are committed ([report](graphify-out/GRAPH_REPORT.md), [graph](graphify-out/graph.html)); `graph.json` is gitignored and rebuilt with [`graphify`](https://github.com/safishamsi/graphify). Rebuild with `graphify update . && graphify cluster-only . --no-label` (code only, no LLM, nothing leaves the machine).
