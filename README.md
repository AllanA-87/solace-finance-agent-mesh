# solace-finance-agent-mesh
A stateful, event-driven AI Agent Mesh for Finance ESG compliance using Solace PubSub+.
# Solace Finance Agent Mesh: ESG Compliance Workflow

This project demonstrates a production-grade, event-driven AI Agent Mesh built on the **Solace PubSub+** platform. It simulates a high-stakes finance environment where AI agents collaborate to enforce ESG (Environmental, Social, and Governance) compliance limits.

## 🚀 The Problem
In enterprise finance, raw LLM output is a risk. This workflow provides an **Event-Driven Guardrail** that intercepts trade requests and cross-references them against real-time risk exposure limits before approval.

## 🛠️ Tech Stack
* **Messaging:** Solace PubSub+ (Event Mesh)
* **Language:** Python 3.13
* **Framework:** Solace Agent Mesh (SAM)
* **API Layer:** FastAPI
* **State Management:** SQLite

## 🏗️ Architecture
The system uses a **Decoupled Request-Reply** pattern:
1. **Gateway:** Publishes user "Intents" to the mesh.
2. **Orchestrator:** Subscribes to intents and coordinates sub-agents.
3. **Compliance Agent:** Validates trade value against sector limits.
4. **State Agent:** Maintains conversation context.



## 📥 Installation & Setup

### Prerequisites
* Python 3.13
* A Solace PubSub+ Cloud account or local Broker

### Local Setup
1. Clone the repo:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/solace-finance-agent-mesh.git](https://github.com/YOUR_USERNAME/solace-finance-agent-mesh.git)
   cd solace-finance-agent-mesh
