# TOPIC: Sovereign SLM Routing (service-slm)

**Classification:** Totebox Service (Headless AI Bridge)
**Domain:** pointsav-monorepo

## 1. Abstract
The `service-slm` operates as a point-in-time linguistic filter and secure bridge. It utilizes locally hosted, open-weight Small Language Models (SLMs) to execute logic without exposing corporate data to external hyperscalers. It is the core engine that translates raw, noisy data into clean, self-healing intelligence.

## 2. Engineering Logic: The Linguistic Air-Lock
To preserve the mathematical integrity of the Totebox Archive, the SLM acts strictly as a data processing diode between isolated service domains.
* **Extraction:** It reads immutable compliance artifacts (e.g., from `service-email`).
* **Sanitization:** It mathematically strips headers, signatures, and legal bloat, extracting only the factual payload.
* **Deposition:** It routes the sanitized facts strictly into the self-healing holding tank (`service-content/knowledge-graph`).

## 3. The Zero-Omnipresence Mandate
Legacy SaaS architectures deploy AI as listening agents that read the entire database continuously, introducing severe prompt injection vulnerabilities. The PointSav architecture physically neuters the engine:
* **Cold-Start Execution:** The SLM operates as a batch script. It wakes up, executes a single text-extraction command, outputs a Markdown file, and shuts down.
* **Terminal Priority:** The SLM has zero execution privileges. It cannot run code, move files, or alter the `os-totebox` ledgers.
