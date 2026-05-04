# ☀️ Quantum Photosynthesis & CO₂ Upcycling Research

> **Status:** Active · Ongoing citizen science research  
> **Started:** May 2026  
> **Maintainer:** [@berniepng](https://github.com/berniepng)

---

## Overview

This repository documents a long-term independent research programme exploring a central question:

> _Can quantum computing help us decode the quantum mechanics of photosynthesis — and use those principles to engineer artificial systems that convert greenhouse gases into useful molecules?_

This sits at the intersection of **quantum biology**, **quantum chemistry simulation**, and **climate technology**. The research is conducted as a citizen scientist — no institutional affiliation, no lab access — using open datasets, open-source tools, and publicly available quantum hardware.

This README is a living document. It will evolve as new findings, papers, companies, and experiments are added.

---

## Table of Contents

1. [Problem Statement](#1-problem-statement)
2. [Current Landscape](#2-current-landscape)
   - [Research Findings](#21-research-findings)
   - [Companies](#22-companies)
   - [Institutions](#23-institutions)
   - [Key Scientists](#24-key-scientists)
3. [How Quantum Computing Can Help](#3-how-quantum-computing-can-help)
4. [Prototype: Citizen Science Simulation](#4-prototype-citizen-science-simulation)
5. [Repo Structure](#5-repo-structure)
6. [Roadmap](#6-roadmap)
7. [Contributing & Notes](#7-contributing--notes)

---

## 1. Problem Statement

Global warming is driven by the accumulation of greenhouse gases — primarily CO₂ — in the atmosphere. Nature already has a near-perfect solution: **photosynthesis**, a process that has been converting CO₂ and sunlight into useful organic molecules for approximately 3.5 billion years.

What makes photosynthesis remarkable is not just its chemistry — it's the _efficiency_ of its energy transfer. Light-harvesting complexes in plants and bacteria transfer absorbed solar energy to reaction centres with near-100% quantum yield. Emerging evidence suggests this isn't classical physics at work. **Quantum mechanical effects — coherence, superposition, and possibly entanglement — appear to play a functional role in making this energy transfer so efficient.**

The central hypothesis of this research programme:

> If we can decode the quantum mechanical principles behind photosynthetic energy transfer, and simulate those principles using quantum computers, we can design artificial molecular systems that replicate and exceed nature's efficiency — and use them to upcycle CO₂ and other greenhouse gases into valuable molecules (fuels, plastics, chemicals).

This is not a single solved problem. It is three interconnected frontiers:

| Layer                         | Question                                                         | Status                                                    |
| ----------------------------- | ---------------------------------------------------------------- | --------------------------------------------------------- |
| **Quantum Biology**           | Do quantum effects meaningfully drive photosynthesis efficiency? | Confirmed experimentally; functional significance debated |
| **Quantum Simulation**        | Can quantum computers model these molecular dynamics?            | Demonstrated at small scale (IBM Q, 2020)                 |
| **Artificial Photosynthesis** | Can we engineer CO₂ → useful molecules systems?                  | Commercially operational (no quantum design layer yet)    |

The gap this research explores: **using quantum computing to close the loop between biological insight and engineered CO₂ conversion.**

---

## 2. Current Landscape

### 2.1 Research Findings

#### Foundational Papers

| Paper                                                                                          | Authors                                  | Year | Significance                                                                                            | Link                                                                                        |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------- | ---- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| Evidence for wavelike energy transfer through quantum coherence in photosynthetic systems      | Engel, Fleming et al.                    | 2007 | First experimental evidence of quantum coherence in FMO complex at 77K                                  | [Nature 446, 782–786](https://www.nature.com/articles/nature05678)                          |
| Long-lived quantum coherence in photosynthetic complexes at physiological temperature          | Panitchayangkoon, Engel et al.           | 2010 | Extended quantum coherence observed at room temperature                                                 | [PNAS 107, 12766](https://www.pnas.org/doi/10.1073/pnas.1005484107)                         |
| Environment-assisted quantum transport                                                         | Rebentrost, Mohseni, Lloyd, Aspuru-Guzik | 2009 | Showed environmental noise _assists_ rather than disrupts quantum transport                             | [New J. Phys. 11, 033003](https://iopscience.iop.org/article/10.1088/1367-2630/11/3/033003) |
| Quantum biology revisited                                                                      | Cao, Cogdell, Engel, Scholes et al.      | 2020 | Critical reassessment of the field; honest review of what is/isn't proven                               | [Science Advances](https://www.science.org/doi/10.1126/sciadv.aaz4888)                      |
| Simulation of non-radiative energy transfer in photosynthetic systems using a quantum computer | Guimarães, Tavares, Vasilevskiy          | 2020 | **Key paper**: FMO energy transfer simulated on IBM Q 5-qubit computer                                  | [arXiv:2009.01283](https://arxiv.org/abs/2009.01283)                                        |
| Reassessing the role and lifetime of Qx in chlorophyll a energy transfer                       | Keil, Hauer et al.                       | 2024 | Quantum superposition shown as first stage of energy transfer in chlorophyll                            | [Chemical Science, RSC](https://pubs.rsc.org/en/content/articlelanding/2024/sc/d4sc06441k)  |
| Full microscopic simulations uncover persistent quantum effects in primary photosynthesis      | —                                        | 2025 | Most recent confirmation of persistent quantum effects                                                  | [Science Advances](https://www.science.org/doi/10.1126/sciadv.ady6751)                      |
| Artificial photosynthetic processes using CO₂, water and sunlight                              | —                                        | 2025 | Comprehensive review of solar-driven CO₂ reduction                                                      | [RSC Chemical Science](https://pubs.rsc.org/en/content/articlehtml/2025/sc/d5sc03976b)      |
| Artificial photosynthesis catalyst converts CO₂ to methane                                     | In, Powar et al.                         | 2025 | Photocatalyst converting CO₂ → methane at atomic-level detail, quantum mechanical calculations          | [ACS Catalysis](https://pubs.acs.org/doi/10.1021/acscatal.5c05258)                          |
| Recent Progress in Designing Nanomaterial Biohybrids for Artificial Photosynthesis             | Jeevanandham et al.                      | 2025 | Nanomaterial hybrids combining photocatalysts with biological enzymes; quantum efficiency exceeding 20% | [NCBI / Nanomaterials](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC12113824/)              |

#### Open Databases & Datasets

| Resource               | Use                                                                     | Link                                                         |
| ---------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------ |
| RCSB Protein Data Bank | FMO complex structure (PDB: `3ENI`), chlorophyll proteins               | [rcsb.org](https://www.rcsb.org)                             |
| PubChem                | Molecular data for photocatalysts, chlorophyll, CO₂ reduction catalysts | [pubchem.ncbi.nlm.nih.gov](https://pubchem.ncbi.nlm.nih.gov) |
| ChEMBL                 | Bioactive molecule and catalyst screening                               | [ebi.ac.uk/chembl](https://www.ebi.ac.uk/chembl/)            |
| NIST Chemistry WebBook | Molecular spectroscopy and thermochemical data                          | [webbook.nist.gov](https://webbook.nist.gov)                 |
| IBM Quantum Network    | Free access to real quantum hardware for simulation experiments         | [quantum.ibm.com](https://quantum.ibm.com)                   |

---

### 2.2 Companies

| Company                                                              | Focus                                                                                             | Stage               | Notable                                                                                               | Link                                         |
| -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------- | ----------------------------------------------------------------------------------------------------- | -------------------------------------------- |
| **Twelve** (formerly Opus 12)                                        | Industrial photosynthesis: CO₂ + water + renewable electricity → hydrocarbons, jet fuel, polymers | Commercial          | $187M raised; backed by DCVC, Chan Zuckerberg Initiative; working with Mercedes-Benz, aviation sector | [twelve.co](https://www.twelve.co)           |
| **Quantinuum**                                                       | Quantum computing + quantum chemistry simulation                                                  | Commercial          | Helios platform; active chemistry simulation programs                                                 | [quantinuum.com](https://www.quantinuum.com) |
| **IBM Quantum**                                                      | Quantum hardware + open access platform                                                           | Commercial          | Free tier available; FMO simulation already demonstrated on IBM Q                                     | [quantum.ibm.com](https://quantum.ibm.com)   |
| **Google Quantum AI**                                                | Quantum hardware, quantum chemistry                                                               | Research/Commercial | Cirq open source framework; collaborations with quantum chemistry groups                              | [quantumai.google](https://quantumai.google) |
| **PsiQuantum**                                                       | Photonic quantum computing                                                                        | Pre-commercial      | $1B raised (2025); photon-based qubits relevant to photosynthesis-inspired architectures              | [psiquantum.com](https://www.psiquantum.com) |
| **Panasonic / Toyota R&D / Mitsubishi Chemical / Fujitsu / Toshiba** | Artificial photosynthesis R&D                                                                     | Corporate R&D       | Major players in the $109M (2026) and growing artificial photosynthesis market                        | Various                                      |

---

### 2.3 Institutions

| Institution                                           | Programme                                                                                                   | Link                                                     |
| ----------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| **Joint Center for Artificial Photosynthesis (JCAP)** | Lawrence Berkeley National Lab / Caltech — largest US government-funded artificial photosynthesis programme | [solarfuelshub.org](https://solarfuelshub.org)           |
| **Cyclotron Road / Activate**                         | Lawrence Berkeley National Lab fellowship that incubated Twelve (formerly Opus 12)                          | [activate.org](https://www.activate.org)                 |
| **University of Toronto**                             | Aspuru-Guzik lab — quantum computing + quantum chemistry, molecular machine learning                        | [matter.toronto.edu](https://matter.toronto.edu)         |
| **University of Chicago**                             | Engel lab — 2D electronic spectroscopy of photosynthetic systems                                            | [chemistry.uchicago.edu](https://chemistry.uchicago.edu) |
| **UC Berkeley**                                       | Fleming lab — quantum biology, ultrafast spectroscopy                                                       | [lb.berkeley.edu](https://lb.berkeley.edu)               |
| **MIT**                                               | Seth Lloyd group — quantum transport theory                                                                 | [mit.edu](https://www.mit.edu)                           |
| **TU Munich**                                         | Hauer lab — quantum mechanics in photosynthesis (2024 Chemical Science paper)                               | [tum.de](https://www.tum.de)                             |
| **University of Gothenburg**                          | Westenhoff group — critical analysis of quantum coherence claims                                            | [gu.se](https://www.gu.se)                               |

---

### 2.4 Key Scientists

| Name                     | Institution              | Contribution                                                                                                              | Notable Work                                                                      |
| ------------------------ | ------------------------ | ------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| **Graham Fleming**       | UC Berkeley              | Godfather of quantum photosynthesis; led 2007 _Nature_ paper establishing quantum coherence in FMO                        | [Scholar](https://scholar.google.com/scholar?q=Graham+Fleming+photosynthesis)     |
| **Gregory Engel**        | University of Chicago    | Extended coherence to room temperature; 2D electronic spectroscopy methods                                                | [Lab](https://engellab.uchicago.edu)                                              |
| **Alán Aspuru-Guzik**    | University of Toronto    | Bridge between quantum biology and quantum computing; molecular ML; computational coherence modeling                      | [Lab](https://matter.toronto.edu)                                                 |
| **Seth Lloyd**           | MIT                      | Quantum transport theory; environment-assisted quantum walks; coined "quantum hanky-panky"                                | [MIT](https://www.mit.edu)                                                        |
| **Gregory Scholes**      | Princeton                | Observed quantum coherence in cryptophyte algae at ambient conditions                                                     | [Scholar](https://scholar.google.com/scholar?q=Gregory+Scholes+photosynthesis)    |
| **Jürgen Hauer**         | TU Munich                | 2024 discovery of quantum superposition as first stage of chlorophyll energy transfer                                     | [TUM](https://www.tum.de)                                                         |
| **Etosha Cave**          | Twelve (co-founder)      | Stanford PhD; developed photosynthesis-mimicking CO₂ reduction catalysts, co-founded Twelve                               | [Twelve](https://www.twelve.co)                                                   |
| **Kendra Kuhl**          | Twelve (co-founder, CTO) | Stanford PhD; core catalyst engineering behind Twelve's CO₂ electrolyser technology                                       | [Twelve](https://www.twelve.co)                                                   |
| **Sebastian Westenhoff** | University of Gothenburg | Critical perspective: argues quantum coherence in natural photosynthesis may be misinterpreted — essential counterbalance | [Scholar](https://scholar.google.com/scholar?q=Westenhoff+quantum+photosynthesis) |

---

## 3. How Quantum Computing Can Help

Classical computers struggle to simulate quantum mechanical systems because the state space grows **exponentially** with the number of interacting particles. A system of N quantum particles requires 2^N classical bits to represent — which becomes intractable fast.

Photosynthetic systems are exactly this kind of problem. The Fenna-Matthews-Olson (FMO) complex — the most studied quantum photosynthetic structure — involves 7–8 coupled chlorophyll molecules whose excitation dynamics are governed by quantum mechanics. To understand _why_ nature achieves near-100% energy transfer efficiency, you need to simulate these quantum dynamics accurately.

**Quantum computers can simulate quantum systems natively** — using qubits to directly represent quantum states, reducing exponential classical cost to polynomial quantum cost.

### What's already been done

- The Haken-Ströbl model of FMO energy transfer has been **simulated on IBM Q** (5 qubits), validating quantum coherence dynamics against analytical results ([Guimarães et al., 2020](https://arxiv.org/abs/2009.01283))
- Variational Quantum Eigensolver (VQE) algorithms have been applied to molecular ground-state problems relevant to photocatalyst design
- Aspuru-Guzik's group has pioneered quantum algorithms for simulating vibronic spectra and molecular energy landscapes

### Where the frontier is (2026)

1. **Scale up FMO simulation** — current 5-qubit demos are proof-of-concept; full FMO requires ~50+ logical qubits
2. **Design new photocatalysts** — use quantum chemistry simulation to screen novel molecular configurations for CO₂ reduction efficiency
3. **Optimize reaction pathways** — quantum ML to predict which CO₂ → molecule conversion pathways are most energetically favourable
4. **Close the loop** — feed quantum simulation insights back into materials synthesis guidance

### Key algorithms to study

| Algorithm                                           | Application                                               |
| --------------------------------------------------- | --------------------------------------------------------- |
| **VQE** (Variational Quantum Eigensolver)           | Ground state energy of photocatalyst molecules            |
| **QAOA** (Quantum Approximate Optimisation)         | Reaction pathway optimisation                             |
| **Quantum Walks**                                   | Energy transfer simulation in FMO                         |
| **Lindblad Master Equation (open quantum systems)** | Simulating decoherence effects in biological environments |

---

## 4. Prototype: Citizen Science Simulation

### Philosophy

No lab. No institutional access. No experimental equipment. But the mathematics of quantum photosynthesis is **open, documented, and runnable on free platforms** — including real quantum hardware.

The goal of this prototype track is:

1. Reproduce published results (credibility baseline)
2. Explore parameter space computationally (hypothesis generation)
3. Visualise findings to build intuition (communication)
4. Identify anomalies or questions worth investigating further

### Stack

| Layer              | Tool                                                                                                 | Purpose                                              | Cost      |
| ------------------ | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------- | --------- |
| Quantum simulation | [QuTiP](https://qutip.org)                                                                           | Open quantum systems, Lindblad dynamics, FMO model   | Free      |
| Quantum hardware   | [IBM Quantum](https://quantum.ibm.com)                                                               | Run circuits on real quantum computers               | Free tier |
| Quantum circuits   | [Qiskit](https://qiskit.org)                                                                         | Build and simulate quantum algorithms                | Free      |
| Molecular data     | [RDKit](https://www.rdkit.org)                                                                       | Cheminformatics, molecular fingerprinting            | Free      |
| Protein structure  | [RCSB PDB](https://www.rcsb.org) + [PyMol](https://pymol.org)                                        | Visualise FMO complex structure                      | Free      |
| ML on molecules    | [DeepChem](https://deepchem.io) / [ChemBERTa](https://huggingface.co/seyonec/ChemBERTa-zinc-base-v1) | Predict catalyst properties from molecular structure | Free      |
| Visualisation      | [Streamlit](https://streamlit.io) + [Plotly](https://plotly.com)                                     | Interactive dashboards for simulation results        | Free      |
| Environment        | [Jupyter](https://jupyter.org) / [Google Colab](https://colab.research.google.com)                   | Notebooks, free GPU                                  | Free      |

### Milestone Sequence

```
Milestone 1 — Reproduce FMO energy transfer (QuTiP, Haken-Ströbl model)
    ↓
Milestone 2 — Run FMO simulation on IBM Q (Qiskit, replicate Guimarães 2020)
    ↓
Milestone 3 — Fetch FMO structure from PDB, visualise with PyMol / 3Dmol.js
    ↓
Milestone 4 — Screen CO₂ reduction catalysts using RDKit + DeepChem ML
    ↓
Milestone 5 — Build Streamlit dashboard connecting simulations + visualisations
    ↓
Milestone 6 — Run VQE on a small photocatalyst molecule (H₂O, CO₂ fragments)
    ↓
Milestone 7 — Publish findings and open hypothesis log
```

### Getting Started

```bash
# Clone this repo
git clone https://github.com/your-handle/quantum-photosynthesis-research.git
cd quantum-photosynthesis-research

# Install core dependencies
pip install qutip qiskit qiskit-ibm-runtime rdkit deepchem streamlit plotly numpy matplotlib

# Run first experiment: FMO Haken-Ströbl simulation
jupyter notebook notebooks/01_fmo_haken_strobl.ipynb
```

> IBM Quantum free account: [quantum.ibm.com](https://quantum.ibm.com)  
> Google Colab (no install needed): [colab.research.google.com](https://colab.research.google.com)

---

## 5. Repo Structure

```
quantum-photosynthesis-research/
│
├── README.md                          ← This file (living document)
│
├── notebooks/                         ← Jupyter notebooks, numbered by milestone
│   ├── 01_fmo_haken_strobl.ipynb      ← Milestone 1: Classical quantum sim of FMO
│   ├── 02_ibmq_fmo_circuit.ipynb      ← Milestone 2: IBM Q circuit implementation
│   ├── 03_pdb_structure_viz.ipynb     ← Milestone 3: FMO protein structure
│   └── 04_catalyst_screening.ipynb   ← Milestone 4: ML catalyst screening
│
├── src/
│   ├── models/                        ← Quantum system models (Hamiltonians, Lindbladians)
│   ├── utils/                         ← Data loaders, PDB parsers, molecule utilities
│   └── visualization/                 ← Reusable plot and dashboard components
│
├── experiments/
│   ├── fmo_simulation/                ← FMO energy transfer experiments
│   ├── co2_catalysts/                 ← CO₂ catalyst screening experiments
│   └── quantum_circuits/              ← Qiskit circuit experiments
│
├── data/
│   ├── raw/                           ← Downloaded PDB files, molecular datasets
│   ├── processed/                     ← Cleaned, transformed data
│   └── references/                    ← Downloaded papers (PDFs), notes
│
├── results/
│   └── figures/                       ← Output plots and visualisations
│
├── docs/
│   ├── hypothesis_log.md              ← Running log of hypotheses and questions
│   ├── reading_list.md                ← Papers read, annotated
│   └── glossary.md                    ← Key terms and definitions
│
├── requirements.txt                   ← Python dependencies
├── environment.yml                    ← Conda environment spec
└── .gitignore
```

---

## 6. Roadmap

- [ ] **Milestone 1** — Reproduce Haken-Ströbl FMO energy transfer in QuTiP
- [ ] **Milestone 2** — Run FMO quantum circuit on IBM Q (replicate Guimarães 2020)
- [ ] **Milestone 3** — Visualise FMO protein structure from PDB
- [ ] **Milestone 4** — Screen CO₂ catalysts with RDKit + ML
- [ ] **Milestone 5** — Streamlit dashboard: energy transfer + molecule viewer
- [ ] **Milestone 6** — VQE experiment on CO₂ / H₂O molecular fragments
- [ ] **Milestone 7** — Publish hypothesis log and invite collaboration
- [ ] _(Future)_ — Connect quantum simulation outputs to catalyst design suggestions
- [ ] _(Future)_ — Benchmark artificial photosynthesis efficiency vs. natural FMO

---

## 7. Contributing & Notes

This is an independent, open research log. If you're a researcher, student, or fellow citizen scientist working in quantum biology, artificial photosynthesis, or quantum chemistry simulation — feel free to open an issue, submit a PR, or reach out.

**Ethos:** Rigorous curiosity. No institutional gatekeeping. Open science.

---

_Last updated: May 2026_
