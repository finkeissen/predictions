# predictions

Versioned, referenceable, **operationally verifiable** projections  
as the operational layer derived from `hypotheses` + `matrix` under MMS governance.

## Purpose of this repository

This repository contains **exclusively**:

- projections / consequence derivations (“predictions”) from explicit hypotheses (`H###`)  
- run artifacts with **manifest obligation** (inputs/outputs/validation)  
- evaluations including documented failures (spiral model)

**Important:**  
There are **no** new hypotheses here (those belong in `hypotheses`) and no black-box optimization / no “fitting”.  
Permitted are constraint-based derivations, consequence maps, scenario trees, and traceable transitions.

## Architectural embedding (as of February 2026)

Layer ordering (canonical):

0. legacy (inadmissibility)  
1. research-program (analytics)  
2. mms (dbms)  
3. matrix (artifacts)  
4. hypotheses (falsifiable)  
5. **predictions (verifiable)**  ← this repository

Flow: Kernel → Hypotheses → Matrix → Predictions  
Feedback: evaluation → (instantiation correction | hypothesis status change) → new run

→ Canonical governance: see `docs/README.md` (source: `research-program`)

## Core Rules

- Each prediction **must** be traceable to at least one hypothesis `H###`.  
- Each prediction **must** reference one or more runs: `RUN-YYYY-MM-###`.  
- **Manifest obligation** per run: versions, inputs, outputs, validation status.  
- Empirical failure is documented, not hidden (evaluations are artifacts).  
- “Verifiable” means: **operationally testable** – not “proven true”.

## Folder structure (current)

predictions/
├── README.md  
├── index.md  
├── runs/  
│   └── 2026-02-run-001/  
│       ├── manifest.yaml  
│       ├── inputs/  
│       ├── outputs/  
│       └── validation-report.md  
├── projections/  
├── evaluations/  
├── tools/               ← optional, strictly separated from artifacts  
└── schema/

## License

CC BY-NC 4.0

## Role in the epistemic flow

Predictions operationalize hypotheses within admissible structure.

They do not generate claims.
They expose consequences.

Outcomes may include:
- empirical support,
- empirical failure,
- instantiation refinement,
- STOP when evaluation cannot be meaningfully performed.

## Prediction lifecycle across layers

A prediction may:
- instantiate one or more hypotheses,
- generate runs and evaluations,
- trigger hypothesis revision,
- refine Matrix structure,
- or result in STOP when operational conditions collapse.

## Interfaces

- Hypotheses → define claims being operationalized
- Matrix → provides admissible structural context
- MMS → governs admissible transitions and evaluation constraints
- Predictions → expose consequences and empirical interaction
- Legacy → preserves runs that cannot be interpreted

## STOP vs empirical failure

Empirical failure concerns outcome mismatch.

STOP concerns evaluation inadmissibility:
the prediction cannot be meaningfully executed or interpreted under current constraints.

Both are recorded.

## External orientation

This repository is where the architecture encounters reality:
runs,
evaluations,
failure,
and operational limits.


