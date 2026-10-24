# Nexus
Local GGUF coding workbench · early macOS application.

[Browse the public source](https://github.com/MANTHAN137/nexus-local-ide)

## The problem
Local model integration needs a usable project workflow: select the model and project, inspect actions, apply bounded changes and see what failed.

## Implemented
- Electron and React interface with resizable explorer, editor, assistant and activity panels.
- Local llama.cpp model integration, GGUF discovery and resource controls.
- Chat, reviewed single-file edits and project-scoped file tools.
- Builder, Reviewer and Tester roles running sequentially with one loaded model.
- Cancellation, conflict detection, bounded work and memory/thermal stops.
- Optional local stdio MCP servers with macOS confinement.

<img src="../assets/nexus-workbench.jpg" alt="Browser design preview of Nexus with the included example workspace. Native inference and file access run in the desktop app." width="1000">

## Evidence and limits
The public repository includes source, setup, architecture, security notes and verification instructions. This image is a browser design preview, not an inference benchmark. The project is an early macOS app, with model-dependent capability and hardware-dependent performance.

The bounded check runner is not a general interactive terminal. Remote MCP transports, cloud model fallback and model downloads are outside the documented version. The source repository had no selected project license when reviewed; public visibility alone does not grant unrestricted reuse.

## Relevant client work
Desktop interfaces around a local AI runtime, project-scoped action controls, model-selection UX and focused debugging of an existing integration.
