# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Learning Loop | Merchant questions, searches, feature usage, support interactions | Improved knowledge base and more accurate responses | Y | active |
| Recommendation Loop | Merchant actions taken on AI recommendations | Better future recommendations and prioritization | Y | active |
| Operational Benchmarking Loop | Aggregated merchant operational data | Industry benchmarks, anomaly detection, and best-practice insights | Y | missing |

**Broken loop identified by partner:**  
Operational Benchmarking Loop — Menza currently helps merchants with their own data but does not yet leverage cross-merchant insights to improve recommendations and create network effects.

**Fix plan:**  
Capture anonymized operational signals across merchants, build benchmark datasets, and use them to generate comparative insights (e.g., food cost, labor efficiency, sales trends, and menu performance). Each new merchant improves the quality of recommendations for all merchants.

---

## Context Connectivity

Menza AI sits on top of multiple restaurant operational systems, allowing knowledge to flow across traditionally siloed domains such as sales, inventory, labor, customer engagement, subscriptions, and training.

Current context connectivity is strongest within individual merchant environments, where data from different operational modules can be combined to generate recommendations and answer business questions.

### Current Knowledge Flow

- Sales → Operational recommendations
- Inventory → Cost optimization insights
- Customer behavior → Revenue opportunities
- Support interactions → Knowledge base improvements
- Training content → AI-assisted guidance

### Current Silos

- Cross-merchant benchmarking data
- Training outcomes and operational outcomes
- Support knowledge and product usage signals

### Future State

- Merchant actions improve future recommendations.
- Support and training interactions improve AI responses.
- Operational data creates industry benchmarks.
- Cross-domain signals (sales, inventory, staffing, marketing) improve decision quality.

**Goal:** Transform Menza from a reactive copilot into a continuously learning operational intelligence platform.

## Governance Policy

**Scope:**
**Autonomy boundaries:**
**Escalation triggers:**
**Audit cadence:**
**Regulatory exposure (EU AI Act / other):**

## Agent Topology
<!-- If using agents: what can each agent do? What can't it do? Who approves what? -->

## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |

**Total tools found:**
**Tools after triage:**
**Estimated hidden spend:**
