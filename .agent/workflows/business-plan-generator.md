---
description: Generate investment-ready HTML business plan with adversarial validation for any business idea
---

# Investment-Ready Business Plan Generator

This skill generates comprehensive, investment-ready HTML business plans with adversarial validation, premium visuals, and grounded market research. Designed to create documents capable of securing investment.

## Prerequisites
- Access to web search for market research grounding
- Image generation capability (or browser access to AI image generators)
- Target market/location for the business

## Workflow Steps

### Phase 1: Discovery & Research

1. **Understand the Business Concept**
   - Read any provided transcripts, notes, or descriptions
   - Identify: Industry, target market, geography, unique value proposition
   - Extract: Technical requirements, competitive advantages, operational model

2. **Conduct Web Research Grounding**
   Search for the following (adapt to specific business):
   - `[City/Region] [industry] market size cost pricing 2024 2025`
   - `[State] contractor license requirements [business type] registration`
   - `[industry] liability insurance cost 2024`
   - `[industry] market growth trends 2024 2025`
   - `[industry] startup costs equipment pricing`

3. **Document Research Findings**
   Create a research summary with:
   - Market size (TAM/SAM/SOM)
   - Pricing benchmarks (per unit, per hour, per sqft, etc.)
   - Regulatory requirements (licenses, permits, insurance)
   - Competitive landscape data
   - Industry growth rates

---

### Phase 2: Section Development with Adversarial Validation

For each section, apply the 10-Persona, 3-Round validation methodology:

#### The 10 Adversarial Personas

| # | Persona | Focus Area |
|---|---------|-----------|
| 1 | **Skeptical VC** | Financial viability, ROI, market size |
| 2 | **Insurance Actuary** | Liability, coverage gaps, premiums |
| 3 | **Industry Regulator** | Compliance, permits, legal requirements |
| 4 | **Industry Veteran** | Practical operations, margins, labor |
| 5 | **IP/Business Attorney** | Contracts, liability, indemnification |
| 6 | **Safety Engineer** | Equipment failure, safety protocols |
| 7 | **Target Customer** | Value proposition, trust, concerns |
| 8 | **Competitor** | Weaknesses, moat, differentiation |
| 9 | **Environmental Officer** | Regulatory, environmental compliance |
| 10 | **Scaling CEO** | Unit economics, hiring, expansion |

#### 3-Round Discourse Structure

**Round 1: Initial Critique**
- Each persona reviews section from their expert lens
- Identifies gaps, errors, outdated information
- Flags items with confidence < 90%

**Round 2: Defense & Counter-Arguments**
- Address critiques with additional web search
- Resolve conflicts between personas
- Update content with grounded data

**Round 3: Consensus Building**
- Final validation pass
- Achieve 90%+ confidence on all claims
- Document remaining caveats

---

### Phase 3: Required Sections (Adapt as Needed)

Generate 10-15 sections depending on business type:

1. **Executive Summary** (~300 words)
   - Investment thesis, key metrics, opportunity summary

2. **The Problem** (~150 words)
   - Pain points, market gaps, customer frustrations

3. **The Solution** (~250 words)
   - Technology/service description, key innovations

4. **Market Opportunity** (~200 words)
   - TAM/SAM/SOM, growth rates, market timing

5. **Competitive Analysis** (~200 words)
   - Positioning matrix, differentiation, moat

6. **Local/Target Market Deep Dive** (~200 words)
   - Geographic-specific data, pricing, demand

7. **Pricing Model** (~200 words)
   - Unit pricing, margins, comparison to alternatives

8. **Financial Projections** (~200 words)
   - 3-year revenue, unit economics, break-even

9. **Cost Breakdown / BOM** (~100 words)
   - Equipment, startup costs, sources

10. **Legal & Licensing** (~200 words)
    - Required permits, registrations, compliance checklist

11. **Insurance Requirements** (~150 words)
    - Coverage types, annual costs, providers

12. **Operational Workflow** (~150 words)
    - Day-to-day operations, process flow

13. **Risk Assessment** (~150 words)
    - Risk matrix (likelihood × impact), mitigations

14. **Team & Hiring** (~100 words)
    - Required skills, org structure, hiring timeline

15. **Investment Ask & Use of Funds** (~150 words)
    - Capital required, allocation, milestones

---

### Phase 4: Visual Asset Creation

1. **Generate Images** (3-5 minimum)
   - Hero/header image showcasing the business
   - System architecture or workflow diagram
   - Before/after or comparison visual
   - Additional industry-specific imagery

   Image prompts should include:
   - Subject matter (what to show)
   - Aesthetic style (cyberpunk, professional, clean, etc.)
   - Technical quality (4K, photorealistic, etc.)
   - Color scheme (match document palette)

2. **Create CSS-Based Charts** (8-12 minimum)
   - Market growth trajectory
   - Cost comparison bars
   - Profit margin comparison
   - TAM/SAM/SOM visualization
   - Hardware/cost breakdown
   - Risk assessment matrix
   - Revenue projection
   - Fund allocation

---

### Phase 5: HTML Document Assembly

#### Design System

```css
/* Color Palette */
--primary: #00f3ff;    /* Innovation/tech - cyan */
--secondary: #ffe600;  /* Energy/action - yellow */
--danger: #ff0055;     /* Risk/warning - red */
--success: #00ff88;    /* Positive/profit - green */
--dark: #0a0a0a;       /* Background */
--panel: #121218;      /* Cards */
--text: #e0e0e0;       /* Body text */

/* Typography */
Headings: Space Grotesk (or similar modern sans)
Body: Inter (clean, readable)
Mono: JetBrains Mono (data/code)

/* Key Elements */
- Validation badges on each section
- Micro-animations (fade-in on scroll)
- Glowing accents on hover
- Responsive grid layouts
- Premium card styling with borders
```

#### Document Structure
```html
1. Hero section with stats overlay
2. Alternating light/dark section backgrounds
3. Grid layouts (2-col, 3-col) for content
4. Bar charts with animated fills
5. Tables with hover states
6. Risk badges (color-coded)
7. CTA box with glow animation
8. Footer with disclaimer
```

---

### Phase 6: Validation Report

Include in final deliverable:
- Validation methodology used
- Confidence scores per section
- Key findings from adversarial review
- Resolved conflicts
- Remaining caveats/assumptions

---

## Output Deliverables

1. **HTML Business Plan** (`[project]_business_plan.html`)
   - Complete, standalone HTML file
   - Embedded CSS (no external dependencies except Google Fonts)
   - ~2,500+ words of prose
   - 10+ data visualizations
   - Micro-animations for engagement

2. **Assets Folder** (`assets/`)
   - Generated images
   - Any additional visual resources

3. **Research Summary** (optional artifact)
   - Grounded data sources
   - Validation notes

---

## Example Usage

```
User: Create an investment-ready business plan for a mobile pet grooming service in Austin, TX

Agent:
1. Researches Austin pet services market, pricing, regulations
2. Applies 10-persona validation to each section
3. Generates professional imagery
4. Builds premium HTML document
5. Delivers complete package with validation report
```

---

## Quality Checklist

Before delivering:
- [ ] All sections have validation badges with confidence scores
- [ ] All financial claims grounded via web search
- [ ] All regulatory requirements verified for specific geography
- [ ] Premium visual design with micro-animations
- [ ] 10+ charts/graphs included
- [ ] Professional imagery generated
- [ ] ~2,500+ words of compelling prose
- [ ] Document opens correctly in browser
- [ ] All images load properly
