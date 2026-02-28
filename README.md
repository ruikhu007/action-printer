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

This makes the system predictable, auditable, and safer.
