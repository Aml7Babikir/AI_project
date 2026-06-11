# Cost Curve & Pricing Strategy

## Cost Model

| Cost Category | Per-User/Month | Notes |
|---------------|----------------|-------|
| Inference (primary model) | $4.00 | Core AI generation, product analysis, requirements creation, strategy recommendations |
| Inference (cascading/triage) | $1.00 | Lightweight models for routing, summarization, classification, and prompt optimization |
| Infrastructure | $1.50 | Hosting, orchestration, monitoring, vector database, API gateway |
| Data/storage | $0.50 | User projects, embeddings, conversation history, analytics, backups |
| Human-in-the-loop | $2.00 | Customer support, quality reviews, prompt tuning, expert validation |
| **Total AI COGS** | **$9.00** | Approximate blended monthly cost per active user |

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

**Triage model:** GPT-4o Mini / Claude Haiku

**Frontier model:** GPT-5 / Claude Opus

**Routing rule:** Use the triage model for intent detection, document parsing, summarization, categorization, and simple PM tasks. Escalate to the frontier model for strategic analysis, PRD generation, competitive research, roadmap recommendations, and complex multi-step reasoning.

**Expected cascade ratio:** 80% triage model / 20% frontier model

## Pricing Model

**Current pricing:** Free beta / prototype stage

**Proposed AI pricing:** $29/month (Individual), $79/month (Pro PM), $299/month (Team)

**Model:** Hybrid (seat-based subscription with usage limits and premium AI credits for advanced workflows)

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | AI COGS increase from ~$9/user to ~$21/user. Gross margin drops from ~89% to ~73% on Pro plan. | Increase use of model routing, caching, and prompt optimization. Pass a portion of the cost increase to new customers. |
| Heaviest segment doubles | Power users consume disproportionate compute, reducing margins on fixed-price plans. | Introduce usage caps, AI credits, or premium tiers for high-volume users. |
| Model provider raises prices 50% | AI COGS increase from ~$9/user to ~$13.5/user. Margin compression across all plans. | Multi-model strategy, negotiate enterprise pricing, and shift workloads to alternative providers. |

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):**
- Fixed monthly subscription.
- Value tied to features and seats.
- Limited personalization.
- Revenue growth driven by customer acquisition and seat expansion.

**After (AI-enabled):**
- Subscription + AI-powered workflows.
- Personalized recommendations improve with usage.
- Higher engagement and retention through continuous learning.
- Opportunity for premium AI tiers, usage-based pricing, and enterprise packages.

**Net margin shift:**
- Gross margins decrease slightly due to AI serving costs (90%+ → ~80–85%).
- Revenue per customer increases through premium AI capabilities.
- Higher retention and expansion revenue offset increased AI costs.
- Overall business value increases through data flywheels and differentiated AI experiences.
