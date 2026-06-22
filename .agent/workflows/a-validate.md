---
description: Rigorous multi-persona adversarial validation with web grounding for any decision, design, or artifact
---

# Adversarial Validation Skill

A methodology for validating decisions, designs, documents, or code changes through structured multi-persona discourse with web-grounded research.

---

## Quick Reference

### Default Configuration

| Profile | Agents | Rounds | Pulses | Use Case |
|---------|--------|--------|--------|----------|
| Lite | 3 | 1 | 0 | Quick sanity check |
| **Standard** | **8** | **3** | **1** | **Normal validation** |
| Deep | 10 | 3 | 2 | High-stakes, investor review |

### When to Use

- Complex decisions with multiple valid approaches
- High-stakes changes (architecture, API, security, business plans)
- Contentious proposals where stakeholder disagreement is likely
- Documents for external review (investor decks, PRDs)

### Relationship to FORGE

This skill implements the **CEO council type** from FORGE, specialized for adversarial validation. It can be invoked via `/a-validate` or as part of FORGE's validation phase.

---

## The Method

### Execution Pattern (Standard: V(8, 3, 1))

```
[Pulse] → R₁ (Initial Assessment) → [Pulse] → R₂ (Refined Proposal) → [Pulse] → R₃ (Final Vote) → [Pulse]
   ↑                                    ↑                                  ↑                        ↑
   Pre-R1                           Inter-round                        Post-R2                   Final
   grounding                        conflict search                    verification              grounding
```

**Structure:**
- 8 adversarial personas evaluate the proposal
- 3 rounds of discourse with votes
- 1 web search (Pulse) between each round
- Total: 4 web searches per validation cycle

---

## The 8 Adversarial Personas (Adapt to Context)

| # | Persona | Role | Focuses On |
|---|---------|------|------------|
| 1 | Strategic Investor | VC/Funding | Capital viability, ROI |
| 2 | Technical Expert | Engineer | Feasibility, complexity, debt |
| 3 | End User | Target Customer | Value, usability, trust |
| 4 | Risk Assessor | Insurance/Legal | Liability, compliance |
| 5 | Regulatory Expert | Compliance | Legal requirements, standards |
| 6 | Market Strategist | Marketing/GTM | Messaging, positioning |
| 7 | Domain Specialist | Subject Matter Expert | Technical accuracy, edge cases |
| 8 | Devil's Advocate | Critical Thinker | Weaknesses, blind spots |

**Persona Substitution Rules:**
- Replace with project-relevant roles
- At least 3 personas should conflict by default (e.g., Cost vs. Quality)
- Always include at least one adversarial critic (#8)

---

## Round Structure

### Round 1: Initial Assessment

Each persona evaluates proposal independently:
- Vote: APPROVE / CONDITIONAL / OPPOSE
- Document specific concerns
- Flag items with confidence <90%

### Round 2: Refined Proposal

After inter-round web search:
- Incorporate R1 feedback into refined proposal
- Re-evaluate with all personas
- Track vote shifts (⬆️ upgraded, → maintained, ⬇️ downgraded)

### Round 3: Final Vote

After post-R2 verification:
- Binary APPROVE / REJECT with confidence percentage
- Document final recommendation
- Specify implementation requirements if approved

---

## Web Grounding (Pulses)

| Stage | Focus |
|-------|-------|
| Pre-R1 | Topic fundamentals, industry standards, competitor analysis |
| Inter-round 1-2 | Address specific conflicts raised in R1 |
| Inter-round 2-3 | Verify assumptions, edge cases |
| Post-R3 | Final fact-check on critical claims |

**Search Query Patterns:**
```
"[topic] best practices [industry] [year]"
"[competitor] [product] limitations [use case]"
"[domain] startup failures common reasons"
"[topic] regulations requirements [jurisdiction]"
```

---

## Conflict Resolution Protocol

When personas disagree:

1. **Identify the axis** (cost vs. quality, simplicity vs. completeness)
2. **Search for third-party data** to break the tie
3. **Propose resolution** that addresses both concerns
4. **Re-vote in Round 2** with resolution in place
5. **Document unresolved conflicts** for user decision

---

## Output Format

```markdown
## [PROPOSAL NAME] Validation

### Grounding Summary
| Source | Key Finding |
|--------|-------------|

### Round 1
| # | Persona | Vote | Concerns |
|---|---------|------|----------|

**R1 Conflicts:**
| Conflict | Personas | Resolution |
|----------|----------|------------|

### Round 2
| # | Persona | Vote | Shift |
|---|---------|------|-------|

### Round 3: Final Vote
| # | Persona | Vote | Confidence |
|---|---------|------|------------|

**FINAL: [X]/8 APPROVE. [VALIDATED/REJECTED]**

### Implementation Specification
[If validated, specific implementation details]
```

---

## Execution Checklist

```
[ ] 1. Define proposal clearly (1-2 sentences)
[ ] 2. Select/adapt 8 personas for context
[ ] 3. Execute Pre-R1 grounding (1+ searches)
[ ] 4. Run Round 1, document in table
[ ] 5. Identify conflicts, execute inter-round grounding
[ ] 6. Refine proposal based on R1 feedback
[ ] 7. Run Round 2, track vote shifts
[ ] 8. Execute Post-R2 grounding
[ ] 9. Run Round 3 final vote with confidence
[ ] 10. Document specification if approved
```

---

## Anti-Patterns

❌ **Rubber-stamping**: All 8 approve immediately → re-examine assumptions
❌ **Analysis paralysis**: 3+ rounds without convergence → escalate to user
❌ **Echo chamber**: All personas agree too easily → add adversarial persona
❌ **Scope creep**: Validation covers more than proposal → refocus

---

## ⚠️ Attention Boost: Critical Reminders

> **This section repeats key instructions for long-context processing.**

### DO NOT SIMPLIFY

1. **Default is 8 personas, 3 rounds, 1 pulse** — Standard V(8, 3, 1)
2. **Always include Devil's Advocate** — Persona #8 is mandatory
3. **Web search between rounds** — Don't skip pulses
4. **Track vote shifts** — Document ⬆️ / → / ⬇️ changes
5. **Conflicts require data** — Search to break ties, don't just compromise

### Quick Formula

```
Adversarial Validation = V(8, 3, 1)
= 8 adversarial personas × 3 rounds × 1 pulse between each
= 4 web searches + 24 persona-evaluations per validation
```

**END OF SKILL DOCUMENT**
