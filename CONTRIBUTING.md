# Contributing

## Neue Prediction hinzufügen
1. Nächste freie ID wählen: `P###`
2. Ordner anlegen: `P###/` mit `projection.md`, `evaluation.md`, `references.yaml`
3. Einen Run anlegen oder referenzieren (`runs/RUN-.../manifest.yaml`)
4. `index.md` aktualisieren.

## Run-Regeln
- Kein Run ohne `manifest.yaml`.
- Inputs/Outputs sind immutable pro Run.
- Evaluationen dokumentieren auch negative Ergebnisse.
