---
description: Generate investment-ready HTML business plan with adversarial validation for any business idea
---

# Investment-Ready Business Plan Generator

Generate comprehensive, investment-ready HTML business plans with adversarial validation, premium visuals, and grounded market research.

---

## Quick Reference

### Default Configuration

| Profile | Validation | Sections | Images | Charts |
|---------|------------|----------|--------|--------|
| Lite | V(3, 1, 0) | 5 core | 2 | 4 |
| **Standard** | **V(8, 3, 1)** | **10** | **4** | **8** |
| Deep | V(12, 5, 2) | 15 | 6 | 12 |

### Mode Detection

- **CREATE mode**: User says "create business plan for [X]" → Generate full plan
- **REFINE mode**: User provides existing plan → Validate and improve

### This Skill Uses

- FORGE for section validation (V(8, 3, 1) per section)
- Adversarial Validation (8-persona council)
- Web grounding for market research

---

## Phase 1: Discovery & Research

### 1. Understand the Business Concept

From user input, identify:
- Industry and target market
- Geographic focus
- Unique value proposition
- Technical requirements
- Competitive advantages

### 2. Web Research Grounding

Execute 3+ searches:
```
"[City] [industry] market size cost pricing 2024"
"[State] contractor license requirements [business type]"
"[industry] liability insurance cost 2024"
"[industry] market growth trends forecast"
"[industry] startup costs equipment pricing"
```

### 3. Document Research Findings

Create summary with:
- Market size (TAM/SAM/SOM)
- Pricing benchmarks
- Regulatory requirements
- Competitive landscape
- Industry growth rates

---

## Phase 2: Section Development with FORGE Validation

Apply V(8, 3, 1) adversarial validation to each section:

### The 8 Adversarial Personas

| # | Persona | Focus Area |
|---|---------|------------|
| 1 | Skeptical VC | Financial viability, ROI, market size |
| 2 | Insurance Actuary | Liability, coverage gaps, premiums |
| 3 | Industry Regulator | Compliance, permits, legal |
| 4 | Industry Veteran | Practical operations, margins, labor |
| 5 | Target Customer | Value proposition, trust, concerns |
| 6 | Competitor | Weaknesses, moat, differentiation |
| 7 | Safety/Risk Engineer | Equipment failure, protocols |
| 8 | Scaling CEO | Unit economics, hiring, expansion |

### 3-Round Validation per Section

**Round 1**: Each persona critiques from their lens
**Round 2**: Address critiques with web search, resolve conflicts
**Round 3**: Achieve 90%+ confidence on all claims

---

## Phase 3: Required Sections

### Core Sections (all profiles)

1. **Executive Summary** (~300 words) - Investment thesis, key metrics
2. **The Problem** (~150 words) - Pain points, market gaps
3. **The Solution** (~250 words) - Technology/service description
4. **Market Opportunity** (~200 words) - TAM/SAM/SOM, growth rates
5. **Competitive Analysis** (~200 words) - Positioning, differentiation

### Standard Profile (add these)

6. **Local Market Deep Dive** (~200 words) - Geographic-specific data
7. **Pricing Model** (~200 words) - Unit pricing, margins
8. **Financial Projections** (~200 words) - 3-year revenue, break-even
9. **Cost Breakdown** (~100 words) - Equipment, startup costs
10. **Legal & Licensing** (~200 words) - Permits, compliance

### Deep Profile (add these)

11. **Insurance Requirements** (~150 words)
12. **Operational Workflow** (~150 words)
13. **Risk Assessment** (~150 words) - Risk matrix
14. **Team & Hiring** (~100 words)
15. **Investment Ask** (~150 words) - Capital required, use of funds

---

## Phase 4: Visual Asset Creation

### Generated Images (4 minimum)

- Hero/header image showcasing the business
- System architecture or workflow diagram
- Before/after or comparison visual
- Industry-specific imagery

### CSS-Based Charts (8 minimum)

- Market growth trajectory
- Cost comparison bars
- Profit margin comparison
- TAM/SAM/SOM visualization
- Hardware/cost breakdown
- Risk assessment matrix
- Revenue projection
- Fund allocation

---

## Phase 5: HTML Document Assembly

### Design System

```css
/* Colors */
--primary: #00f3ff;    /* Cyan - innovation */
--secondary: #ffe600;  /* Yellow - energy */
--danger: #ff0055;     /* Red - risk */
--success: #00ff88;    /* Green - profit */
--dark: #0a0a0a;       /* Background */
--panel: #121218;      /* Cards */

/* Typography */
Headings: Space Grotesk
Body: Inter
Mono: JetBrains Mono
```

### Key Elements

- Validation badges on each section
- Micro-animations (fade-in on scroll)
- Responsive grid layouts
- Premium card styling
- Alternating section backgrounds

---

## Output Deliverables

1. **HTML Business Plan** (`[project]_business_plan.html`)
   - Complete standalone file
   - Embedded CSS (no external dependencies except fonts)
   - 2,500+ words of prose
   - 10+ data visualizations

2. **Assets Folder** (optional)
   - Generated images

---

## Execution Checklist

```
[ ] 1. Detect MODE (CREATE or REFINE)
[ ] 2. Identify business concept and geography
[ ] 3. Execute web research grounding (3+ searches)
[ ] 4. For each section:
      [ ] a. Draft content
      [ ] b. Apply V(8, 3, 1) validation
      [ ] c. Incorporate feedback
[ ] 5. Generate visual assets (4+ images)
[ ] 6. Create CSS charts (8+ charts)
[ ] 7. Assemble HTML document
[ ] 8. Final quality check
[ ] 9. Deliver with validation report
```

---

## Anti-Patterns

❌ **Ungrounded claims**: All financial data must cite web sources
❌ **Generic content**: Must be specific to geography and industry
❌ **Skipping validation**: Each section needs 8-persona review
❌ **Placeholder images**: Generate real imagery, no placeholders
❌ **Missing charts**: Minimum 8 data visualizations required

---

## ⚠️ Attention Boost: Critical Reminders

> **This section repeats key instructions for long-context processing.**

### DO NOT SIMPLIFY

1. **All financial claims must be web-grounded** — Search before asserting
2. **Each section gets V(8, 3, 1)** — 8 personas, 3 rounds, 1 pulse
3. **Minimum 4 images, 8 charts** — Premium visual standard
4. **2,500+ words prose** — Not a skeleton, a complete document
5. **Validation badges on every section** — Show confidence scores

### Quick Formula

```
Business Plan = 10 sections × V(8, 3, 1) each
             = 80 persona-evaluations + 10 web searches
             + 4 images + 8 charts
```

**END OF SKILL DOCUMENT**
