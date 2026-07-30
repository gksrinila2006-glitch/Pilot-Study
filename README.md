🏥 Problem Definition

Modern Hospital Management Systems (HMS) consist of hundreds of distributed services that continuously exchange clinical and operational data. During production failures, engineering teams encounter several challenges that delay incident resolution and affect the reliability of healthcare services.

These challenges include:

Large volumes of heterogeneous logs generated from multiple distributed services.
Manual correlation of application logs, infrastructure metrics, deployment history, and system events.
Difficulty identifying the actual root cause across interconnected systems.
Repeated investigation of similar incidents due to limited reuse of organizational knowledge.
Long incident resolution times that impact hospital operations and patient services.
Heavy dependence on experienced engineers for complex troubleshooting.
Limited explainability in existing monitoring tools, which primarily detect failures rather than explain why they occurred.

These challenges increase operational costs, reduce system availability, and negatively impact the quality and continuity of healthcare services.

💡 Solution Overview

Instead of relying on a single AI model, the system adopts a Multi-Agent AI Architecture, where specialized AI agents analyse different aspects of an incident in parallel.

The architecture consists of the following agents:

Orchestrator Agent
Log Analysis Agent
Metrics Analysis Agent
Event Analysis Agent
Deployment Analysis Agent
Correlation Agent
Knowledge Retrieval Agent (RAG)
Recommendation Agent

Each agent performs a specialised task and returns its findings to the Orchestrator Agent, which correlates the collected evidence to identify the most probable root cause.

The system also retrieves similar historical incidents from a knowledge base, recommends corrective actions, and continuously improves through engineer feedback.

📋 Functional Requirements

The system should:

Collect logs from distributed services.
Collect infrastructure and application metrics.
Receive alerts from monitoring systems.
Analyse incidents using multiple AI agents.
Correlate evidence from multiple sources.
Retrieve similar incidents from the knowledge base.
Generate Root Cause Analysis (RCA).
Recommend corrective actions.
Record engineer feedback.
Continuously update organizational knowledge.
