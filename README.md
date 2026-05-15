# Action-Printer

## Update: SomaBridge / EchoBridge v0.2

Action-Printer now includes **SomaBridge / EchoBridge**, a CDP-mediated browser bridge layer that connects web-based LLM conversation interfaces to the Action-Printer deterministic local execution system.

The updated architecture is:

```text
Web LLM conversation window
→ Google CDP browser layer
→ SomaBridge bridge interface
→ Action-Printer local skill library
→ Desktop OS actions
```

SomaBridge is documented here:

- [docs/somabridge.md](docs/somabridge.md)

## Evidence

Multi-model operational evidence is documented here:

- [docs/evidence.md](docs/evidence.md)

## Public Technical Record

This repository documents real-world tests in which large language model (LLM) applications were used to operate a desktop computer through an external execution gateway.

## Verified Timestamped Evidence

The experiment log has been permanently recorded using Git version control and cryptographic commit history.

**Primary Evidence (Immutable Commit Record):**
https://github.com/ruikhu007/action-printer/commit/e94e91975c8a974ea23207b02d5aaa5d47fb279d

**SomaBridge Disclosure Commit:**
https://github.com/ruikhu007/action-printer/commit/be7216604eb5933bfa4a9806eff81ab101db86bd

These commits contain timestamped public disclosure of the architecture and real-world validation.

## Purpose

The purpose of this repository is chronological technical disclosure.
It serves as a public engineering record establishing that:

- A mobile or web LLM application can issue operational instructions
- Instructions can be transmitted through a constrained execution interface
- A desktop computer can be directly operated via the external execution gateway
- A Google CDP-mediated browser layer can bridge web-based LLM conversation interfaces with the Action-Printer execution layer

No proprietary or unsafe control access is provided in this repository.
This repository is documentation of architecture and experiment only.

## Date of Initial Disclosure

March 1, 2026
