# AutonomQA
**Self-Planning LLM Agents for High-Coverage Web QA**

---

## Overview
**AutonomQA** is an autonomous, multi-agent web testing framework powered by Large Language Models (LLMs). It transforms **natural-language testing goals** into executable browser-based test cases, adapts dynamically to UI and DOM changes, and produces human-readable test reports without relying on brittle, hand-written scripts.

The framework is designed for modern CI/CD environments where rapid UI evolution often breaks traditional automated test suites.

---

## Motivation
Manual and script-based web testing faces several persistent challenges:

- High maintenance cost due to fragile DOM-dependent scripts  
- Test failures caused by minor UI or layout changes  
- Record-and-replay tools breaking under dynamic interfaces  
- Time-consuming, repetitive, and error-prone manual testing  

Although UI implementations change frequently, **high-level testing intent remains stable**. AutonomQA leverages this insight by reasoning over intent rather than fixed UI structure.

---

## Key Contributions
- **Natural-Language Test Execution** – Write tests as plain English goals  
- **Multi-Agent Architecture** – Specialized agents collaborate to plan, execute, recover, and report  
- **Self-Healing Tests** – Automatically recovers from missing elements, wrong actions, or navigation failures  
- **High Coverage & Efficiency** – Robust execution across diverse web applications  

---

## System Architecture

### Core Agents
- **Instruction Agent**  
  Decomposes a high-level testing goal into granular unit test cases.

- **Execution Agent**  
  Performs browser interactions using LLM-based reasoning and adapts dynamically when failures occur.

- **DOM Parser**  
  Converts raw HTML into a structured, semantic representation of elements with unique identifiers.

- **Browser Parser**  
  Maintains browser state, including active tabs, navigation history, and page metadata.

- **Tool Agent**  
  Handles specialized tasks beyond standard DOM interaction:
  - Login validation  
  - Form validation  
  - Hidden HTML extraction  
  - External service integration  

- **Reporter Agent**  
  Aggregates execution outcomes into structured, human-readable summaries for developers.


## Example Test Case

### Input (Natural Language Goal)
