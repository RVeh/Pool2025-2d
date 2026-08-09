# Eine Abituraufgabe weitergedacht

## Materialien zum Artikel

Dieses Repository enthält die digitalen Materialien zum Beitrag

> Reimund Vehling: *Eine Abituraufgabe weitergedacht – vom berechneten
> Konfidenzintervall zur Verfahrenswahrscheinlichkeit und zurück*

Repository: [RVeh/Pool2025-2d](https://github.com/RVeh/Pool2025-2d)

Ausgangspunkt ist ein Aufgabenteil aus dem gemeinsamen Abituraufgabenpool der
Länder für das Jahr 2025. An der Aufgabe werden die Diskretheit der relativen
Häufigkeit, die Rolle der Standardisierung, die Entsprechung von Prognose- und
Konfidenzintervall sowie die tatsächliche Verfahrenswahrscheinlichkeit
entfaltet. Der so geschärfte Blick führt anschließend zur Ausgangsaufgabe
zurück.

Die Materialien verbinden zwei Zugänge: GeoGebra lädt zum unmittelbaren
Entdecken und Variieren ein; die Python-Notebooks machen Berechnungen und
Simulationen transparent, reproduzierbar und gezielt veränderbar.

## Direkt im Browser starten

Die Python-Notebooks können ohne Installation direkt im Browser geöffnet,
verändert und ausgeführt werden.

[![JupyterLite](https://jupyterlite.rtfd.io/en/latest/_static/badge.svg)](https://rveh.github.io/Pool2025-2d/jupyterlite/lab/index.html?path=0-Start.ipynb)

Als Einstieg dient die Datei [`0-Start.ipynb`](jupyterlite/content/0-Start.ipynb).
Sie enthält eine Übersicht und direkte Verweise auf alle Python-Notebooks und
GeoGebra-Dateien.

## Python-Notebooks

Die folgende Reihenfolge beschreibt einen möglichen Lernweg; die Notebooks
können auch einzeln verwendet werden.

### Von der Simulation zur Verteilung

1. [Empirische Verteilung der relativen Häufigkeit](jupyterlite/content/01-Empirische-H-Verteilung.ipynb)  
   Wiederholte Stichproben als Dotplot; auf Wunsch mit Prognoseintervall und
   markierten Punkten außerhalb.

2. [Verteilung der relativen Häufigkeit](jupyterlite/content/02-Binomialverteilung-H.ipynb)  
   Exakte Binomialverteilung von $H=X/n$ und ihre diskreten möglichen Werte
   $h=k/n$.

### Vom Prognose- zum Konfidenzintervall

3. [Konfidenzellipse und Wilson-Intervall](jupyterlite/content/03-Wilson-Konfidenzellipse.ipynb)  
   Vom Prognosebereich im $(p,h)$-Raum durch Inversion zum
   Wilson-Konfidenzintervall.

4. [Verfahrenswahrscheinlichkeit bei festem $p_0$](jupyterlite/content/04-Verfahrenswkeit-H-Sim-p0.ipynb)  
   Dieselben Stichproben in zwei Blickrichtungen: Realisationen von $H$ und die
   zugehörigen Wilson-Konfidenzintervalle.

5. [Verfahrenswahrscheinlichkeit: empirische $H$-Verteilung](jupyterlite/content/05-H-Verteilung-Ellipse-p0.ipynb)  
   Die empirische Verteilung von $H=X/n$ im $(p,h)$-Raum.

6. [Verfahrenswahrscheinlichkeit: Wilson-Konfidenzintervalle](jupyterlite/content/06-Simulation-Wilson-Intervalle.ipynb)  
   Die Intervallgrafik für sich: Überdeckung und Nichtüberdeckung als
   Denkraum.

### Verfahren vergleichen

7. [Drei Binomial-Konfidenzintervalle im Vergleich](jupyterlite/content/07-Konfidenzintervalle-Vergleich.ipynb)  
   Berechnung von Wald-, Wilson- und Clopper-Pearson-Intervall.

### Grafik zur Abituraufgabe

8. [Nahaufnahme im $(p,h)$-Raum](jupyterlite/content/10-Nahaufnahme-ph-Raum.ipynb)  
   Die Diskretheit von $H=k/n$ in der Nahaufnahme; Lösungshinweis zu einer
   Aufgabe aus dem Abituraufgabenpool 2025.

## GeoGebra

Die GeoGebra-Dateien sind vor allem zum unmittelbaren Entdecken und Variieren
gedacht. Sie können über die
[gemeinsame Auswahlseite](https://rveh.github.io/Pool2025-2d/)
direkt im Browser geöffnet werden.

| Datei | Schwerpunkt |
|:--|:--|
| [Lösung von Aufgabenteil 2d mit Standardisierung](jupyterlite/content/KI-freirubbeln.ggb) | Lösung der Abituraufgabe mit Schiebereglern und der Idee einer Standardisierung |
| [Verteilung von $H=X/n$: einzelne Realisationen](jupyterlite/content/Prognoseintervalle_einzeln.ggb) | Realisationen werden schrittweise erzeugt und als Dotplot dargestellt; das zugehörige Prognoseintervall kann eingeblendet werden |
| [Verteilung von $H=X/n$: mehrere Realisationen](jupyterlite/content/Prognoseintervalle_gesamt.ggb) | Eine vorgegebene Anzahl von Realisationen wird erzeugt und als Dotplot dargestellt; das zugehörige Prognoseintervall kann eingeblendet werden |
| [Wilson-Konfidenzellipse](jupyterlite/content/WaldWilsonBerechnungen.ggb) | Konfidenzellipse, Prognoseintervalle sowie Berechnung der zugehörigen Wilson- und Wald-Konfidenzintervalle |
| [Verfahrenswahrscheinlichkeit](jupyterlite/content/Verfahrenswkeit.ggb) | Dieselben Stichproben in zwei Blickrichtungen: Realisationen von $H$ und die zugehörigen Wilson-Konfidenzintervalle |

## Arbeiten in JupyterLite

1. Ein Notebook über einen Link öffnen.
2. Nur die Zelle **Eingaben** verändern.
3. Anschließend alle Zellen von oben nach unten ausführen.
4. In den Grafik-Notebooks werden mit `save_figure = True` PNG- und PDF-Dateien
   gespeichert. Der Unterordner `fig/` wird bei Bedarf automatisch angelegt.

Ein fest eingestellter `seed` macht Simulationen reproduzierbar. Alle
Notebooks trennen Eingaben, Prüfung, Berechnung, Grafik und Ausgabe sichtbar
voneinander.

## Python lokal ausführen

Vorausgesetzt wird Python 3.11. Danach genügen im Repository:

```bash
python -m pip install -r requirements.txt
jupyter lab
```

Eine lokale Installation ist für die Nutzung der Materialien nicht
erforderlich.
