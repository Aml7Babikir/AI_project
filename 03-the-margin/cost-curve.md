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
| Inference costs 3x | | |
| Heaviest segment doubles | | |
| Model provider raises prices 50% | | |

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):**
**After (AI-enabled):**
**Net margin shift:**
