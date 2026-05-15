# Multi-model Operational Evidence

## Overview

This document indexes the public evidence files for the SomaBridge / EchoBridge v0.2 architecture update of the Action-Printer project.

The evidence records show operational testing across multiple LLM clients using the same conceptual three-layer architecture:

```text
Web or mobile LLM conversation interface
→ Google CDP browser mediation layer / SomaBridge
→ Action-Printer deterministic local execution layer
→ Desktop OS actions
```

## Evidence Files

### Claude

- `evidence/claude/claude-session-01.jpg`

Purpose:
Claude was used as an LLM client to test model-side instruction generation and interaction with the Action-Printer execution layer.

### DeepSeek

- `evidence/deepseek/deepseek-session-01.jpg`

Purpose:
DeepSeek was used as an LLM client to test whether the SomaBridge / Action-Printer structure can operate beyond a single model provider.

### Tencent Yuanbao

- `evidence/yuanbao/yuanbao-session-01.jpg`

Purpose:
Tencent Yuanbao was used as an additional LLM client to verify cross-client operation through the same architecture.

## Interpretation

These files are not intended to disclose the full private implementation.

They serve as public timestamped evidence that the Action-Printer project has been tested with multiple LLM client interfaces and has evolved into a browser-mediated, model-client-agnostic LLM-to-OS interaction architecture.

## Disclosure Boundary

The repository documents:

- Architecture
- Operational validation
- Evidence files
- Chronological public records

The repository does not fully disclose proprietary implementation details or unrestricted execution mechanisms.
