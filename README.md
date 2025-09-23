# BCQM Programs

This repository contains the simulation code accompanying the *Boundary-Condition Quantum Mechanics (BCQM)* paper.

## Contents
- `double_slit/` — double-slit simulation illustrating ensemble interference vs. incoherent sums.
- `toy_experiment/` — compact BCQM toy model demonstrating the collapse horizon \(W\) (and optional speculative \(V\)).

Outputs, figures, and large artifacts are intentionally excluded to keep the repository light. Re-run scripts to regenerate plots locally.

## Quick start
```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt

# run the double-slit demo (adjust filename if needed)
python double_slit/double_slit_sim.py

# run the toy model (adjust filename if needed)
python toy_experiment/bcqm_toy.py
```
