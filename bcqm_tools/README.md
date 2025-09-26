# bcqm_tools — Reproducible tools for the BCQM companion

This folder is **drop-in**: copy it into your repo (e.g. `BCQM-Programs/`) and you can run the tools
**without installing** or, optionally, install just this subfolder as a package.

## Quick start (no install)

From the repository root (where this `bcqm_tools/` folder sits):

```bash
# Show help
python -m bcqm_tools.cli --help

# RAMSEY (constant gamma) — writes CSV/PNG/JSON under bcqm_tools/examples/
python -m bcqm_tools.cli ramsey --gamma 0.1 --fstar 0.9 --tmax 5e-5 --dt 2e-7 --out bcqm_tools/examples/ramsey

# GKLS qubit (phase-covariant; pure dephasing example)
python -m bcqm_tools.cli gkls --gamma-phi 0.1 --gamma-relax 0.0 --tmax 5e-5 --dt 5e-7 --out bcqm_tools/examples/gkls

# Galton channels (seeded)
python -m bcqm_tools.cli galton --rows 10 --n 1000 --seed 42 --out bcqm_tools/examples/galton
```

## Run from YAML (zero-typing of params)

```bash
# Run the sample configs:
python -m bcqm_tools.run_from_yaml --config bcqm_tools/configs/ramsey_constant.yml
python -m bcqm_tools.run_from_yaml --config bcqm_tools/configs/gkls_basic.yml
python -m bcqm_tools.run_from_yaml --config bcqm_tools/configs/galton.yml
```

## Optional: install this subfolder as a package

```bash
cd bcqm_tools
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\Activate.ps1
pip install -e .
bcqm --help
```

## Requirements

- Python 3.9+
- Dependencies listed in `bcqm_tools/requirements.txt` (or use `pip install -e .` to auto-install).

## Reproducibility features

- All stochastic steps are **seeded**.
- Each run writes a `*.json` **metadata** file (parameters + Python/platform versions).
- Unit tests (`pytest -q`) cover Ramsey constant-γ and pure dephasing decay.

## Layout

```
bcqm_tools/
  README.md
  requirements.txt
  pyproject.toml            # optional local install
  LICENSE
  CITATION.cff
  configs/
    ramsey_constant.yml
    gkls_basic.yml
    galton.yml
  examples/                 # outputs written here
  tests/
    test_ramsey.py
    test_gkls.py
  bcqm_tools/
    __init__.py
    cli.py
    run_from_yaml.py
    ramsey.py
    gkls.py
    galton.py
    utils.py
  .gitignore
```
