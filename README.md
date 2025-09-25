# BCQM Programs

Simulation code supporting the **Boundary-Condition Quantum Mechanics (BCQM)** framework.  
This repository contains two core models:

- **Toy Experiment** (`toy_experiment/`):  
  A minimal BCQM simulator demonstrating collapse dynamics, horizon effects, and ensemble reproducibility.  
- **Double-Slit Simulation** (`double_slit/`):  
  Numerical model of interference, decoherence, and collapse horizons in the double-slit setup.

---

## Repository Structure

```
bcqm-programs/
├─ toy_experiment/
│  ├─ bcqm_toy_experiment.py
│  ├─ *.csv                  # example output data
│  └─ README.md              # details for this module
├─ double_slit/
│  ├─ bcqm_double_slit.py
│  ├─ bcqm_double_slit_sim.py
│  └─ README.md              # details for this module
├─ requirements.txt
├─ .gitignore
└─ README.md                 # (this file)
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/<your-username>/bcqm-programs.git
cd bcqm-programs
```

Create a virtual environment and install dependencies:

```bash
python3 -m venv venv
source venv/bin/activate   # or `venv\Scripts\activate` on Windows
pip install -r requirements.txt
```

---

## Usage

### Toy Experiment
```bash
cd toy_experiment
python bcqm_toy_experiment.py
```

### Double-Slit Simulation
```bash
cd double_slit
python bcqm_double_slit_sim.py
```

Both programs generate data/figures into their respective directories.

---

## Requirements

- Python ≥3.8  
- Dependencies: `numpy`, `scipy`, `matplotlib`, `pandas`

---

## License

MIT License (or another license if you prefer).  
You are free to use, modify, and distribute this code with attribution.

---

## Citation

If you use this code in academic work, please cite:

> Ferguson, P. M. (2025). *Boundary-Condition Quantum Mechanics (BCQM): Simulation Programs*. GitHub.  
> https://github.com/<your-username>/bcqm-programs
---

# BCQM Programs

This repository contains the two small simulation programs used alongside the BCQM preprint.

- **double_slit_sim/** – double-slit ensemble simulation producing interference/incoherent outputs.
- **bcqm_toy_experiment/** – toy collapse dynamics producing damping/coherence figures.

Each subfolder includes:
- A short README explaining how the figures were generated,
- The exact `outputs/*.png` used in the paper,
- A `PROVENANCE.txt` noting environment and date.

> These scripts retain “fast/stub” branches used during exploratory runs. They’re documented in each README.