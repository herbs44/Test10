# Raupen- und Käfer-Klassifikator

Ein einfacher linearer Klassifizierer, der anhand von Breite (`x`) und Länge (`y`)
eines Insekts entscheidet, ob es sich um eine Raupe (`1`) oder einen Käfer (`0`)
handelt. Die Trenngerade verläuft durch den Ursprung (`y = c · x`); trainiert wird
der Multiplikator `c` schrittweise aus den Trainingsdaten.

## Inhalt

- `Klassifikator.ipynb` – Jupyter-Notebook mit der vollständigen Herleitung:
  1. Vorhersagemaschine (wie in Teil 2)
  2. Erweiterung zu einem Klassifizierer (nur Korrektur bei Fehlklassifikation)
  3. Erweiterung: kleine Lernrate + mehrere Epochen, damit der Multiplikator
     sich langsam aus **allen** Trainingsdaten bildet statt nur aus dem zuletzt
     bearbeiteten Datensatz
  4. Auswertung auf den Testdaten (Trefferquote, Konfusionsmatrix, Plots)
- `daten/trainingsdaten.csv` – 1000 Trainingsdatensätze (Breite, Länge, Klasse)
- `daten/testdaten.csv` – 20 Testdatensätze im gleichen Format

## Ausführen

```bash
pip install -r requirements.txt
jupyter notebook Klassifikator.ipynb
```

## Ergebnis

Der final trainierte Multiplikator (`c ≈ 1.15`) trennt die Trainingsdaten mit
~99,8 % und die Testdaten mit 100 % Genauigkeit.
