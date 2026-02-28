# External Action Printer

This project explores a safer way for LLM agents to operate real computers.

Instead of giving an AI system direct control over the operating system, we separate:

Cognition (LLM)  
Execution (Gateway)

The intelligence runs inside an official mobile LLM app (ChatGPT / Claude).

The execution layer is an external gateway that translates instructions into deterministic OS actions.

## Architecture

phone LLM app → data link → action gateway → predefined action skills → desktop OS

The gateway does not allow arbitrary code execution.
It only performs whitelisted primitives:

•⁠  ⁠keyboard sequences
•⁠  ⁠window operations
•⁠  ⁠command calls

## Technical Idea

The model never directly controls the interface.

We built a local action skill library.

The LLM selects a skill.
The gateway executes it.

We turned computer control from a continuous control problem into a discrete decision problem.

## Experimental Setup

The prototype was tested using an official mobile LLM application (Claude mobile app) paired with the external execution gateway.

The model ran entirely inside the mobile application.
No API keys or embedded model processes were used on the computer.

The desktop system only received constrained action commands selected from a predefined local skill library.

This makes the system predictable, auditable, and safer.
