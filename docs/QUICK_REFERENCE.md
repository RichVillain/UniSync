# UniSync — Quick Reference

## What is UniSync?

UniSync is a dual-calculator platform system that provides:
- **SoulCode Calculator:** Personal metric analysis with comprehensive assessment framework
- **LifeCode Calculator:** Core life metric computation with rigorous mathematical optimization
- **Educational Framework:** Transparent, explainable calculation methodology for users
- **Strategic Vision:** Overarching direction and feature roadmap

**Status:** Phase 1 — Specification & Architecture Design
**Owner:** Project Lead (RichVillain)
**Team:** Engineering (Claude AI Agent)

---

## The Five Core Documents

### 1. SoulCode Calculator (117.8 KB)
**What:** Complete SoulCode calculator system with analysis framework
**Key Content:** Implementation patterns, calculation logic, analysis modules
**Priority:** DO FIRST (Quadrant I)
**Action:** Extract algorithm specs; implement in `services/engine/soulcode/`

### 2. LifeCode Calculator (84.9 KB)
**What:** Complete LifeCode calculator system with analysis framework
**Key Content:** Core implementation, calculation flows, system integration
**Priority:** DO FIRST (Quadrant I)
**Action:** Extract algorithm specs; implement in `services/engine/lifecode/`

### 3. LifeCode Math Optimization (85.6 KB)
**What:** Rigorous mathematical analysis for LifeCode USLC system
**Key Content:** Formulas, optimization algorithms, computational complexity, numerical stability
**Priority:** DO FIRST (Quadrant I)
**Action:** Translate math to code; create reference implementation in `services/engine/lifecode/math.py`

### 4. Individual Chart Calculations Framework (65.9 KB)
**What:** Educational framework for transparent calculation disclosure
**Key Content:** Methodology explanation, user-facing documentation, calculation steps
**Priority:** SCHEDULE (Quadrant II)
**Action:** Create UI component for calculation explainability; build help content

### 5. Vision Compendium (Binary)
**What:** Strategic direction, roadmap, and decision framework
**Key Content:** Platform vision, feature priorities, governance rules
**Priority:** SCHEDULE (Quadrant II)
**Action:** Extract to markdown; use as arbiter for design decisions

---

## Key Insights

### No Waste
- **0 items** in "Delegate" quadrant (Urgent + Not Important)
- **0 items** in "Eliminate" quadrant (Not Urgent + Not Important)
- **100% focus** on strategic, important work

### Consolidation Opportunities
1. **Shared Calculator Base:** Both SoulCode and LifeCode can inherit from `CalculatorBase` class
2. **Unified Math Authority:** Single spec document serves both implementation and user education
3. **Common Pipeline:** Shared data validation, caching, serialization infrastructure

### Timeline
- **Weeks 1-2:** Foundation (specs, architecture, infrastructure)
- **Weeks 3-4:** LifeCode implementation + math optimization
- **Weeks 5-6:** SoulCode implementation
- **Weeks 7-8:** User experience layer (explainer UI, docs, education)
- **Weeks 9-10:** Polish, optimization, release

---

## Where Things Go

```
Repository Integration Map

Source documents (SoulCode/LifeCode PDFs, math spec, vision compendium)
    ↓
    ├─→ services/engine/          (Calculator implementations)
    ├─→ docs/MATH_SPEC.md         (Extracted mathematical specs)
    ├─→ docs/VISION.md            (Extracted vision & strategy)
    ├─→ apps/web/components/      (User-facing calculation UI)
    └─→ packages/api-client/      (API types & client)
```

---

## Success Metrics

| Metric | Target |
|--------|--------|
| Test Coverage | 90%+ |
| API Response Time (p50) | < 20ms |
| API Response Time (p99) | < 100ms |
| Calculator Accuracy | 100% (verified against spec) |
| Documentation Completeness | 100% |
| User Satisfaction with Explainability | 4.5+/5.0 |

---

## Getting Started

### For New Team Members
1. Read `docs/QUICK_REFERENCE.md` (this file)
2. Read `docs/CONSOLIDATION.md` (full strategy)
3. Read `services/engine/docs/MATH_SPEC.md` (technical foundation, once written)
4. Check `services/engine/calculator_base.py` (architecture pattern, once written)

### For Implementers
1. Start with shared infrastructure (`services/engine/shared/`)
2. Implement LifeCode + math first (Sprint 2)
3. Implement SoulCode second (Sprint 3)
4. Build UI explainers (Sprint 4)

### For Product/Design
1. Reference `docs/VISION.md` for direction (once extracted)
2. Review Eisenhower Matrix in `docs/CONSOLIDATION.md` for prioritization
3. Schedule quarterly vision review sessions
4. Track user feedback on calculation transparency

---

## Eisenhower Matrix (Visual Summary)

```
                    IMPORTANT
                        ↑
         ╔═════════════════════════════════════╗
         ║      DO FIRST (Quadrant I)         ║
         ║  ▪ SoulCode Calculator             ║
         ║  ▪ LifeCode Calculator             ║
         ║  ▪ Math Optimization               ║
         ║                                    ║
  URGENT ║                                    ║ NOT URGENT
         ║      (Nothing here - Good!)        ║
         ╚═════════════════════════════════════╝
              ↑
         ╔═════════════════════════════════════╗
         ║    SCHEDULE (Quadrant II)          ║
         ║  ▪ Educational Framework           ║
         ║  ▪ Vision Compendium               ║
         ║                                    ║
         ║      (Nothing here - Good!)        ║
         ╚═════════════════════════════════════╝
                    NOT IMPORTANT
```

---

## Questions?

- **Full strategy?** See `docs/CONSOLIDATION.md`
- **For architecture questions?** Review `docs/CONSOLIDATION.md` § "Dual Calculator Architecture"
- **Where did this come from?** See `docs/PROVENANCE.md`

---

**Originally authored:** 2026-07-12 (on `RichVillain/Ndrap-platform`, branch `claude/uploads-batches-eisenhower-gzlel7`)
**Extracted to this repository:** 2026-07-13
**Status:** Analysis Complete • Pending Implementation
