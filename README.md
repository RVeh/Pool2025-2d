# Was hat ein Platz, was ein anderer nicht hat?

## Ergänzende Materialien zu Symmetrien bei zufälligen Anordnungen

## Python-Simulationen

Die Python-Notebooks können ohne Installation direkt im Browser geöffnet,
verändert und ausgeführt werden.

[![JupyterLite](https://jupyterlite.rtfd.io/en/latest/_static/badge.svg)](https://rveh.github.io/Pool2025-2d/jupyterlite/lab/index.html?path=0-Start.ipynb)

Als Einstieg dient die Datei `00_Start.ipynb`; sie enthält eine Übersicht und
direkte Verweise auf alle drei Simulationsprogramme.

Dieses Repository enthält die digitalen  Materialien zum
Beitrag

> Reimund Vehling: *Eine Abituraufgabe weitergedacht - vom berechneten Konfidenzintervall zur Verfahrenswahrscheinlichkeit und zurück*


## GeoGebra

Die GeoGebra-Simulationen können über die
[gemeinsame Auswahlseite](https://rveh.github.io/Pool2025-2d/)
direkt im Browser geöffnet werden.


### Positionen


## Python-Notebooks

| Notebook | Inhalt |
| --- | --- |
| [Simulation_Urne_ohne_Zuruecklegen.ipynb](jupyterlite/content/Simulation_Urne_ohne_Zuruecklegen.ipynb) | Relative Häufigkeiten \(h(A_j)\), exakte Invariante, Stabilisierung, bedingte Wahrscheinlichkeiten und hypergeometrischer Ausblick |
| [Simulation_erwartete_Positionen.ipynb](jupyterlite/content/Simulation_erwartete_Positionen.ipynb) | Positionen \(T_j\) der weißen Kugeln, empirische Erwartungswerte, Varianzen und Standardabweichungen sowie Spiegelsymmetrie |
| [Simulation_Luecken.ipynb](jupyterlite/content/Simulation_Luecken.ipynb) | Empirische und exakte Verteilung einer Lückenlänge, Erwartungswert, Varianz, Standardabweichung und punktweise Wilson-Konfidenzintervalle |

Alle veränderbaren Eingaben stehen jeweils am Anfang eines Notebooks.
Die Voreinstellung `seed = 42` macht die Simulationen reproduzierbar.



## Python lokal ausführen

Vorausgesetzt wird Python 3.11. Danach genügen im Repository:

```bash
python -m pip install -r requirements.txt
jupyter lab
```

Eine lokale Installation ist für die Nutzung jedoch nicht erforderlich:
Der Binder-Link am Anfang dieser Seite startet die Notebooks direkt im
Browser. Beim ersten Aufruf kann der Aufbau der Umgebung einige Minuten
dauern.
