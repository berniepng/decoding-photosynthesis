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

### HYP-003: Upgrade to 8-site FMO Hamiltonian
**Date:** 2026-05-04
**Status:** Open
**Question:** Does adding the 8th BChl molecule (discovered by Tronrud et al. 2009) at the chlorosome interface meaningfully change the energy transfer dynamics compared to the standard 7-site model?
**Hypothesis:** The 8th BChl acts as an entry relay — accelerating the initial population drop from BChl 1 and shifting early-time oscillations, but leaving the final transfer to BChl 3 largely unchanged since it sits upstream of the main 7-site highway.
**Experiment:** Implement the 8-site Hamiltonian from Tronrud et al. 2009, rerun Haken-Ströbl simulation, compare BChl 3 population at t=0.5ps and t=2.0ps against the 7-site result.
**Links:** Tronrud et al. 2009 — *The structural basis for the difference in absorbance spectra for the FMO antenna protein*, `notebooks/01_fmo_haken_strobl.ipynb`
**Notes:** 7-site model (Adolphs & Renger 2006) remains the established benchmark. 8-site extension is the natural next step once Milestone 1 is fully validated.

---

### HYP-004: ENAQT peak confirmed at room temperature
**Date:** 2026-05-04
**Status:** Confirmed ✅
**Question:** Does environmental noise assist rather than hinder quantum energy transfer in FMO, and does efficiency peak at biological room temperature (γ ≈ 100 cm⁻¹)?
**Hypothesis:** Yes — the ENAQT curve peaks at γ = 100 cm⁻¹, exactly where green sulfur bacteria operate, consistent with Rebentrost, Mohseni, Lloyd & Aspuru-Guzik 2009.
**Experiment:** Section 5 dephasing sweep in `notebooks/01_fmo_haken_strobl.ipynb` — five Lindblad simulations at γ = 10, 50, 100, 300, 1000 cm⁻¹, population at BChl 4 measured at t = 0.3 ps.
**Links:** [Rebentrost et al. 2009](https://iopscience.iop.org/article/10.1088/1367-2630/11/3/033003), `notebooks/01_fmo_haken_strobl.ipynb`
**Notes:** Results — γ=10: 0.0412, γ=50: 0.0977, γ=100: 0.1125 (peak), γ=300: 0.1018, γ=1000: 0.0554. Peak lands exactly on orange room-temperature line. Classical simulation on Google Colab using QuTiP. Milestone 1 complete.

---
