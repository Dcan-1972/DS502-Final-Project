# DS502 Final Project

Final project repository for DS502: Introduction to Operational Research Techniques Using Data Science.

The project studies ATM cash replenishment under demand uncertainty, based on the robust optimization approach from Ekinci, Serban, and Duman (2021). The notebook builds a Python simulation workflow, visualizes ATM locations, and evaluates replenishment cost behavior under different assumptions.

## Repository Contents

- `DS502 - Final Project Code.ipynb` - main Python notebook
- `DS502-Final Project Report.pdf` - final written report
- `DS502 - Final Project Presentation.pdf` - final presentation slides
- `requirements.txt` - Python dependencies for reproducing the notebook

## Project Overview

The notebook includes:

- synthetic ATM demand and location generation
- ATM cluster/location visualization with Folium
- demand uncertainty and replenishment-cost simulation
- forecasting and regression-based demand components
- sensitivity analysis for replenishment and shortage-cost behavior

Running the notebook generates:

- `atm_locations.html`
- `paper_model_comprehensive.png`

These files are reproducible outputs and are intentionally ignored by Git.

## Setup

Python 3.11 is recommended.

Create and activate a virtual environment:

```bash
python -m venv .venv
```

On Windows:

```bash
.venv\Scripts\activate
```

On macOS/Linux:

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start Jupyter:

```bash
jupyter notebook
```

Then open `DS502 - Final Project Code.ipynb`.

## Reproduce the Notebook

To execute the notebook from the command line:

```bash
jupyter nbconvert --to notebook --execute --ExecutePreprocessor.timeout=1200 --output executed_final_project.ipynb "DS502 - Final Project Code.ipynb"
```

## Verification

The notebook was tested locally with `jupyter nbconvert --execute` and completed successfully. A GitHub Actions workflow also executes the notebook on pushes and pull requests.

## Reference

Ekinci, Y., Serban, N., & Duman, E. (2021). Optimal ATM replenishment policies under demand uncertainty. *Operational Research*, 21, 999-1029. https://doi.org/10.1007/s12351-019-00466-4
