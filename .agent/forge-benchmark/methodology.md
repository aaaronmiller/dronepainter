# FORGE Benchmark Testing Methodology
# Compares FORGE against: Self-Refine, Multi-Agent Debate (MAD), and baseline (no refinement)

## Test Design

### Test Cases
We will use a document refinement task - improving the `aerostroke_business_plan.html` content.

### Methodologies to Compare
1. **Baseline**: Single-pass generation (no refinement)
2. **Self-Refine**: Single agent, iterative self-critique (Y rounds, X=1)
3. **Multi-Agent Debate (MAD)**: X agents debate, fixed 3 rounds
4. **FORGE Lite**: V(3, 1, 1, 0) - 3 personas, 1 round, 1 pre-search
5. **FORGE Standard**: V(10, 3, 1, 1) - 10 personas, 3 rounds, grounded

### Evaluation Dimensions
| Dimension | Measurement | Weight |
|-----------|-------------|--------|
| Factual Accuracy | Count of verifiable claims validated | 25% |
| Completeness | Coverage of required sections | 20% |
| Coherence | Logical flow between sections | 20% |
| Actionability | Specificity of recommendations | 15% |
| Cost Efficiency | Tokens consumed / quality gained | 20% |

### Test Protocol

```
FOR EACH test_case IN [business_plan_section]:
    FOR EACH methodology IN [baseline, self_refine, mad, forge_lite, forge_standard]:
        
        1. EXTRACT original text
        2. APPLY methodology
        3. RECORD:
           - Token count (input + output)
           - Time elapsed
           - Number of iterations/rounds
        4. EVALUATE output on 5 dimensions (1-10 scale)
        5. CALCULATE weighted score
        
    COMPARE results
    REPORT winner per dimension and overall
```

---

## Simulated Test Execution

Since we cannot actually run multiple LLM instances simultaneously, we will:
1. Execute each methodology sequentially as a simulated council
2. Use web grounding to validate factual claims
3. Score outputs based on structural analysis

### Test Target
File: `aerostroke_business_plan.html`
Section: Executive Summary (for manageable scope)
