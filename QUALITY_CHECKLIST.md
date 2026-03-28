# Chapter Quality Checklist (Zestic Publishing)

Based on ZDP v2.3 quality standards, each chapter must pass:

## Content Quality

- [ ] **Completeness**: All outline items from context-engineering-outline.md are covered
- [ ] **Accuracy**: Technical claims are verifiable (cite sources)
- [ ] **Structure**: Follows book outline flow (concepts before implementation)
- [ ] **Cohesion**: Connects to previous/next chapters (use cross-references)

## Writing Quality

- [ ] **Clarity**: Each paragraph has one main idea
- [ ] **Examples**: At least one concrete example per major concept
- [ ] **Code**: Code blocks are runnable/verified
- [ ] **Tables**: Complex comparisons use tables for readability

## Technical Quality

- [ ] **Cross-references**: Links to related chapters (Ch.1→Ch.4→Ch.8 for concept modelling)
- [ ] **Sources**: Citations to external research (Zestic AI, MedGemma, etc.)
- [ ] **Research integration**: CTO Executive System learnings incorporated
- [ ] **No hallucinated facts**: Claims about tools/frameworks match reality

## Format Quality (Quarto)

- [ ] **Valid QMD**: Renders without errors (`quarto check`)
- [ ] **Heading hierarchy**: H1 for chapter title, H2 for major sections
- [ ] **Code blocks**: Fenced with language identifier
- [ ] **Links**: External links are valid

## Review Requirements

| Stage | Review Type | Approver |
|-------|-------------|----------|
| draft | self | Author |
| final_draft | peer | Peer (not author) |
| release | internal + gate | 2+ reviewers |

## Current Status

Chapters 1-12: Self-reviewed (draft quality), need peer review for final_draft
