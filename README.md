# predictions

Versionierte, referenzierbare, **operativ überprüfbare** Projektionen  
als operative Schicht aus `hypotheses` + `matrix` unter MMS-Governance.

## Zweck dieses Repositories

Dieses Repository enthält **ausschließlich**:

- Projektionen / Konsequenz-Ableitungen („predictions“) aus expliziten Hypothesen (`H###`)  
- Run-Artefakte mit **Manifestpflicht** (Inputs/Outputs/Validierung)  
- Evaluationen inkl. dokumentierter Fehlschläge (Spiralmodell)

**Wichtig:**  
Hier gibt es **keine** neuen Hypothesen (die gehören nach `hypotheses`) und keine Black-Box-Optimierung / kein „Fitting“.  
Zulässig sind constraint-based Ableitungen, consequence maps, scenario trees und nachvollziehbare Übergänge.

## Architektur-Einbettung (Stand Februar 2026)

Layer-Reihenfolge (kanonisch):

0. legacy (inadmissibility)  
1. research-program (analytics)  
2. mms (dbms)  
3. matrix (artifacts)  
4. hypotheses (falsifiable)  
5. **predictions (verifiable)**  ← dieses Repo

Fluss: Kernel → Hypothesen → Matrix → Predictions  
Rückkopplung: Evaluation → (Instanziierungs-Korrektur | Hypothesen-Statuswechsel) → neuer Run

→ Canonical governance: siehe `docs/README.md` (Quelle: `research-program`)

## Core Rules

- Jede Prediction **muss** auf mindestens eine Hypothese `H###` zurückführbar sein.
- Jede Prediction **muss** einen oder mehrere Runs referenzieren: `RUN-YYYY-MM-###`.
- **Manifestpflicht** pro Run: Versionen, Inputs, Outputs, Prüfstatus.
- Empirisches Scheitern wird dokumentiert, nicht versteckt (Evaluations sind Artefakte).
- „Verifiable“ bedeutet: **operativ prüfbar** – nicht „bewiesen wahr“.

## Ordnerstruktur (aktuell)

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
├── tools/               ← optional, strikt von Artefakten getrennt
└── schema/

## Lizenz

CC BY-NC 4.0

