# Local AI Agent Orchestrator
Native macOS control center for local GGUF workflows.

[Public source](https://github.com/MANTHAN137/Local-AI-Agent-Orchestrator)

![Existing public project screenshot of the agent registry](https://raw.githubusercontent.com/MANTHAN137/Local-AI-Agent-Orchestrator/main/docs/images/agents.png)

The SwiftUI/AppKit application configures local models as agents and schedules dependent work. Independent branches can run together when model slots and live memory admit them. It exposes routing, cancellation, model loading/unloading and workflow activity.

The public [0.4.1 verification notes](https://github.com/MANTHAN137/Local-AI-Agent-Orchestrator/blob/main/VERIFICATION.md) record 44 deterministic tests passing. Earlier notes record a two-model concurrent inference run. These are historical project checks; publication of this case study did not rerun them.

This is a working MVP. It has no arbitrary terminal or filesystem tools, vector memory or notarized public distribution. Optional public web tools are enabled separately per agent. Memory estimates and model size cannot guarantee accuracy or speed.

Relevant client work: native local-AI interfaces, model lifecycle integration, observable task scheduling and bounded background workflows.
