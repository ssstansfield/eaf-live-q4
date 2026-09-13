# EAF LIVE Q4 — Extreme Value Analysis

This repository contains the Question 4 analysis for the Module 2 EAF LIVE project. The notebook evaluates heavy-tailed losses and estimates 99% loss quantiles using Gaussian, empirical, peaks-over-threshold (POT), and Hill estimators.

## Contents

- `Q4.ipynb` — main analysis notebook
- `600900.SH.xlsx` — Yangtze Power price data
- `882528.WI.xlsx` — Wind Public Electricity Index data
- `000300.SH.xlsx` — CSI 300 Index data
- `Q4.pptx` — presentation deck
- `LIVE 2 Script.md` — presentation script

The three Excel files remain in the repository root because `Q4.ipynb` reads them using relative paths.

## Run locally

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
jupyter lab Q4.ipynb
```

The project files were copied from the original course directory without modifying the source files.
