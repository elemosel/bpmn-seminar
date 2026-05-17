# BPMN Seminar — BPIC-17 Process and Data Science

Code accompanying the first individual assignment of the seminar
*Business Process Prediction, Simulation, and Optimization* (TUM,
Summer Semester 2026). Performs process discovery, conformance
checking, knowledge-distillation-based model refinement, and
data-aware decision mining on the BPIC-17 loan application event log.

## Setup

```bash
uv sync           # creates .venv and installs locked dependencies
```

Python 3.11 is pinned via `.python-version`. Graphviz must be
installed separately (system-level) for Petri-net visualisation.

## Data

The BPIC-17 event log (`BPI Challenge 2017.xes`) is **not** in this
repo. Download from
<https://data.4tu.nl/articles/dataset/BPI_Challenge_2017/12696884>
and place at `data/BPI Challenge 2017.xes`.

## Running the analysis

Open `main copy.ipynb` and execute cells in order. The notebook is
self-contained; intermediate state (Petri nets, decision trees,
quality metrics) is computed in-memory and visualisations are saved
to `outputs/`.

Key sections:
1. **Log analysis** — outcome distribution, duration percentiles,
   waiting-time bottlenecks
2. **Discovery baseline** — Alpha, Inductive, Heuristic miners
3. **Knowledge-distillation iteration** — teacher `net_final`
   (grid-search optimal) distilled onto V1/V2 backbones; final model
   V2+a
4. **Decision mining** — `DecisionTreeClassifier` per XOR gateway,
   guards extracted and annotated onto BPMN + colored Petri net

## Outputs

The `outputs/` directory contains all generated artefacts referenced
by the report:
- `*.png` — Petri net and BPMN visualisations
- `*.pnml`, `*.bpmn` — model exports
- `decision_rules_all.md` — extracted guard expressions per XOR
- `*.csv` — quality metrics, simplicity metrics, decision-mining
  summary, grid-search results

## Report

The LaTeX report source is not in this repo (compiled PDF is
submitted separately via Moodle).
