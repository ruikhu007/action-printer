# SomaBridge / EchoBridge

## Overview

SomaBridge, also referred to as EchoBridge, is a browser-mediated bridge layer that connects web-based large language model (LLM) interfaces to the Action-Printer deterministic local execution system.

This document records SomaBridge as an update and architectural extension of the Action-Printer project.

## Three-layer Architecture

The current architecture is organized as a three-layer interaction structure:

```text
Web LLM conversation window
→ Google CDP browser layer
→ SomaBridge bridge interface
→ Action-Printer local skill library
→ Desktop OS actions
```

## Design Principle

SomaBridge does not give the model direct control over the operating system.

The web or mobile LLM client remains the model-side interaction surface. The Google CDP-controlled browser layer observes and writes back to the conversation interface. Action-Printer remains the deterministic local execution layer that maps approved intent into constrained desktop actions.

## Role of Google CDP

Google Chrome DevTools Protocol (CDP) is used as the browser mediation layer for observing and writing back to web-based LLM conversation interfaces.

This makes the bridge model-client agnostic. The same local Action-Printer execution layer can be driven by different LLM clients without embedding the model into the desktop operating system and without relying on private API interception.

## Tested Interfaces

Initial operational testing has included the following LLM clients:

- Claude
- DeepSeek
- Tencent Yuanbao

## Safety Boundary

The LLM does not execute arbitrary operating system commands.

Desktop operations are executed only through the Action-Printer local skill library and constrained execution gateway.

## Disclosure Statement

This file serves as a timestamped public disclosure of SomaBridge as an architectural upgrade to the Action-Printer project.

Core implementation details are intentionally not fully open-sourced at this stage. This repository documents the architecture, validation record, and public disclosure timeline.