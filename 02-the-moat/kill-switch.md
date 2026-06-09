# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|------------|---------------|------------|----------------|
| Provider | Core intelligence powered by OpenAI models | H | Add support for Anthropic Claude and Google Gemini as fallback providers |
| Abstraction | Limited abstraction layer between application and LLM provider | H | Implement a unified AI service layer to decouple application logic from model providers |
| Routing | Single-model routing strategy | M | Introduce model routing based on use case (analysis, reasoning, summarization, extraction) |
| Eval | No formal evaluation framework for comparing model outputs | H | Build benchmark datasets and automated evaluation pipeline for key workflows |

---

# Portability Score

**2/5**

Menza AI currently relies heavily on a single foundation model provider. While the business logic and data layer are proprietary, the intelligence layer can be replicated unless model abstraction and evaluation systems are introduced.

---

## If OpenAI doubles pricing tomorrow

- Route workloads to Claude and Gemini where performance is comparable.
- Reduce expensive model calls through caching and agent optimization.
- Introduce tiered intelligence levels based on customer plans.
- Prioritize high-value workflows for premium models.

**Impact:** Moderate financial pressure, but survivable with proper abstraction.

---

## If OpenAI ships a competing product

- Compete on proprietary business context rather than model quality.
- Leverage integrations across 650+ business systems.
- Build benchmark intelligence and industry-specific insights unavailable to general-purpose assistants.
- Focus on organizational memory, business workflows, and operational recommendations.

**Impact:** High strategic risk if Menza remains a thin AI wrapper. Lower risk if Menza owns proprietary data, outcomes, and business intelligence workflows.

---

## Biggest Risk

Menza's current moat comes primarily from data integration and business context rather than AI infrastructure.

## Priority Mitigation

Over the next 90 days:

1. Implement multi-model support (OpenAI, Claude, Gemini).
2. Create a model evaluation framework.
3. Build benchmark datasets from customer outcomes.
4. Capture recommendation acceptance/rejection signals.
5. Invest in proprietary business intelligence that cannot be replicated by foundation model providers.

### Desired Future State

The AI provider becomes a replaceable component, while Menza's value comes from:
- Proprietary business context
- Benchmark intelligence
- Organizational memory
- Workflow orchestration
- Outcome-driven recommendations
