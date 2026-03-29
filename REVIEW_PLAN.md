# Book Review Plan: Context Engineering

Using **Z.ai GLM-5** and **Groq Llama 3.3 70B** for peer review.

## Strategy

| Model | Use Case | Strength |
|-------|----------|----------|
| **GLM-5** (Z.ai) | Deep technical review | Reasoning + code comprehension |
| **Groq Llama 3.3 70B** | Fast pass / structural review | Speed + breadth |

## Review Workflow

### Phase 1: Structural Scan (Groq Llama - Fast)
Goal: Check flow, cross-references, consistency

1. Load all chapters sequentially
2. Prompt: "Verify chapter 1-22 flow logically. Flag missing cross-references. Check part organization."

### Phase 2: Deep Technical Review (GLM-5)
Goal: Validate technical accuracy, code examples, KG concepts

**Part I (Foundations):** Ch 1-4
- Ch 1: Why AI projects fail
- Ch 2: Context definition
- Ch 3: Context Engineering discipline
- Ch 4: Architecture of Meaning

**Part II (Knowledge Graphs):** Ch 5-9
- Ch 5-9: KG theory + Terraphim implementation

**Part III (Optimization):** Ch 10-11
- Ch 10: Token Budget
- Ch 11: Compression

**Part IV (Implementation):** Ch 12-16
- Ch 12: Skills
- Ch 13: CLAUDE.md
- Ch 14: Validation
- Ch 15: Multi-agent
- Ch 16: Hooks

**Part V (Real-World):** Ch 17-20
- Ch 17: OpenClaw
- Ch 18: Enterprise
- Ch 19: Hybrid Pipelines
- Ch 20: Practice

**Part VI (Future):** Ch 21-22
- Ch 21: Market Landscape
- Ch 22: Open Problems

### Phase 3: Synthesis (GLM-5)
- Compile findings
- Generate revision list
- Prioritize fixes

## Execution

```bash
# Phase 1: Quick scan with Groq
for ch in {01..22}; do
  echo "=== Chapter $ch ===" >> review-phase1.md
  groq "Review chapter $ch for flow and structure" < chapters/$ch.qmd >> review-phase1.md
done

# Phase 2: Deep review with GLM-5 (per part)
glm5 "Perform deep technical review of Part I (Ch 1-4). Check: accuracy of claims, code validity, KG concept correctness."
```

## Output

- `review-phase1-groq.md` - Structural findings
- `review-phase2-glm5.md` - Technical findings  
- `review-revisions.md` - Prioritized fix list

## Timeline

- Phase 1: ~30 min (Groq speed)
- Phase 2: ~2-3 hours (GLM-5 depth)
- Phase 3: ~30 min
