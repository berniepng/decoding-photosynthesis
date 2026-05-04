# Hypothesis Log

> A running record of open questions, hypotheses, and research directions.  
> Each entry should link to relevant papers or experiments where possible.

---

## Format

```
### HYP-XXX: [Short title]
**Date:** YYYY-MM-DD  
**Status:** Open / Testing / Confirmed / Rejected  
**Question:** What are we asking?  
**Hypothesis:** What do we expect to find?  
**Experiment:** How would we test this?  
**Links:** Relevant papers or notebooks  
**Notes:** Findings, updates, observations
```

---

## Log

### HYP-001: FMO coherence time vs. temperature
**Date:** 2026-05-04  
**Status:** Open  
**Question:** How does quantum coherence lifetime in the FMO complex change across biologically relevant temperatures (77K → 310K)?  
**Hypothesis:** Coherence time decreases as temperature increases, but remains long enough for efficient energy transfer at room temperature — consistent with Panitchayangkoon et al. 2010  
**Experiment:** QuTiP Haken-Ströbl model, sweep temperature parameter, plot coherence decay rate  
**Links:** [PNAS 107, 12766](https://www.pnas.org/doi/10.1073/pnas.1005484107), `notebooks/01_fmo_haken_strobl.ipynb`  
**Notes:** —

---

### HYP-002: IBM Q decoherence vs. biological decoherence
**Date:** 2026-05-04  
**Status:** Open  
**Question:** Is the decoherence timescale of current IBM Q qubits comparable to, shorter than, or longer than quantum coherence in biological FMO?  
**Hypothesis:** IBM Q T2 coherence times (~100 microseconds) are actually *longer* than FMO coherence (~100–500 femtoseconds), which means noise is the limiting factor in simulating biology on hardware — not hardware limitations per se  
**Experiment:** Compare IBM Q T2 specs against published FMO coherence lifetimes  
**Links:** [Guimarães et al. 2020](https://arxiv.org/abs/2009.01283)  
**Notes:** —

---

*Add new hypotheses above this line.*
