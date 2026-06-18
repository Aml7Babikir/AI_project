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
Menza AI provides operational insights, recommendations, diagnostics, and workflow assistance for restaurant operators. The system can analyze business data and suggest actions but does not independently execute high-impact business changes.

**Autonomy boundaries:**  
- Can analyze data and generate recommendations.
- Can answer operational and business questions.
- Can draft actions and workflows for user approval.
- Cannot modify pricing, financial settings, inventory levels, payroll, or customer-facing operations without explicit user approval.
- Cannot perform irreversible actions autonomously.

**Escalation triggers:**  
- Financial impact exceeds predefined thresholds.
- AI confidence falls below acceptable levels.
- Recommendations conflict with historical business patterns.
- Sensitive customer or employee data is involved.
- Regulatory or compliance-related decisions are requested.

**Audit cadence:**  
- Weekly review of AI-generated recommendations.
- Monthly evaluation of model quality and hallucination rates.
- Quarterly governance and compliance review.
- Annual security and data privacy assessment.

**Regulatory exposure (EU AI Act / other):**  
- Low to Medium Risk.
- Primarily a business operations copilot.
- Requires transparency that outputs are AI-generated.
- Requires audit logging and human oversight for business-critical decisions.
- Subject to data privacy regulations (GDPR, local privacy laws) where applicable.

---

## Agent Topology

### Operations Analyst Agent
**Can do:**
- Analyze restaurant performance.
- Identify trends and anomalies.
- Generate operational insights.

**Cannot do:**
- Execute operational changes.
- Modify business configurations.

---

### Recommendation Agent
**Can do:**
- Recommend actions to improve sales, margins, labor efficiency, and customer retention.
- Prioritize opportunities.

**Cannot do:**
- Automatically implement recommendations.

---

### Knowledge Agent
**Can do:**
- Answer product, operational, and training-related questions.
- Surface best practices and documentation.

**Cannot do:**
- Create or modify source-of-truth content.

---

### Workflow Agent
**Can do:**
- Draft workflows and action plans.
- Prepare configuration changes for approval.

**Cannot do:**
- Publish or execute changes without approval.

---

### Human Approval Layer

**Approves:**
- Financial changes.
- Operational changes.
- Configuration updates.
- Customer-facing actions.
- High-impact recommendations.

---

## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|--------|--------|-----------|----------|
| ChatGPT | Individual employees | M | govern |
| Claude | Individual employees | M | govern |
| Gemini | Individual employees | L | keep |

**Total tools found:** 3

**Tools after triage:** 3

**Estimated hidden spend:**  
$200–$500/month during early-stage adoption across product, operations, support, and leadership teams.
