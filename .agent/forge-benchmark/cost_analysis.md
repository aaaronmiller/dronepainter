# FORGE Methodology: Cost Analysis by Model
# Generated: 2024-12-19

## Executive Summary

This analysis calculates the **cost per FORGE run** across different AI models, determining:
1. Which profiles are viable for free-tier web usage
2. API costs per methodology
3. Cost-efficiency recommendations

**Status**: Business plan was **NOT modified** — left as-is for testing purposes.

---

## Pricing Matrix (per 1M tokens)

| Model | Input | Output | Avg (weighted 40/60) | Free Tier |
|-------|-------|--------|---------------------|-----------|
| **Claude Opus 4** | $15.00 | $75.00 | $51.00 | None |
| **Claude Sonnet 4** | $3.00 | $15.00 | $10.20 | 20 msgs/day web |
| Claude Sonnet 4 (>200K) | $6.00 | $22.50 | $15.90 | — |
| Claude Haiku 3.5 | $1.00 | $5.00 | $3.40 | Limited |
| **Gemini 2.5 Pro** | $1.25 | $10.00 | $6.50 | 50 req/day |
| Gemini 2.5 Pro (>200K) | $2.50 | $15.00 | $10.00 | — |
| **Gemini 2.0 Flash** | $0.10 | $0.40 | $0.28 | 1500 req/day |
| **Llama 405B (Azure)** | $5.33 | $16.00 | $11.73 | None* |
| Llama 405B (Fireworks) | ~$2.00 | ~$6.00 | ~$4.40 | Limited |

*OSS models require self-hosting or pay via provider

---

## FORGE Token Usage by Methodology

From benchmark results:

| Methodology | Total Tokens | Input (~40%) | Output (~60%) |
|-------------|--------------|--------------|---------------|
| Baseline | 0 | 0 | 0 |
| Self-Refine | ~2,000 | ~800 | ~1,200 |
| MAD | ~6,000 | ~2,400 | ~3,600 |
| **FORGE Lite** | ~3,500 | ~1,400 | ~2,100 |
| **FORGE Standard** | ~12,000 | ~4,800 | ~7,200 |
| FORGE Deep | ~25,000 (est.) | ~10,000 | ~15,000 |
| FORGE Exhaustive | ~50,000 (est.) | ~20,000 | ~30,000 |

---

## Cost Per FORGE Run (API)

### FORGE Lite (~3.5K tokens)

| Model | Input Cost | Output Cost | **Total** |
|-------|------------|-------------|-----------|
| Claude Opus 4 | $0.021 | $0.158 | **$0.18** |
| Claude Sonnet 4 | $0.004 | $0.032 | **$0.04** |
| Gemini 2.5 Pro | $0.002 | $0.021 | **$0.02** |
| **Gemini 2.0 Flash** | $0.0001 | $0.0008 | **$0.001** ⭐ |
| Llama 405B (Azure) | $0.007 | $0.034 | **$0.04** |

### FORGE Standard (~12K tokens)

| Model | Input Cost | Output Cost | **Total** |
|-------|------------|-------------|-----------|
| Claude Opus 4 | $0.072 | $0.540 | **$0.61** |
| Claude Sonnet 4 | $0.014 | $0.108 | **$0.12** |
| Gemini 2.5 Pro | $0.006 | $0.072 | **$0.08** |
| **Gemini 2.0 Flash** | $0.0005 | $0.003 | **$0.003** ⭐ |
| Llama 405B (Azure) | $0.026 | $0.115 | **$0.14** |

### FORGE Exhaustive (~50K tokens)

| Model | Input Cost | Output Cost | **Total** |
|-------|------------|-------------|-----------|
| Claude Opus 4 | $0.30 | $2.25 | **$2.55** |
| Claude Sonnet 4 | $0.06 | $0.45 | **$0.51** |
| Gemini 2.5 Pro | $0.025 | $0.30 | **$0.33** |
| **Gemini 2.0 Flash** | $0.002 | $0.012 | **$0.01** ⭐ |
| Llama 405B (Azure) | $0.11 | $0.48 | **$0.59** |

---

## Free Tier Viability Analysis

### Web-Based "Free" Usage Thresholds

| Platform | Daily Limit | FORGE Profile Viable? |
|----------|-------------|----------------------|
| **Claude.ai (free)** | ~20 msgs/day | FORGE Lite (1-2) ❌ Exhaustive |
| **Claude.ai (Pro $20/mo)** | ~100+ msgs/day | FORGE Standard ✅ |
| **Gemini.google.com** | Unlimited (free) | All profiles ✅ |
| **ChatGPT (free)** | ~15-20 msgs/day | FORGE Lite only |
| **ChatGPT Plus ($20/mo)** | 80-100 GPT-4 msgs | FORGE Standard ✅ |

### Recommended Free-Tier Configuration

| Profile | Best Free Platform | Notes |
|---------|-------------------|-------|
| **FORGE Lite** | Gemini web (free) | Unlimited with Flash |
| **FORGE Standard** | Gemini web OR Claude Pro | Full validation |
| **FORGE Deep** | Gemini web only | Needs high volume |
| **FORGE Exhaustive** | API only | Too many turns for web UI |

---

## Extended Thinking Cost Impact

Claude Sonnet with Extended Thinking uses additional "thinking tokens" that count as output:

| Thinking Budget | Extra Output Tokens | Extra Cost (Sonnet 4) |
|-----------------|--------------------|-----------------------|
| Light (10K) | +10,000 | +$0.15 |
| Medium (32K) | +32,000 | +$0.48 |
| Heavy (64K) | +64,000 | +$0.96 |

**For FORGE Standard + Extended Thinking (Medium):**
- Base: $0.12
- Thinking: +$0.48
- **Total: $0.60** (5x base cost)

**Recommendation**: Use extended thinking only for FORGE Deep/Exhaustive on high-stakes documents.

---

## Model Recommendations by Use Case

### Daily Web Usage (Free)
| Use Case | Model | Profile | Cost |
|----------|-------|---------|------|
| Quick sanity check | Gemini Flash (web) | FORGE Lite | $0.00 |
| Document review | Gemini Pro (web) | FORGE Standard | $0.00 |
| Full validation | Claude Pro (sub) | FORGE Standard | $20/mo flat |

### API Usage (Pay-per-use)
| Use Case | Model | Profile | Cost/run |
|----------|-------|---------|----------|
| High-volume screening | Gemini 2.0 Flash | FORGE Lite | $0.001 |
| Production quality | Gemini 2.5 Pro | FORGE Standard | $0.08 |
| Maximum quality | Claude Opus 4 | FORGE Exhaustive | $2.55 |
| OSS alternative | Llama 405B | FORGE Standard | $0.14 |

### Quality vs. Cost Efficiency

| Model | Quality Tier | Cost Efficiency (quality/$) |
|-------|-------------|----------------------------|
| Gemini 2.0 Flash | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ (best value) |
| Gemini 2.5 Pro | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| Claude Sonnet 4 | ⭐⭐⭐⭐ | ⭐⭐⭐ |
| Claude Opus 4 | ⭐⭐⭐⭐⭐ | ⭐⭐ (premium) |
| Llama 405B | ⭐⭐⭐⭐ | ⭐⭐⭐ |

---

## Cost Comparison Summary

### FORGE Standard (12K tokens) Across Models

```
Gemini 2.0 Flash:   $0.003  ████░░░░░░░░░░░░░░░░░░░░░░░░░░ (cheapest)
Gemini 2.5 Pro:     $0.08   ████████░░░░░░░░░░░░░░░░░░░░░░
Sonnet 4:           $0.12   ████████████░░░░░░░░░░░░░░░░░░
Llama 405B:         $0.14   ██████████████░░░░░░░░░░░░░░░░
Opus 4:             $0.61   ██████████████████████████████ (premium)
```

### ROI Analysis

Running FORGE Standard on 100 documents:

| Model | Cost | Quality Score | Cost per Quality Point |
|-------|------|---------------|----------------------|
| Gemini Flash | $0.30 | 7.2 | $0.04 |
| Gemini Pro | $8.00 | 7.8 | $1.03 |
| Sonnet 4 | $12.00 | 7.9 | $1.52 |
| Opus 4 | $61.00 | 8.2 | $7.44 |

---

## Key Findings

1. **Gemini 2.0 Flash is 200x cheaper than Opus 4** for equivalent token usage
2. **Free tier covers FORGE Lite and Standard** on Gemini web
3. **Extended Thinking adds 5x cost** — use selectively
4. **OSS (Llama 405B) is mid-tier pricing** when hosted via Azure
5. **Opus 4 is only justified for investor-grade/legal documents**

---

## Appendix: Token Usage Formulas

```
FORGE Token Estimate:

Base tokens = Document size (chars) / 4
Council overhead = X × Y × 150 tokens per persona-round
Search context = (Z + W) × Y × 500 tokens per search
Synthesis = T × 200 tokens per concept

TOTAL ≈ Base + Council + Search + Synthesis

Example FORGE Standard (T=10, X=10, Y=3, Z=1, W=1):
  Base: 3000 / 4 = 750
  Council: 10 × 3 × 150 = 4,500
  Search: 2 × 3 × 500 = 3,000
  Synthesis: 10 × 200 = 2,000
  TOTAL: ~10,250 tokens (close to 12K observed)
```
