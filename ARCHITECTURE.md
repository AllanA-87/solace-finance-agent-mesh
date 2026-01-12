# Agent Mesh Logic Flow

This document describes how the Request-Reply pattern is handled within the mesh.

### 1. Topic Hierarchy
We use a structured hierarchy for granular filtering:
* `finance/esg/request/v1`: Where the UI publishes trade intents.
* `finance/esg/response/v1`: Where the Orchestrator publishes final decisions.

### 2. The Decision Loop
1. **User Request:** "Buy 50k shares of PANW."
2. **Orchestrator:** Parses the intent and triggers the **Compliance Agent**.
3. **Compliance Agent:** - Queries Current Sector Value ($1.2M).
   - Calculates Transaction Value (50k * $340 = $17M).
   - Rejects if New Sector Percentage > 15%.
4. **State Agent:** Stores the rejection reason in SQLite for conversation continuity.
